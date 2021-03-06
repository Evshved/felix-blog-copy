---
layout: post
title: "Лучшие ошибки софта II"
date: 2015-10-07 17:50:12 +0300
categories: best_fails
---
Mars Climate Orbiter, 1998 год — отличная иллюстрация того, чем заканчивается разобщённость команд разработки. [Железка](https://en.wikipedia.org/wiki/Mars_Climate_Orbiter) должна была подкрасться к Марсу, выйти на орбиту и оттуда следить за интересным. Так и произошло бы, не используй разработчики двигателя метрическую систему СИ, а разработчики софта британскую метрическую систему. Состыковаться не получилось на $327M — спутник распался в атмосфере, промахнувшись на разницу между ньютонами и фунт-силами.

---

В 2005 году крупнейший британский продуктовый ритейлер J Sainsbury PLC потерял $526M. История покрыта мраком, удаётся найти лишь хвостики произошедшего. Выкатили систему автоматизации полезной логистики, упрощающей поступление товаров со склада на полки магазинов. Вместо автоматизации получилась блокировка, ничто никуда не поступало. Ритейлер срочно нанял ~3000 «клерков», которые вручную обеспечивали хоть какое движение, но уже было поздно. Суммарный ущерб от плохой разработки, простоя сети, дополнительного найма и прочих убытков влетел в сотни миллионов.

---

15 января 1990 года ~60К пользователей AT&T не смогли никуда позвонить. И не могли ещё девять часов. Всё это время 114 свитчей компании хороводили reboot, успев заблокировать [~50M звонков](http://users.csc.calpoly.edu/~jdalbey/SWE/Papers/att_collapse.html) и лишить AT&T около $60M прибыли. Ущерб второго порядка (у пользователей) составил и того больше. А всё потому, что за месяц до катастрофы программисты обновили софт на свитчах, попутно влепив одну строчку с ровно одной багой. Выстрелило через месяц. Казалось бы, всё очень, очень хорошо тестировали.

---

Осенью 2003 года госпиталь St. Mary’s Mercy в Мичигане [убил](http://www.baselinemag.com/c/a/Projects-Networks-and-Storage/Hospital-Revives-Its-QTEDeadQTE-Patients) около 8500 человек. Хорошо, что «на бумаге», а не натуральным образом. И снова последствия миграции. Был старый софт. Перешли на новый софт. В процессе переноса данных вместо кода «01» (правильный) влепили «20» (неправильный), что привело к виртуальному геноциду. Было бы смешно, если бы не массовая же рассылка уведомлений о смерти в страховые компании, блокировка выплат и т.п.

---

Должен был быть первым в списке, но я начал с финансовых потерь, а тут планета на кону. 26 сентября 1983 года [Станислав Петров](https://ru.wikipedia.org/wiki/Петров,_Станислав_Евграфович) спас нас всех. Я тогда уже был, потому мог краем глаза увидеть грибки ядерных взрывов, если бы Петров (в тот момент дежурный командного пункта Серпухов-15) поверил [ложному срабатыванию](https://ru.wikipedia.org/wiki/Ложное_срабатывание_системы_предупреждения_о_ракетном_нападении_%281983%29) космической системы раннего предупреждения и дал ход последовательности, завершающейся World War III. Не поверил и не дал. Спасибо. Не спасибо тем, кто не учёл, что датчики спутника могут настолько засвечиваться солнечным светом, отражённым от высотных облаков. Не думаю, что проблема железная (исправили сверкой данных с других спутников, как понимаю), потому с натяжкой в софт.
