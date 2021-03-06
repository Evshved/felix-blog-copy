---
layout: post
title: "Разговор о сроках"
date: 2020-08-11 11:00:00 +0300
categories: talk
---
Присутствовал на совещании, задавал вопросы. До вопросов одна дата была, а после вопросов стала другой. Давайте кратко конспект о том, как правильно слушать обсуждение сроков и какие вопросы надо задавать.

Обязательная вводная: навсегда следует приучить себя и окружающих к тому, что к какой-либо дате должно быть привязано не воздушное без формы *«ну я чёт сделаю, да»*, но максимально конкретные ответы на *«что именно будет сделано»* (какой модуль? какая функциональность из ТЗ? какие тикеты из трекера?), *«в какой степени готовности»* (альфа? предрелиз? продакшен? прошло QA? только разраб потыкался?), *«кем именно будет сделано»* (либо кто отвечает на вопросы, если эти вопросы появятся). Казалось бы, если у вас есть план (особенно у тех, кто у водопада), ответы в плане. Но нет, планы далеко не всегда учитывают содержание процессов, они задают форму и цель, а вам до неё шагать по буеракам.

А чтобы получить такую конкретику, аморфное следует оформить.

Итак, беглая категоризация того, что влияет на сроки и нередко слышится и читается разными людьми по-разному. В какой-то мере этот можно принимать за методичку джуниорам. Наверное.

---

**Во-первых**, выделяйте блокеры -- то, что однозначно и без вариантов мешает выполнять задачу хоть в каком виде. Даты разрешения блокеров являются реперными точками плана.

Например, поступила задача написать драйвер для изделия *«Миллениал-17 ЧМ»*. А есть ли документация на изделие? А есть ли само изделие? А в достаточном ли количестве (и не будет ли команда толкаться локтями у единственного экземпляра, замедляясь в разработке)? А если нет, то *когда* будет? А кто отвечает за доставку? Ага, Петров. А все помнят, что сейчас 24 марта, а Петров в отпуске до 5 апреля? А все помнят, что коммуникация с заводом *«Милмашзавтвит»* всегда два-три дня минимум? И железке оттуда тоже дня два-три в лучшем случае. И да, на выходных они не работают почему-то. Такой завод. Т.ч. хоть убейся, а раньше 12 апреля на руках у нас ничего нет и не будет. Следовательно, от текущего момента до любых практических работ у нас лаг в 18+ дней, товарищи.

---

**Во-вторых**, *«почти сделано»* -- не сделано. И *«да на 90% сделано»* тоже. И даже *«на 99% сделано»*.

Можно сказать, что инициация менеджеров происходит не как у индейцев (высидеть жопой на муравейнике и не заплакать), но в момент, когда они перестают верить слову *«сделано»*, но сжимают челюсти на слове *«почти»*. Иногда вы получаете задержку по сроку выполнения работ на 100%, т.к. разработчик сдвигал на финал то, что ну никак не получалось. Оп, а оно всё так же не получается. Неделю. Другую. И каждую неделю вы будете слышать *«да на 90% сделано»*.

Соответственно, едва слышите что-то подобное, двигайте даты вперёд.

---

**В-третьих**, если разработчик что-то сделал и говорит, что оно работает, ведь *«я потестировал вчера, всё ок»* -- оно не работает. Или работает на те самые 90% из предыдущего пункта.

