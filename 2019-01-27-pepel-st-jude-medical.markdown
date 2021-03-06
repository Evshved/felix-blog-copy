---
layout: post
title: "Пепел St. Jude Medical в наших сердцах"
date: 2019-01-27 12:32:48 +0300
categories: talk
---
[St. Jude Medical](https://en.wikipedia.org/wiki/St._Jude_Medical) — большая такая компания, до 2017 года самостоятельно производившая медицинское оборудование с продажами по всей планете. Основана в США в 1976 году, с 2010 года входила в Fortune 500. Что могло пойти не так?

---

Современный кардиостимулятор — штука, которая имплантируется в человека, по пути предоставляя возможность дистанционной настройки, диагностики, сбора статистики и т.п. Такие и выпускала компания. Такие и были имплантированы в несколько сотен тысяч человек. Уже всё понятно, да?

В 2016 году MedSec и Muddy Waters Research выпускают отчёт, в котором устройства SJM обвиняются в наличии множества дыр безопасности. Если кратко, суть в следующем: злоумышленный человек может подключиться к импланту и сделать кирдык.

Несколько осложняло ситуацию то, что... Речь шла про 350K..500K+ кардиостимуляторов 4..6 моделей — это много (числа в разных источниках плавают, потому воспринимайте как указание порядка, а не как абсолютные данные). Исследователи были финансово [заинтересованы](https://medicalconnectivity.com/2016/09/02/muddy-waters-alleges-st-judes-devices-vulnerable-cyberattack/) и не скрывали этого, что вызвало [волну](https://threatpost.com/researchers-medsec-muddy-waters-set-bad-precedent-with-st-jude-medical-short/120266/) неприятных вопросов про этику. Отчёт был опубликован в обход обычной практики (сначала тихо связываются с производителями), т.к. у исследователей было опасение, что информацию заметут под ковёр и ничего исправлять не будут.

Реакция St. Jude Medical проста и обычна для корпораций: вывсёврёти. Более того, дяди обидчиво [подали](https://threatpost.com/st-jude-alleges-false-claims-stock-manipulation-in-suit-against-med-sec-muddy-waters/120399/) в суд, мол, что за поклёпы, что за наветы, мы же такие хорошие. Тем не менее, пользователи заволновались, зашла речь о возврате устройств, акции пошли вниз. Исследователи [решили](https://medsec.com/entries/stj-lawsuit-response.html) не сдаваться, юристы сторон начали битву. Маслица подлило ещё и то, что в исследовании появилась и четвёртая сторона (Bishop Fox), нанявшая безопасников для изучения проблемы. Те подтвердили критику, пересказ от лица одно из экспертов вполне [читаем](https://blog.cryptographyengineering.com/2018/02/17/a-few-notes-on-medsec-and-st-jude-medical/amp/).

Не угадать, чем бы всё закончилось, но на происходящее обратило внимание [Food and Drug Administration](https://en.wikipedia.org/wiki/Food_and_Drug_Administration). Очень интересно читать [warning letter](https://www.fda.gov/ICECI/EnforcementActions/WarningLetters/2017/ucm552687.htm) за 12 апреля 2017 года, поглядывая на упоминаемые даты, а также на остальные замечания к производству. Как итог, компания признала проблемы, были налиты патчи, ну и ладушки, все живут мирно.

---

В целом история достаточно обычная и скучная, хоть и вызвала эдак на год возбуждённое оживление в кругах (особенно тех, внутри тела которых эти устройства находились). Пища для размышлений появляется после следующих вопросов...

**Во-первых**, как старая и опытная фирма произвела такое оборудование? Какие внутренние стандарты такое пропустили, как вообще производилось тестирование? О, у нас тут имплант с проводами к сердцу наружу портами торчит... ай, ну и ладно.

**Во-вторых**, какие государственные и  рыночные стандарты и сертификации пропустили такое оборудование на рынок? И ладно бы в Нигерии, но речь-то про США.

**В-третьих**, есть ли вообще повторные аудиты оборудования после того, как оно вышло на рынок? Годы идут, безопасники и хакеры учатся новому, а только спустя годы озвучиваются дыры, которые находятся не производителем и не государством. Ищутся ли вообще?

**В-четвёртых**, вызывает вопросы и растянутость цикла обнаружения, подтверждения и закрытия дыр. Если предположить, что злые хакеры (ну вот китайцы купили железку и отправили в один из миллиарда НИИ Ха Кин Га) обнаруживают дыру через месяц от выхода устройства на рынок. И... Проходит три года волокиты, пока дыра закроется. Всё это время устройство под угрозой. Сиди дома и гадай, не ставят ли в 15 метрах от тебя за забором должным образом настроенный Merlin@Home какой-нибудь.

---

Потому... как бы сказать... надо осторожнее приводить в пример медицинский софт как нечто качественное, проходящее многослойную сертификацию и всё такое. Даже в этой отрасли творится бардак (масштабы которого не узнать). От говнокодеров хоть как защищают не сертификации (как видите, они вполне преодолимы), мне кажется, но только лишь нежелание производителя пересчитывать трупы в случае чего.

PS. St. Jude Medical в 2017 году поглощена Abbott Laboratories, потому с того момента в СМИ оливье — кардиостимуляторы то SJM, то AL, то SJM (AL), то AL (SJM). Я решил оставить для рассказа SJM, т.к. не особо влияет.
