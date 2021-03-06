---
layout: post
title: "ClickHouse: не сегодня"
date: 2018-08-12 00:52:49 +0300
categories: clickhouse
---
После месяцев экспериментов с ClickHouse отставляем в сторону. Не срослось, подождём ещё.

Прежде всего следует объяснить.

**Во-первых**, до этих экспериментов была изучена документация, был прочёсан интернет, были сделаны первые пробы. Про ограничения базы мы знали [ещё год назад], но решили проверить на практике, насколько нам (софту, процессам, людям) терпима та или иная особенность.

**Во-вторых**, интересно было поработать не только с аналитикой и бигдатой, но также и пощупать привычные сценарии. Что-то пощупали сами, что-то вычитали в чате и решили грабли обойти. На некоторые понаступали сознательно, измеряя толщину шишки.

В общем, если у вас при чтении возникнет желание сказать мне, что ClickHouse нидляэтава, не надо. Я знаю. ClickHouse сознательно прикручивался не только по прямому назначению. Получили в какой-то мере ожидаемый результат, зато теперь объективно знаем, с чем можем жить, а с чем не хотим.

---

Информации не хватает со старта. Вы ставите базу, заливаете первые десятки миллионов записей, выполняете простой SELECT и... он медленнее текущего решения в несколько раз. Т.к. *"ClickHouse не тормозит"*, пытаетесь избавиться от тормоза в руках. Но как? Документация всё ещё декларативна. Она неплохо описывает то, что есть в базе, но не отвечает на вопросы *"как?"*, *"зачем?"* и *"почему?"*