QA / ОТК придуманы не просто так. В идеале всегда проверять работу должен кто-то посторонний. Причин тому хватает:
* проверка -- отдельный и обширный род деятельности, специальность, которой разработчик обычно не владеет [в должной мере];
* у разработчика замыливаются глаза и руки -- тридцать раз проходишь по коду, а мимо проходящий Пётр секунду смотрит на экран и тут же тыкает пальцам -- Васян, а чего у тебя условие на x, а не y?
* у разработчиков есть склонность проверять себя по [happy (golden) path](https://en.wikipedia.org/wiki/Happy_path) -- протыкивать комбинацию, которая совершенно точно работает, и не проверять остальные.

Соответственно, всегда выясняйте, таки кто и как проверял что-либо, после чего сдвигайте срок.

Например, поступила задача внедрить в проект библиотеку *«Паразит»* -- разработка соседнего отдела. Отдел говорит, что библиотека работает, хоть сейчас линкуй и в бой. Нет, давайте сначала спросим, почему они считают, что библиотека работает: кто проверял? по каким сценариям? а ваш сценарий там был? В половине случаев ответы приводят к простому -- вы будете ещё и тестировщиком *«Паразита»*, что сдвигает даты.

---

**В-четвёртых**, между написанным кодом и готовым продуктом есть большая разница.

Разработчик может сказать *«я сделяль»*, когда у него проект собрался, запустился, все кнопки нажались и отпустились. А руководство может считать, что *«я сделяль»* наступает, когда у заказчика в машзале лампочки замигали и поползла первая перфолента с результатами. И упаси вас боженька вашей религии от молчания в следующей ситуации:  
-- *Евгений, а давайте спросим разработку... Олег, когда будет готово?*  
-- *Думаю, в июне, Игнат Васильевич.*  
-- *Ну и отлично, ну и молодцы.*  

Если вы руководитель или менеджер, ответственный за проект, у вас в этот момент должна запуститься первая ступень под задницей. Всегда, всегда намертво назубок помните, что самый настоящий финальный *«я сделяль»* -- проект со всеми выполненными работами по договорам (или тикетам, планам, поправкам), включая сопутствующую документацию и/или инфраструктуру и/или ещё чем-либо вплоть до одобрения приложения модераторами AppStore. И вы можете здорово пролететь, если другая сторона подразумевает именно этот финал, а вы бездумно подразумеваете сырую заготовку для тестирования.

PS. Ну и да, это одна из причин, по которой разработку стараются держать подальше от власть влачащих. Как ляпнут, так лысеешь.

---

**В-пятых**, на выходных люди не работают. А если работают, то не так, как в будни.

Не считал, сколько раз Васян говорил *«я за выходные доделаю»* и за выходные не доделывал. Не знаю. Много. План, внутри которого есть надежда на работу в выходные и/или праздники -- плохой план. Руководитель, считающий результативность таких дней равной результативности буднего дня -- наивный. Ни фига так не работает.

Тут сразу можно побить себя пяткой в грудь, обещая и прочее, но если вы на совещании слышите, что кто-то, от кого зависят ваши сроки, говорит, что будет работать на майских, двигайте сроки на 5..6 дней вперёд. Оно мудрее будет.

---

**В-шестых**, подготовка к работе -- тоже работа.

Тоже не раз замечал, как из тайминга проекта словно за кадр уходят подготовительные работы. За редким исключением всегда есть что-то, что у команды отсутствует и это следует либо выучить, либо раскатить, либо выцыганить, либо закупить, либо определиться с тем, надо ли оно или же можно обойтись. Да те же совещания. Примеры на пальцах и с потолка:
* на работы дали два месяца, а у нас по два часовых совещания в неделю -- два рабочих дня вне поля зрения;
* нужно купить и поставить и обучиться хоть бегло требуемой IDE -- часы вне поля зрения;
* на совещании как-то мельком упомянули про изучение даташитов и выделили пару часов пацанам, а чё -- а даташиты оказались по 300 страниц убористого гранита -- влетели на пару дней.

И т.д. В сумме можно так вот слепо проехать мимо даты релиза на недели. Потому всегда чётко выясняйте, какие в проекте будут активности помимо *«основных»*. Самый косяк -- пропустить время подготовки к цепочке задач, включающих в себя блокер, на котором в режиме ожидания будут болтаться другие ветви проекта.

---

Резюме:
* вычленяйте блокеры;
* почти сделано -- не сделано;
* разработчик тестировал -- никто не тестировал;
* код не продукт;
* на выходных работы нет;
* подготовка тоже работа.

Всё это достаточно простые правила, которые можно выполнять механически без знания конкретных людей. Безусловно, на сроки будут влиять личности исполнителей, тут деваться некуда. Но если вы это сами уже поняли и начали применять, присматриваясь и запоминая *«Сергей всегда занижает прогноз»* или *«тут сходятся задачи NN и MM, а они друг друга терпеть не могут»*, методичка не нужна.

Не хворайте.