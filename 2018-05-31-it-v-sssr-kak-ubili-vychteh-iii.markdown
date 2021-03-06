---
layout: post
title: "IT в СССР (как убили вычтех, развязка)"
date: 2018-05-31 00:24:27 +0300
categories: it_ussr
---
Повторюсь и ещё раз скажу, что умных голов было много, потому о проблеме зоопарка думали на всех уровнях ещё с конца 1950-х. Без высокой степени совместимости невозможны проекты ЕГСВЦ [Китова](https://ru.wikipedia.org/wiki/Китов,_Анатолий_Иванович) (1958..59 гг.), ОГАС [Глушкова](https://ru.wikipedia.org/wiki/Глушков,_Виктор_Михайлович) (1962..198x гг.), проект, мелькнувший в архивах [Ершова](https://ru.wikipedia.org/wiki/Ершов,_Андрей_Петрович), [сайт](http://ershov.iis.nsk.su/russian/) которых упорно лежит (1964 г.). Эти проекты сами по себе очень интересны и погибли по другим причинам, об этом в другой раз, возможно. Факт в том, что не проснулись однажды с осознанием, видели и размышляли.

Но размышлять мало, надо делать. А это не получилось. Сейчас коллективы разработчиков и заводчан назвали бы "недоговорными". Вы могли договориться с кем-либо в личном порядке, но если требовалась официальная поддержка... Беда. Госплан, бюрократия, очереди производства, подковёрная грызня ведомств, планы, сроки, внезапная срочность к знаковым датам.

Попробуйте сами. Вы Иванов, главный конструктор ЭВМ Петя-1, у вас за плечами десять лет оригинальных архитектур и десятки людей в коллективе. И есть Сидоров, главный конструктор ЭВМ Вася-2М, у которого тот же анамнез. Приходит к вам Сидоров и вы за чайником чая обсуждаете унификацию всего. Согласны. Унификация рулит. Но из этого следует, что часть уж очень оригинальных архитектур надо выбросить, а часть переделать, внедрив общие компоненты. Скажите, Иванов, вы готовы отказаться от Пети-1? От государственных наград? От премий? От места автора первой в мире полуторичной 11-разрядной квадратно-выпуклой ЭВМ, выдающей 146 операций в венерианскую секунду? А в глаза коллективу посмотреть? Это что же, они тоже всего лишаться? И все эти годы они неправильное делали? А как вы своему министерству объясните, что Сидоров из другого министерства более стратегически разработку вёл? В конце концов, это у Сидорова его Вася-2М фигня, а вот у вас уж точно наикрутейший Петя-1!

Внутри СВОИХ систем конструкторы занимались унификацией, конечно. Нормальный инженер не может этим не заниматься. Особо достоин упоминания [Рамеев](https://ru.wikipedia.org/wiki/Рамеев,_Башир_Искандарович), заложивший в своих [Уралах](https://ru.wikipedia.org/wiki/Урал_(компьютер)) потенциал единой линейки ЭВМ на разные уровни задач. Но и всё, пожалуй.

---

В таких ситуациях приходит руководство и принимает волевое решение. Могло и позже, наверное, но с 1965 года по миру начались поставки гениальной в производстве, унификации и развитии [IBM System/360](https://en.wikipedia.org/wiki/IBM_System/360) (тут все разработчики встали и поклонились упоминанию источника восьмибитовой чумы), которая прям вот была почти именно то, что всем надо было. Руководство напряглось и обратилось к экспертам, требовалось разработать аванпроект ОКР *"Ряд"* (линейка машин, совместимость и прочее).

Эксперты (ИТМиВТ во главе с [Лебедевым](https://ru.wikipedia.org/wiki/Лебедев,_Сергей_Алексеевич)) в ответ в 1966 году выдали вялый 50-страничный отчёт. В нём скептически отозвались об IBM 360, да и ничего толкового не предложили. Министерство озадачилось. Каждый крупный коллектив вместо общей архитектуры толкал свою (Москва, Киев, Минск, Ереван, Пенза). Министерство озадачилось ещё больше. Ведь всё честно сделали. Дали учёным и конструкторам возможность высказаться, выработать общий вектор. Не получилось. Ну ок.

Разработку аванпроекта поручили сторонникам (как понимаю по [воспоминаниям](http://www.computer-museum.ru/histussr/es_levin.htm) [Левина](https://ru.wikipedia.org/wiki/Левин,_Владимир_Константинович)) выбора IBM 360 в качестве основы и всё было решено ещё ДО января 1967 года (заседание, на котором решение утвердили) и уж точно до 1969 года (финальное совещание с ведущими разработчиками). Почему я считаю, что решено всё было ДО?

Большинство стран, участвовавших в "Ряде", было против IBM 360, топили в пользу английской [Системы-4](https://en.wikipedia.org/wiki/English_Electric_System_4). Только ГДР, уже осваивавшая систему, была за американцев. Большинство участников совещания 1969 года были против IBM 360, топили за Систему-4, раз не получилось своё проработать. Основные аргументы были очень весомыми:
* СССР не мог покупать у IBM ничего, ибо эмбарго.
* К моменту клонирующего производства IBM 360 уже была бы значительно устаревшей системой 10-летней давности.
* Связей с IBM нет никаких и не предвидится, потому никаких стажировок, поддержки и остального.
* С англичанами уже связи, уже стажировки, уже готовность к поставкам, помощи, обучению, наладке.

А со стороны сторонников аргумент один: у IBM 360 огромный богатый софт, на который ушли тысячи человеко-лет, мы круто победим, его стырив через тех же немцев. Ура-ура. По пути и свой напишем, не беда. Потому IBM 360, всем спасибо, расходитесь.

Накал был такой, что в оставку тут же подали [Сулим](https://ru.wikipedia.org/wiki/Сулим,_Михаил_Кириллович) (ему предстояло объяснять англичанам срыв всех предварительных договорённостей) и Рамеев (понимавший последствия принятого решения и тоже участвоваший в процессе с Системой-4).

---

После чтения [конспекта](http://lib.ru/MEMUARY/MALINOWSKIJ/7.htm#4) заседаний и докладных и вообще осмыслении у меня следующие соображения... За два-три года до 1969 года все узнали мнение всех сторон. И это мнение не менялось. Именно обсуждения и диалога я нигде не нашёл. Стороны только фиксировали свою позицию и больше не колебались. Это инженеры и администраторы довольно небольшой прослойки, не первое десятилетие знакомые. Битые жизнью, партией и вообще. Уверен, для них не был сюрпризом ни итог 1967 года, ни итог 1969 года.

Да, это глупый выбор. Очень наивный, очень оптимистичный. Но у него есть причины.

Официальная нередко за кадром в блогах или без акцента, а я акцентирую: острая нехватка программистов и программ. Компьютеры без софта не нужны. Софт пишут программисты. При разработке новой системы требуется новый набор ВСЕГО для всех отраслей от операционной системы до складских журналов. Делать этот софт было некем. Отсюда и такой упор на то, что вот у IBM овердофига всего, писать заново не надо, достаточно обеспечить совместимость. На 70% выбор архитектуры был вызван выбором программного обеспечения.

Неофициальная, мне кажется, тоже имеет право на. Вы министр. Перед вами разработчики компьютеров, которые за годы не смогли договориться и выпустить единое. Перед вами заводы, которые за годы не смогли наладить стабильное и качественное производство. Перед вами программисты... ах да, их нет. А те, что есть, развлекаются переписыванием кода под 25+ систем. Перед вами Госплан и партия, которые вообще понятия не имеют, чего хотят, но хотят этого очень. Вот вы точно будете тем же людям давать вариант, с которым они уже не справились? 20 лет анархии, феодализма и махновщины. Давшие интереснейшие результаты для науки, но не учитывавшие интересы страны.

Вот, собсно, начальственный тапок по столу и стукнул. В этой истории отлично выступили все. Интересно отметить и то, что упускают из виду те, кто упоминает Уралы в качестве альтернативы: Уралы не выдвигались. Это замечательный ряд машин с большим заделом, готовые для сети, пошедшие в серию. Но напомню: каждое КБ тянуло одеялко на себя и фантазировать на тему *"советские конструкторы единым фронтом выступили за отечественную разработку [любого конструктора]"* не стоит. Не было такого. Этот шанс тоже профукали.

---

С 1969 года и отсчитывают начало конца. Но почему? Всё-таки за основу взяли популярную и мощную систему. Да и выпуск своих систем не прекратили, да и вовсе продолжили разрабатывать. Как и ожидалось, не всё просто.

---

Продолжение следует.