Учебников нет. Курсов нет. Доклады на конфах на такие вопросы обычно ответов не содержат. Community ещё крайне мало и не успело нагенерировать фигалиарды ответов на все вопросы. Исходник у ClickHouse в целом понятный и местами даже красивый, но вы точно хотите проводить обеды в листании тысяч строк на C++? Остаётся только чат: [t.me](https://t.me/clickhouse_ru). Он хороший и интересный, особенно когда народ новые билды пробует, но основным источником быть не может, да и не должен.

Потому сидишь и часами бьёшься бабочком об лампочку, перебирая варианты и в сотый раз перечитывая документацию вслух с выражением. А ежедневное чтение чата приводит к диалогам вроде *"давай эту штуку не юзать, я чёт такое нехорошее про неё неделю назад читал от того бойца, что... блин, забыл, кароч, что там у него было, но у него не получилось"*.

---

Чтобы построить минимальный кластер  ClickHouse, требуется пять машин: 2xClickHouse, 3xZooKeeper.

Этот показатель (количество машин) тоже важен, когда вы сравниваете траты и профиты на решение задач. Если база X при 10 машинах отдаёт данные по запросу S за 50ms, а база Y на 5 машинах по тому же S за 60ms, задумаешься. Это очень примитивный пример, но демонстрирует.

Другой показатель: количество разного софта. В одной схеме у вас на 10 машинах стоят 10 инстансов софта X, в другой схеме на 10 машинах 5 инстансов A, 3 инстанса B и 2 инстанса C. Разница в первую очередь заметна эксплуатации (админам, девопсам), но и разработчики не всегда рады, прямо скажем.

---

У ClickHouse было и осталось некоторое эмпирическое правило: вставлять по одной строке плохо, брать одну строку плохо. Ну т.е. медленно. В идеале бомбить пачками от тысячи строк.

Если вы не можете обеспечить без бубна эту пачечность, приходится ставить оный. Обычным уже решением Kafka. Источники в неё льют так, как получается, а на выходе стоит скрипт, который с некоторой периодичностью (раз в секунду, например) выгребает накопленное и льёт в ClickHouse. Казалось бы, ну ладно. Но помните про кластер 2xCH + 3xZK? Добавляем к нему минимальный 3xKafka, используя в целях уплотнения имеющий ZK. Уже восемь машин.

Можно бы пойти прямым путём: есть [Buffer](https://clickhouse.yandex/docs/en/operations/table_engines/buffer/) engine, вроде ровно то, что надо? Ну... Прочтите текст по ссылке внимательнее. С такими особенностями работы более прямым путём всё-таки кажется вариант с Kafka.

Особым местом оказывается и то, что переливает из Kafka в ClickHouse. В нашем варианте это простейший Python-скрипт, но у меня хватает фантазии, чтобы в будущем из этого скрипта вырос микросервис, сам по себе являющийся потенциальной точкой отказа. Не воодушевило.

---

Почти отсутствуют UPDATE и DELETE. Ещё недавно я бы не добавлял слово *"почти"*, но дело сдвинулось с мёртвой точки и теперь есть ALTER TABLE DELETE, пусть и *"in beta stage"* — уже ништяк! Но чёт как-то... Да, у нас есть данные, которые иногда приходится менять, пусть эти данные в теории и не должны меняться. Мир живой, люди живые, сплошь мутации и т.п. Реальность лупит теорию по голове и после пяти шаманств по изменению (фактически переналивались) захотелось больше так не жить.

С вариантом извращения в ситуации, когда UPDATE отсутствует, но очень хочется, можно познакомиться [здесь](https://www.percona.com/blog/2018/01/09/updating-deleting-rows-clickhouse-part-1/). Вот тоже не воодушевило.

---

Нет транзакций и в целом не очень понятно, какие гарантии и чего есть. Мы смелые и сердцем молодые, потому последний месяц наблюдали за ClickHouse, в который лились важные (те, что вот должны сохраняться, а если что, так откатить сохранение в случае ошибки) данные с production'а. И знаете... мне не очень понравился этот месяц.

MongoDB вам даёт "транзакцию" на уровне документа (про 4.0 пока не будем). Elastic тоже на уровне документа, если не ошибаюсь. Про всякие MygrescleSQL с их ACID и так все знают. Если база в ответ на INSERT мне ответила 200 OK, я спокойно переворачиваюсь на другой бок и сплю дальше. Если ClickHouse ответил мне 200 OK, хоть убейте, а сна нет. В общем случае я понятия не имею, сохранятся ли мои данные. Обычно сохраняются, но могут же и не.

Да, это привычно бойцам из мира аналитических баз и вообще бигдаты, ну а мне тревожно.

---

Тут россыпью всякое.

Внезапным камнем в ботинке оказался insert_quorum. Сначала мы хотели при INSERT в инстанс-A тут же убеждаться, что отреплицировалось в инстанс-B, но всё сломалось уже на этапе миграции данных в ClickHouse. Если слишком быстро писать в несколько потоков, начинаются (как я понял) конфликты вида *"я тут ещё не отреплицировал, а ты уже новое сбоку подкидываешь"*. В итоге insert_quorum выключили, что плохо. В чате потом ещё был народ с такой же проблемой, решения пока нет, окромя как лить в один поток.

Нет EXPLAIN. Хороший инструмент для анализа узких место в запросах, а нема. Есть со стороны [совет](https://ruhighload.com/clickhouse+explain) включить trace и читать логи, но я пока не созрел для того, чтобы на production'е трейсы оставлять. Смотреть на test / dev некоторые запросы смысла нет, современные планировщики учитывают и развёрнутые кэши, и статистику запросов и остальное, что вне боевой нагрузки в состоянии бутончика.

Всё так же пока нет окружения из удобных, наглядных и стабильных инструментов. Ткнёшься в угол, а там либо пусто, либо снова переписывают. Мне бы хотелось из DataGrip, но нет (впроечем, уже делают, если не ошибаюсь). Вроде мелочь, да и суровым постсоветским разработчикам хоть топором запросы делай, но таки хочется больше цивилизации с мещанскими окошками, кнопочками и графиками.

Индексы побаливают. Я привык к тому, что в MysgrecleSQL или в MongoDB накинул на десяток полей индексов и всё, живи, радуйся. В ClickHouse сложнее. У вас не получится использовать индексы произвольно. Технически говоря, отсутствуют secondary indexes, потому шаг влево-вправо вполне приводит к деградации скорости ответа.

---

Что в итоге? ClickHouse для big data, где big начинается с миллиардов строк и сотен гигабайтов. С этой планки вас начинают интересовать уже другие запросы (и они в ClickHouse отлично работают). До этой планки ClickHouse совершенно не нужен и даже вреден. Ничем иным, кроме как прям вот большими данными с только лишь аналитикой в ClickHouse ехать не следует. Транзакции, индексы, изменение данных, точечные запросы — все эти штуки из другого мира. Вернее, ClickHouse из другого мира.

Раньше я это понимал головой, ну а теперь и руками. Ну ок, будем ждать, вдруг база станет ближе повседневности. Появился же DELETE.
