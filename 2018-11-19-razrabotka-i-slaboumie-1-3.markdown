---
layout: post
title: "Разработка и цифровое слабоумие, 1/3"
date: 2018-11-19 16:53:02 +0300
categories: talk
---
// .., [часть 2.1/3](/2018/11/20/razrabotka-i-slaboumie-2-1-3/), [часть 2.2/3](/2018/11/23/razrabotka-i-slaboumie-2-2-3/), [часть 3/3](/2018/11/27/razrabotka-i-slaboumie-3-3/).

Следующие три эссе (проблемы, практика в разработке, пути решения) о связанных проблемах, про которые в России вообще почти никто не думает, хоть в США и Азии в набат бьют уже лет десять. Как мне кажется (да даже из наблюдений за собою), эти проблемы отражаются и на разработчиках, о чём давно думаю, а сейчас попробую сформулировать без особой снобистской иронии. Оснащать каждое утверждение ссылками не буду — две доступные на русском языке книги содержат достаточное их количество для верификации. Если читатель всерьёз заинтересуется, этого хватит для раскрутки. Мне не влом. Просто незачем. Авторы доступно и толково всё написали, дублировать их труд не вижу резона.

И это... я разработчик, а это не 500-страничная монография. Скорее, конспект конспекта, потому по всему тексту упрощение за упрощением, от чего неизбежно теряются важные детали. Если вам кажется, что проблема из пальца только на основе моего текста, вы превращаетесь в героя древнего анекдота (он же про Карузо, Моцарта, Битлз и т.д.):
> — Вот все говорят: «Карузо! Карузо!» А я послушал — так ничего особенного.  
> — Вы слышали Карузо?!  
> — Нет. Мне Рабинович напел.

Итак, проблемы.

---

