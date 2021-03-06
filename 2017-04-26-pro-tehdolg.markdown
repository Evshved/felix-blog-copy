---
layout: post
title: "Про техдолг"
date: 2017-04-26 22:23:33 +0300
categories: development
---
Техдолг — это ваше отставание от текущего состояния окружающего мира. Как локального мирка, так и планеты в целом. Разработчики в теории знают, что техдолг надо отдавать. И менеджеры знают. На практике постоянно какой-то адочек. Давайте я попробую пояснить, почему этот адочек опасен и может стоить вам цвета волос и эмали зубов.

---

**Во-первых**, самое банальное — вендоры прекращают поддержку старых версий. Те же LTS у Ubuntu не вечные. Прекращение поддержки чревато *«кто нашёл проблему, тот с ней и разбирается»*. То, что вы N лет проблем не находили, ничего не значит. Найдёте в ночь с субботы на воскресенье, когда оба ведущих разработчика на курорте в оффлайне, а сервис смотрят президенты большой двадцатки. Будет весело.

**Во-вторых**, менее банальное — вы скучны и опасны разработчикам. Скучны потому, что… ну, у контингента характер такой. Старое — оно скучное. Интересно всё новое. А опасны потому, что только самый распоследний junior не осознаёт своё ежедневное отставание от рынка труда. Чем дольше разработчик возится с гвоздями прибитой версией N, тем меньше он интересен рынку. Знаю минимум двоих уволившихся, для которых это было одним из аргументов. В сумме со скукой получаете текучку.

**В-третьих**, проблемы с набором junior’ов. На деле очень мелкие проблемы, но они бывают. Если человек входит в отрасль, он не учится на технологиях прошлого века, но берёт современное. А у вас внезапно прошлый век. И даже если вы уговорите (впрочем, junior’ы покладисты, им кушать очень хочется) Васеньку писать на какой-нибудь Java 1.5, Васенька может ненулевое время перестраиваться с Java 1.8. А потом задумается о том, нафига ему такое счастье, потому смотри «во-вторых».

**В-четвёртых**, обычно техдолг не атомарен. Если что-то одно устаревает, оно тянет за собою другое. Другое тянет третье. И вместо того, чтобы обновлять одну библиотеку, вы будете обновлять двадцать библиотек. Что тоже бывает очень, очень весело. Образно говоря, вы начинаете сменой стояка, а заканчиваете капремонтом квартиры. Если успеваете оценить объём работ… бывает, отказываются от обновления. Устаревание всего накапливается, ну и однажды совсем всё плохо будет — тотальная заморозка продуктовых изменений, вся команда надолго по уши в расчистке древней конюшни.

**В-пятых**, техдолг любит наносить внезапный удар в спину. Вам надо прикрутить библиотеку, а нельзя, минимальная версия фреймворка выше вашей. А надо. Потому срочно всё обновлять. Вам надо использовать метод в API, а его умеет только новый клиент. А надо. Потому срочно всё обновлять. Сюда же стопка лихорадочных security обновлений или ситуации, когда дичайшие баги исправляются только в новых библиотеках, а вам уже сейчас жмёт.

Потом на пустом месте начинаются подвиги, броски на амбразуру, выдирание оставшихся волос и чёрные круги под глазами. Ррромантика!

---

Тут сбоку есть ещё два размышления и наблюдения.

Если у вас растёт техдолг, у вас проблемы с процессом разработки и / или с кодом. Эдакий звоночек тревожный. Процесс не позволяет (или не желает, что тоже бывает) вовремя реагировать на перемены в технологическом стеке. А код не позволяет безопасно обновиться — обычно причиной тому отсутствие внятного покрытия тестами. Эдак обновишься, а оно кааак долбанёт. Грусть и печаль.

Ну и надо понимать, что оголтелое обновление на следующий же день от выхода версии — оно вот тоже зло. Выжидается разумный период накатки патчей, осмысления сообществом, изучением changelog’ов и т.д. Полугодия хватает на это с головой. А уж потом спокойно обновиться.

Такие дела.
