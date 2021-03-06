---
layout: post
title: "Низкий КПД IV"
date: 2017-01-30 12:38:28 +0300
categories: low_ece development
---
Продолжим.

---

**Наследие.** Оно же legacy. Если у меня что и вызывает прям вот искреннюю ненависть, так это ржавые наслоения древнего кода. А его надо тащить в светлое будущее, ибо это дешевле, чем переписывание заново, ну и люди пользуются, чё. Зачастую и люди не прочь съехать с какого-нибудь старого поделия / интерфейса, но у них тоже наследие, тоже пользователи и т.д. Круговая порука.

Что действительно толкового может выстроить строитель, которому 1) нельзя снести гнилой сарай, 2) нельзя увеличить здание до трёх этажей, 3) нельзя использовать бетон, 4) балки брать строго определённой марки (завод давно помер, но), 5) ничего шумного нельзя, ведь в доме живут жильцы.

Да любая задача добавления / исправления чего-либо в старом (а он уже спустя 2 года сейчас может считаться старым) софте превращается в военную операцию по спасению рядового Пупкина. Какой нафиг КПД у подобной деятельности и у результата? Все сроки и усилия умножаешь на K (K > 2), при этом всё равно на выходе получаешь караван со скоростью самого медленного верблюда.

---

**Отсутствие идентификации.** Тут смешная штука. Начну с того, что программисты сами не очень могут договориться о том, что такое программирование и кто такой программист. Есть овердофига трактовок топовых и есть триллиард трактовок индивидуальных. Соответственно, есть некоторая проблема с тем, какие задачи программисту давать, а какие не давать. Мем *«тыжепрограммист[, потому ща быстро заведёшь Боинг, поставишь кластер серверов и вылечишь желтуху у алкоголика Васи]»* — он не только у бабушек-соседок, отдающих утюг на починку, но и в головах многих руководителей. Потому программисты занимаются всем с разной степенью успешности. Степень нередко фиговая, тут КПД и абздольц.

Дальше проблемы с требуемым объёмом знаний и умений. В «реальном» мире есть обязательная экзаменация, есть подтверждение уровня, есть квалификационные тесты и т.п. У программистов такого нет. Без единой бумажки можешь собеседоваться на разработчика по технологиям A, B и C, ну и через 1..6 часов попасть на место. При этом часть часов будут спрашивать про X, Y и Z (так принято). И всё равно будет угадайка. Можно нанять чувака, которого хочется уволить через неделю. Можно не нанять чувака, который… например, Google отказался от автора Homebrew (скажем так, его использует половина от всех), от чего интернетики знатно [забурлили](https://news.ycombinator.com/item?id=9695102), потешаясь над современным HR-процессом.

Чё в итоге? В итоге вы тратите мегатонну времени на поиск и собеседование людей. Потом мегатонну времени на то, чтобы понять, что получилось-то. Потом мегатонну на обучение. И всё равно часто не можете понять, что *действительно* можно давать в работу, т.к. боец зачастую раскрывается очень неожиданно.

Заставлять всех пройти сертификации? Не получится. Это дорого. Это быстро устаревает. По фундаментальным и важным штукам сертификаций нет (кроме корочки о высшем образовании, но она нынче ничего не гарантирует).

И вот какой КПД у всего этого?

---

Резюмирую. Если собрать всё воедино, то IT/CS индустрия в худшем своём варианте представляет собою множество случайных людей случайной квалификации, пытающихся на кое-как построенных процессах быстрее сделать (во время, свободное от посторонней фигни) глючные продукты, которые потом будут отжирать половину стоек в ДЦ (или половину вашего смартфона), а спустя год-другой превратятся в кандалы на ногах прогресса.

Но это нормально.

---

*Finished.*