**Цифровое слабоумие** (digital dementia, [статья (ru)](http://www.hij.ru/read/articles/view/5210/)). Интенсивное использование гаджетов [с детства] приводит к симптомам, схожим со слабоумием: плохая память, слабая концентрация внимания, слабый самоконтроль и т.д. Чем больше страна покрыта гаджетами, тем более явно исследования показывают массовые признаки диагноза. Первой не повезло Южной Корее, дальше США.

Упрощённо модель выглядит следующим образом. У вас есть организм, веками эволюции наработавший определённые механизмы формирования из креветки в опасного монстра. На уровне модели механизмы примитивны: если хочешь сильную руку, пользуйся ею. Комплекс из сильных рук, ног, спины и ушей даёт в итоге сильного человека. Мозг работает *примерно* так же, только качаются не мышцы. Что самое фиговое в контексте проблемы, мозг качает не автономные функции, но их клубок, который и считается личностью.

Что делают гаджеты? Чувак, тебе не надо изучать район, есть навигатор. Да, ты получишь топографический кретинизм, но гаджет поможет. Чувак, тебе не надо живьём общаться с людьми. Да, ты протеряешь навыки невербального общения, разучишься говорить ртом, получишь мешок расстройств социализации (то животное, что сидело с племенем у костра, никуда не делось). Но зато ты мгновенно можешь сказать какому-то рандомному хмырю, что он ошибается! Ну а с женой можно и завтра пообщаться. Наверное. Если жена есть. Память тоже не нужна, для этого есть Google (о чём ниже). Ну и что, что даже пятиминутный контекст диалога теперь вываливается из головы? Да, его не нагуглить, но можно переспросить или вообще поговорить о другом. Или о третьем, если причина другого тоже забудется. Зато гуглить! кликать! Википедия!

Пример менее очевидного замещения: ввести в школах электронные доски и копипасту текста вместо ручного труда (написать на доске мелом, переписать в тетрадь, стереть огрызком тряпки). Казалось бы, цивилизация, круто, детям прикольно. Не круто. Потерялась глубина обработки информации, мозг совершает меньше работы — копипастить дети учатся, а думать уже нет. Ну т.е. банально: за секунду копипасты вы скопипастили слово *"корова"*, а за минуту старательного каляканья прописью вы успели в подкорке и выше эту корову представить, погладить, нарисовать, да ещё раз десять мысленно дописать уже это чёртово слово. Что лучше запомнится? Отож.

Короче. Бездумная [полная] замена части мозга / действий гаджетами превращается в рандом, последствия которого сложно предсказать, но вроде как ничего хорошего для мозга не получается, т.к. гаджетам всего лет тридцать, а мозг несколько древнее и у него своя олдскульная жизнь, которую мы грубо ломаем благими намерениями.

Книга: [Манфред Шпитцер. *Антимозг. Цифровые технологии и мозг*. АСТ, 2013]. Собсно, чувак, который всю бучу поднял и подарил миру термин *"digital dementia"*. Поднял ну очень бодро, за что ожидаемо схлопотал как волну *"да, ты наш кумир! наконец-то кто-то сказал правильно!"*, так и волну *"КГ/АМ, давайте больше смартфонов"*. Как обычно, в общем.

---

**Цифровая амнезия** ([wiki](https://en.wikipedia.org/wiki/Google_effect)). Если мозг «знает», что вы можете добыть (нагуглить) информацию ещё раз, он её не запоминает. Обнаружилось недавно, находится на стадии обсуждения, выявления и критики. Основой принят эксперимент, результаты которого опубликованы в 2011 году. Чуваки читали всякие слова. Одной группе сказали, что потом слова будут удалены из памяти компьютера. Другой группе сказали, что удаляться не будут. В итоге первая группа лучше запомнила слова, а вторая группа лучше запомнила директории, в которых слова находятся.

Как по мне, сам эксперимент несколько... стрёмный по методу и выводам, но зато он поднял в обществе очередную дискуссию о том, следует ли вообще запоминать факты. Ну т.е. нафига мне помнить, какое там отчество у Сталина, если я могу это отчество нагуглить? Дискуссия ведётся давно, берегами упирается и в школьное образование, и в стандарты знания, и во влияние кругозора на *"успешность в жизни"*, всё такое.

Рациональное в этой войне, как мне кажется, находится в той области, которую затронул автор книги ниже. Есть ли связь между тем, сколько фактов о мире вы помните, и тем, какой у вас доход? Есть ли связь между кругозором и обоснованностью решений? Влияет ли общий кругозор на специальную работу специалиста? На что вообще влияет эрудиция и кому она нафиг нужна? Наконец, как объяснить связь (вроде даже и не ложную) между кругозором и той самой успешностью?

Продолжением этой рациональности размышления о том, какие механизмы мозга мы используем для запоминания фактов и как неиспользование этих механизмов (гуглим!) влияет на человека? Вот Вася, Вася умеет пользоваться Google и за год вместо запоминания сотни фактов сто раз нагуглил и забыл из них 4/5. А вот Петя, Петя не гуглил, но брал в библиотеке книги, внимательно читал и вычитал сто фактов, из которых забыл 2/5. Если пронаблюдать за Васей и Петей лет пять-десять, что увидим? Значит ли эта разница то, что Вася меньше использует мозг и в целом (на сотне ситуаций, допустим) покажет себя хуже, чем Петя? Сделает свою работу чуть хуже, из ассортимента решений выберет не самые удачные, не увидит и не воспользуется шансом, мелькнувшим на горизонте.

Книга: [Уильям Паундстоун. *Голова как решето. Зачем включать мозги в эпоху гаджетов и Google*. Азбука Бизнес, 2017]. Книга не прорывная и не особо интересная. Фактически представляет собою детальный и многословный срез знаний в США за последние лет десять. Между результатами опросов автор приводит примеры бардака, ну и прослеживает некоторые связи между. Читать не всегда просто, т.к. тяжело оценить вес незнания американцами чего-то типа *"сколько в США сенаторов?"* Но... но. Увидеть картину невежества по стране — интересно. Узнать о том, каких связей не обнаружилось (скажем, грамматические ошибки в меню ресторана не влияют на желание людей в этом ресторане питаться) — интересно.

---

В сумме с остальным (влияние информационного шума, например) по миру эти две милые штуки показывают довольно фиговую тенденцию. Уровень образования повышается, а качество людей падает. Иными словами, человек в 1960-х годах из десяти книг добывал информации больше и с большей пользой, чем человек 2010-х годов добывает из сотни источников. У американцев наблюдение за происходящим вызывает несколько более тёплое офигение, т.к. внезапно обнаруживается, что при развитой системе голосования за всякое голосует фиг знает кто фиг знает за что. С одной стороны правительство и организации вбухивают миллиарды американских денег в образование, с другой стороны почему-то кнопочки нажимают чуваки, у которых в голове даже ФИО кандидатов не задерживаются дольше минуты.

И ладно бы сидели ворчуны на лавочках и ныли про более мокрую траву в молодости. Обнаруживается тенденция, вот вам ещё один древний анекдот:
> Чукча достал где-то учебник по философии и стал с интересом его читать. Пока читал, стадо оленей убежало далеко, и вот сорвался с обрыва один олень, за ним другой, потом третий. Чукча, оторвавшись от чтения, констатировал: «Тенденция, однако»...

Вот как-то такие же падающие олени сейчас один за другим год за годом, но вместо оленей уровень ответов на элементарные вопросы.

Наконец, волнение в рядах задумывающихся вызвано и тем, что всё связано. Ослабили память — среди прочего ослабился темп переработки информации. Ослабился темп — замедлилось построение семантических структур. Меньше готовых семантических структур — человек просто меньше знает, зачастую нужного. Забегу вперёд, но уже по исследованиям 1980-х годов у программистов со временем формируется большой набор шаблонов ("семантических структур"), которыми программисты оперируют, потому, скажем, при чтении исходника опытный программист "видит" не буквально операторы, но эти шаблоны в коде. Что прикольно, т.к. потом при воспроизведении кода "на доске" эти чуваки воспроизводят код не слово в слово, но структура в структуру, замещая исходник эквивалентными операторами.

Т.е. нет, это не просто *"Вася стал немножко хуже помнить"*. Это *"Вася стал немножко хуже всё[, если хитрый мозг не наработал компенсацию]"*.

---

Тут что ещё надо принимать во внимание...

**Во-первых**, у технарей часто присутствует скепсис в сторону психологов и социологов. Это нормально и местами даже правильно. Но если вы начнёте копать тему, увидите, что над описанными проблемами работают вполне серьёзные специалисты по нейронаукам, а часть экспериментов (с каждым годом всё больше) проводится не опросами населения, но электродами в мозг, так сказать. За десять лет накоплен большой массив объективных данных, потому просто отмахнуться, мол, пф, снова эти болтологи себе занятие придумали... ну... антиразумно.

**Во-вторых**, даже этот массив данных пока недостаточен для однозначных выводов. Мозг сложный, люди сложны, железки разнообразны, между «хорошо» и «плохо» тьма промежуточных комбинаций, всё такое. Такое шаткое состояние даёт огромное поле для манипуляций и одноразовых скандальных выкриков (особенно от политиков и журналистов). Картина хоть как проясняется только после отшелушивания *«учёные хотят запретить смартфоны!»* и *«учёные доказали, что компьютеры вредны здоровью!»*. Не хотят. Не вредны в мере для запрета. Будьте осторожны, читая статьи. Сейчас нащупывают границу вреда, не более. А тревогу поднимают алармисты, видящие, как осознание последствий прогресса ни фига не успевает за прогрессом.

**В-третьих**, относитесь подозрительно к собственной картине мира. Образно говоря, есть вы (Я с мнением), есть мозг (с собственным «мнением»), есть вы-мозг (та часть, которую вы контролируете). Также учитывайте, что эта система постоянно меняется, а последствия могут явно проявиться совсем не сразу. Если вы сломали руку, вы видите (иногда) перелом, вам больно, вы сразу реагируете. Тут просто. Если вы отупели (и нет явной причины в виде гвоздя в черепе), у вас не получится в быту отследить начало процесса, вовремя заметить, да и вообще прям вот заметить. Нет у нас такой обратной связи. Ну и куда же без внутренних монологов *«а не отупел ли я? да ну, бред какой-то! так, это что, голова..? пойду в неё поем»*.

Продолжение следует.
