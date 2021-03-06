---
layout: post
title: "Почему Python и Django"
date: 2018-08-04 17:12:56 +0300
categories: talk
---
После ряда вопросов дополню предыдущую [простынку](/2018/08/01/kak-zarabotat-bolshe/) ответами на вопросы ряда *"почему [не] XYZ"*.

По себе знаю, профессиональная деформация меняет угол оценки людей. Если день за днём 90% круга общения могут читать исходники, упоминать [big O](https://en.wikipedia.org/wiki/Big_O_notation), ностальгировать по [ZX Spectrum](https://en.wikipedia.org/wiki/ZX_Spectrum) и гадать про [Эльбрус](https://ru.wikipedia.org/wiki/Эльбрус_(компьютер)), забываешь очевидное — другим людям бывает сложно даже AND от OR отличить. Они умеют включать компьютер, гулять в интернете, писать письма. Всё. Это раз.

Программирование не является естественной деятельностью человека. Фактически никакой предварительный опыт к ЭТОМУ не готовит. Сугубо умственное самонасилие, структурирующее мысли так, чтобы после конвертированиях оных в примитивные инструкции процессора что-то заработало. Вспомните, как мучительно застывал народ перед первыми банкоматами. Итическая мощь цивилизации, какую же кнопку нажать, чтобы денег дало..? Левую или правую? Или вот эту посерёдке? Аааа, оно жужжит! Вот первый опыт разработки круче банкомата.

Короче говоря, я не сторонник фантазий о том, как из толпы выдёргивают рандомную репку и за месяц из неё куют разработчика на любом языке. Выдрессировать обезьяну, бездумно повторяющую действия по шаблону — да, реально. Остальное считаю кунсткамерными казусами, цели и нюансы которых многое бы объяснили. Ну и да, [великий рандом](http://lurkmore.to/Рандом) существует.

---

Итак, формулируем задачу.

Дано: обычный человек без опыта, но умеющий пользоваться компьютером. Мощность мозга примерно на уровне хорошиста с дипломом. Инициативность и воля на уровне *"готов оторвать жопу от дивана, чтобы жить иначе"*. Снижать планку не считаю интересным — люди с тройками и двойками, продавливающие телами печку в надежде на чудо... тоже чего-нибудь как-нибудь найдут своими методами, пусть их. Мне такие тоскливы, потому избегаю. Повышать же планку неспортивно, современный толковый физмат применение себя уже во время учёбы может найти без проблем.

Задача обширнее, многоэтапная и на века:
* Попасть на высокооплачиваемую (относительно другой "обычной") первую работу.
* Удержаться год на этой работе.
* Полученными знаниями и опытом значительно расширить выбор следующих мест и вариантов работы.

Ограничения:
* Самостоятельная учёба. Во-первых, проверка мотивации — не тянешь, значит, не хочешь, пока-пока. Во-вторых, не тратимся на бесполезные курсы, повторяющие то же, что есть либо бесплатно, либо за весьма меньшие суммы.
* Уложиться в год по два-три часа в день. Вполне возможно, человек уже работает или учится [на кассира в свободной кассе с высшим филологическим]. А года хватит на всё. Если потребовалось больше, что-то не так.
* Москва. Просто трусливый выбор, т.к. понятия не имею, как джуниору найти работу в Красноярске или в Бахчисарае.

Временные затраты: при режиме будень(30м чтение + 90м практика) и выходной(60м чтение + 120м практика) получаем на год с округлениями... около 250ч чтения и 600ч практики, если я не обсчитался по производственному календарю.

---

Самое это самое: какой язык? Мы можем выбрать только один основной. Выбирать, понятно, топовый. Много учебных материалов, вероятность найти советчика под боком, больше вакансий и т.д.

[Go](https://en.wikipedia.org/wiki/Go_(programming_language)) и [Rust](https://en.wikipedia.org/wiki/Rust_(programming_language)) отметаем — хватит и того, что работы мало. [Swift](https://en.wikipedia.org/wiki/Swift_(programming_language)) мог быть вариантом, но мобильная разработка специфична и всё то же количество вакансий. [C](https://en.wikipedia.org/wiki/C_(programming_language)) / [C++](https://en.wikipedia.org/wiki/C%2B%2B)... хороши, но для изначально профессиональных джуниоров, я бы сказал — многое надо знать дополнительно, на собеседовании спросят и про разный low level, а у рандомной репки беда. Ну и снова вакансий так себе. Есть ещё кластер всякого вокруг Microsoft ([C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)), например), но у меня в этом месте лакуна, а гадать не хочу. Может, у них всё офигительно. С другой стороны, учебной литературы на порядок меньше, да и платформа ограничивает вакансии. У [Ruby](https://en.wikipedia.org/wiki/Ruby_(programming_language)) всё плохо с количеством информации, вакансии тоже не очень. Остаются [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), [JavaScript](https://en.wikipedia.org/wiki/JavaScript) и [Python](https://en.wikipedia.org/wiki/Python_(programming_language)).

Java великолепна на рынке труда. Работу найдёт даже джавист с тремя судимостями, опытом в месяц, образованием в два класса церковно-приходской в деревне староверов, глазами наркомана и повадками сомалийского гопника. Но это не язык для начинающих с самостоятельным обучением. Чтобы начать на ней писать хотя бы похоже на правильную Java, надо прям вот долго и с ментором, ещё и помнить тонну нюансов. Собсно, потому количество литературы по ней огромно, но доля учебников для самых маленьких исчезающе мизерная. Маленьким этот язык не дают.

JavaScript тоже прям сверкает вакансиями. И материала много. И в каждой щели он. И учить просто, да ещё снежинки с часиками на экране. Одна фигня: рынок JavaScript — это рынок фронтенда с редкими вкраплениями *"мы пишем на [Node.js](https://en.wikipedia.org/wiki/Node.js)"* (скорее, на Ноде будете вспомогательные скрипты фронту писать). Иногда в дискуссиях с матёрыми джаваскриптизёрами начинается выдвижение списка софта на Node.js, но в сравнении с Java / Python... вышла шаланда под [ГРКР *"Москва"*](https://ru.wikipedia.org/wiki/Москва_(ракетный_крейсер)). Также фронтенд со старта не учит многому хорошему (нафига снежинкам алгоритмы, например?), да и вообще ограничен в качестве вакансий. Оптимистично говоря, бекендер может вчера писать банковский софт, сегодня геймдевить, завтра машинное обучение в [Hadoop](https://en.wikipedia.org/wiki/Apache_Hadoop) ломать. Фронтендер вчера верстает страничку для банковского софта, сегодня страничку для игры, завтра страничку для админки машинного обучения. Утрирую, да. Но и нет. При этом просто *знакомить* с разработкой на примере JavaScript отлично.

Python достаточен вакансиями. У него всё замечательно с литературой (даже детской хватает). Его берут учебным языком в вузах — современный BASIC, чё, вона как [SICP](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs) им... не подберу глагол. Он нередко приветствуется вторым языком. Переживает второе рождение в ML. Многолетние legacy на нём ещё ваших внуков пережить могут. И для простых задач он простой как ведро с краской. И, что очень важно в контексте, питонистам не надо знать ничего (заранее отключить комментарии к эссе, шоле...)! Плюсовиков погоняют по low level и OS. Джавистов по ООП, шаблонам, API и GC, придавив многопоточностью и *"ну, теперь давай про базы данных"*. Этих, которые JavaScript, будут спрашивать про [React](https://en.wikipedia.org/wiki/React_(JavaScript_library)) во [Vue.js](https://en.wikipedia.org/wiki/Vue.js) с [AngularJS](https://en.wikipedia.org/wiki/AngularJS) в соусе из [jQuery](https://en.wikipedia.org/wiki/JQuery) в Internet Explorer на семиугольном мониторе. Питонистов не спрашивают ни о чём, окромя Python и одного из фреймворков, да и тому научат. Лишь бы лапками по кнопкам нужным попадал в первый год. Ну не прелесть? А уж освоить и запомнить за год Python так, чтобы от зубов отлетал, не хитрое дело.

Потому и Python. Что, впрочем, не помешает в дальнейшем изучить другой язык, было бы желание. Ещё отмечу наблюдение из практики: очень, очень часто питонисты (как живые люди, так и резюме) — выходцы из тестировщиков, 1С, поддержки и прочих мест, в коих разработка на зачаточном уровне, если вообще есть. Python — их первый и нередко единственный язык. Они смогли, сможет и наша репка.

---

Подчеркну всё-таки важное. Начинающему следует не просто найти первую работу, но за два года учёбы и работы открыть себе двери в разные ветви разработки. Ведь лучше работать тем, что нравится, а не только тем, что умеешь. В Python легко войти и с Python легче пойти дальше в девопсы, в админство, в web, в ML, в сбор данных и т.д. Когда первый голод удовлетворён (ура, я пишу программы! ура, мой первый миллион [рублей]!), бывший начинающий пойдёт дальше. И вот тут должны выстрелить дополнительные знания и появившаяся привычка учиться. В этой же точке привычка быть бездумной обезьяной с сотней CtrlC/CtrlV на пальцах закроет ряд вариантов, я уверен.

А вот это не подчеркну, но отмечу [ещё раз]: разработка софта очень толерантна к разным людям разного уровня. Войти в разработку можно миллиардом путей. Если у начинающего есть явные наклонности к несколько иной ветви развития (пусть даже ценою снижения универсальности), может хоть [Fortran](https://en.wikipedia.org/wiki/Fortran) осваивать по аудиозаписям лекций. Фишка в доступности. Запрыгнуть на первую ступеньку может любой с желанием, волей и достаточным количеством полезных клеток в черепе.

PS. Выбор [Django](https://en.wikipedia.org/wiki/Django_(web_framework)) в качестве фреймворка объясняется просто. Во-первых, в ней (нём?) есть всё для обучения, ничего дополнительного ставить не надо. Во-вторых, количество вакансий с упоминанием Django довольно велико — прям сейчас 200+, например. В-третьих, после Django освоить другое не так уж сложно.
