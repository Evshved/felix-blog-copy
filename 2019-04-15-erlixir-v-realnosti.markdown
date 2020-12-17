---
layout: post
title: "Erlixir в реальности"
date: 2019-04-15 19:00:00 +0300
categories: erlang elixir
---
При изучении новых [для меня] языков стараюсь в процессе подобрать примеры того, что на этих языках в живом боевом продакшене делают характерного, чтобы лучше понять нишу языка и его уместное применение.

Собрал небольшой список такового для [Erlang](https://en.wikipedia.org/wiki/Erlang_(programming_language)) и [Elixir](https://en.wikipedia.org/wiki/Elixir_(programming_language)) в современном мире. Вообще собирал для Elixir, но чёт... сервера-то крутятся на [BEAM](https://blog.stenmans.org/theBeamBook/), вклад Elixir тут не особо велик, как пока понимаю, потому решил включить и Erlang, ну а Elixir проще рассматривать как язык, на котором готовы писать избалованные программисты, не готовые писать на Erlang, но желающие плюшки BEAM (отношения как между Java / Kotlin и JVM).

Критерии выбора:
* большая нагрузка (количественная, качественная) — минус страницы про кота;
* продукт заметное число лет в продакшене — минус стартап студента Васи;
* продукт развивается (определяю через активность компании) — минус однописные сервера, через которые не понять цену поддержки продукта;
* есть хоть какое описание истории, причин, перехода — просто упоминание как-то скучно.

После такого список всё равно пришлось резать, выбирал уже субъективно (скажем, **ejabberd** напрашивается, но слишком очевидный) десять примеров. Получил примерно то же, что везде, но зато со ссылками. Кто хочет прям всё-всё-всё, тем и так собирают: [A collection of companies using Elixir in production](https://elixir-companies.com/ru)

---

**WhatsApp**. Самый известный кейс, он же локомотив Erlang'а вне телекома. Особенно после покупки Facebook'ом за 19 миллиардов фейсбукодолларов. В 2014 году речь шла про [450M пользователей](https://www.fastcompany.com/3026758/inside-erlang-the-rare-programming-language-behind-whatsapps-success), в 2015 году уже [900M пользователей](https://www.wired.com/2015/09/whatsapp-serves-900-million-users-50-engineers/), а в 2018 году и [вот такое](https://www.erlang-solutions.com/blog/20-years-of-open-source-erlang-openerlang-interview-with-anton-lavrik-from-whatsapp.html): *«Today, we have over 1 billion daily active users - just wow!»* Ну и всё это обслуживается очень малым количеством инженеров.

**Discord**. Кто не геймер, может не знать про Discord, геймерам же представлять не надо. Так вот, они на Elixir'е живут. Относительно недавняя статья: [How Discord Scaled Elixir to 5,000,000 Concurrent Users](https://blog.discordapp.com/scaling-elixir-f9b8e1e7c29b?gi=4c4ec086da02)

**Pinterest**. Не очень понятный в 2019 году кейс, т.к. не самые открытые человечеству ребята, но в 2015 году они выложили в open source часть своих разработок на Elixir, заодно написали типичную историю успеха, мол, кода стало меньше, а работать стало круче: [Introducing new open-source tools for the Elixir community](https://medium.com/@Pinterest_Engineering/introducing-new-open-source-tools-for-the-elixir-community-2f7bb0bb7d8c)

**Bleacher Report**. Понятия не имею, кто эти ребята (веб, спорт, мобилы), но в 2017 году они *«1.5 billion page views per month and 250,000 users at its peak»*, что вполне так норм. Изначально были написаны на Ruby on Rails, доросли до 150 серверов и задолбались, после чего перешли на Elixir, ужавшись до 5 серверов (чем по сию пору нагревают рубистов, уверенных, что на их RoR'ушке просто надо было правильно написать): [Benefits of Elixir: How Elixir helped Bleacher Report handle 8x more traffic](https://www.techworld.com/apps-wearables/how-elixir-helped-bleacher-report-handle-8x-more-traffic-3653957/)

**Lonely Planet**. Древность какая, одни из первых аще в интернетах. Так вот, в 2015 году они наняли чуваков после того, как предыдущие чуваки не смогли отчувачить модернизацию бекенда, задыхавшегося (ой, тут снова Ruby on Rails, да шо ж такое) под миллионами ежемесячных юников. Другие чуваки сделали довольно странно (пять микросервисов на разных языках, из них два на Elixir): [Building A Modern, Scalable Backend: Modernizing Monolithic Applications](https://medium.com/@derrickburns/building-a-modern-scalable-backend-modernizing-monolithic-applications-15fc3b8101fa)

**AdRoll**. А это чуваки из области рекламы и аукционов, на Erlang живут давно-давно (уже в 2014 году [рассказывали](https://www.youtube.com/watch?v=qURhXHbxbDU) на конференции про *«ten billion a day»*), нагрузка в 2018 году где-то рядом с *«AdRoll currently participates in well over one million programmatic auctions per second»*: [Quaff that potion: saving $millions with Elixir and Erlang](http://tech.adroll.com/blog/dev/2018/01/08/quaff-that-potion-saving-millions-with-elixir-and-erlang.html)

**Toyota**. Не про нагрузку, пожалуй (хотя вот фиг знает), но про развитие продукта целиком на базе Elixir, что тоже интересно: [Elixir powers first Car Share Service from Toyota](https://codesync.global/media/elixir-powers-first-car-share-service-from-toyota/)

**PagerDuty**. А эта история, видимо, как про нагрузку (если верить рекламному *«analyzing billions of signals across virtually any data source»*), так и про продукт. Как я понял, автоматизация с интеграцией всего со всем в корпорациях (ну, клиенты у них мощные, надо сказать). Прям по шаблону. Сначала быстро наваяли на Ruby on Rails. Упёрлись. Пометались, подумали, в 2018 году почти всё уже жило на Elixir, счастье-счастье: [Elixir at PagerDuty](https://www.pagerduty.com/blog/elixir-at-pagerduty/)

**Shedul**. Чуваки делают решение для салонов красоты (ну типа того). Занятный кейс без диких нагрузок (но «*several millions of bookings are being made through Shedul each month from as many as 120 countries»*), в категории чего-то промежуточного и с разбором мотивации ухода с Ruby on Rails в Elixir: [Choosing Elixir for Shedul’s tomorrow](https://medium.com/fresha-engineering/choosing-elixir-for-sheduls-tomorrow-3debbe485d77)

**Остальные**. Не смог найти удовлетворяющий меня кейс, приведу примером того, что было бы интересным (но чуваки не рассказывают). Есть достаточно известные [cars.com](https://www.cars.com) и [bikebandit.com](https://www.bikebandit.com). У них огромная нагрузка. У них неплохой бизнес. У них есть бекенды на Erlixir.

---

А и всё. Компаний, конечно, намного больше, но с поиском кейсов проблемы:
* много кейсов вокруг телекома, там всё слишком очевидно и понятно;
* много кейсов вокруг ядра бизнеса, но не в самом ядре — так-то пофиг, что у кого-то на окраине инфраструктуры какая-то мелочь на Erlixir чёт делает;
* много кейсов из одного лишь упоминания без деталей — чуваки вроде Goldman Sachs не очень любят публичность в таких темах;
* немало кейсов просто не упомянуты — в компании вакансии есть, а и всё, что про Erlixir в XYZ известно наружу.

В общем и целом понятно, куда это всё и зачем.

PS. Тем, кому трудно: Erlixir = Erlang or / and Elixir.
