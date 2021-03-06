---
layout: post
title: "Таки что должен разработчик"
date: 2018-06-12 20:10:42 +0300
categories: talk
---
Порою бывают разговоры с разными разработчиками, которые (разговоры) после суммы за N..M времени дают интересную картину. Прочтите список ниже. Уверен, хоть с парой пунктов, но сталкивались. А часть одобряете.

---

Разработчик не должен ставить себе задачи. Этим занимаются лиды и менеджеры.

Разработчик не должен проверять свою работу. Этим должны заниматься тестировщики.

Разработчик не должен хотя бы думать про эксплуатацию. Этим должны заниматься админы.

Разработчик не должен делать архитектуру. Этим должны заниматься архитекторы и лиды.

Разработчик не должен учиться. Его должен обучать работодатель.

Разработчик не должен думать про юзеров. Этим должен заниматься саппорт.

Разработчик не должен разбираться в базах. Этим должен заниматься специальный DBA.

Разработчик не должен разбираться в железе. Этим должен заниматься хелпдеск или железячник.

Разработчик не должен заниматься продуктом. Этим должен заниматься product owner.

Разработчик не должен в удобство. Этим должен заниматься UX-боец.

И ещё куча всего. Бекендеры не должны даже админку на бутстрапе. Фронтендеры не должны даже Node.js на Ubuntu поставить. Джависты не должны в JVM, а питонисты в PVM, так сказать. Скучной тикетной бюрократией тоже менеджеры. А планы оставим лидам и... да, менеджерам. Про прибыль пусть голова у бизнеса болит.

---

Тут... сложно с оценкой. Формулировать не хочу, попробовал, получил даже наброском две страницы. Предлагаю умственное упражнение. Найдите ответы на вопрос *"в какого рода бизнесах и в каких задачах такие разработчики применимы?"* Из "таких" при этом исключим редких узких специалистов, которые ничего больше не знают, но могут по названию функции сказать файл и номер строки в исходнике JVM. Их очень мало, живут справа на крае распределения.

Напомню некоторые важные элементы производства софта, чтобы вам было удобнее.

**Экономика**. Грубо говоря, количество денег на старте. Влияет на то, как долго вы можете что-либо делать до момента, когда что-то начнёт приносить прибыль, достаточную, чтобы покрывать текущие расходы. Например, у вас 1М рублей и разработчик Иванов за 100К рублей. Соответственно, уже через 10 месяцев на рынке должен быть МойСуперПродукт с остатком в 100К рублей (вам ведь всё ещё платить Иванову) после выплат за хостинг, рекламу, налоги и т.д. Если Ивановых два, у вас 5 месяцев, а продукт должен выдавать 200К. Если для надзора за этой парой вам нужен Сидоров за 200К, вам хана — бюджета на  два с половиной месяца, затем пополнение списка *"миллион закрытых стартапов"*. Примитивно, но наглядно.

**Продукт**. Разработка ради разработки не нужна вне стен квартиры. Программист программой решает задачу / проблему. Цельная совокупность решений составляет продукт. Целью разработки является выход продукта на рынок / в науку / в народные массы. Пока продукта нет, все работают в минус и на перспективу (ща мы наберём компетенцию на семи граблях и каааак ух!).

**Качество**. Иванов, не умеющий в эксплуатацию, склонен делать сервисы, падающие под слабой нагрузкой. Петров, не умеющий в базы, поставит базу колом своим селектзвёздочка на месячном логе. Мало того, что вы можете так нарваться уже на репутационные риски, так впереди могут оказаться претензии от клиентов. А, да, ещё Иванов и Сидоров будут месяц чинить. Посмотрите на *Экономику* — это минус 200К от вашего начального бюджета.

**Форсмажоры**. У вас два разработчика и один лид. Лида сбивает автобус. Что дальше? У вас бекендер и фронтендер, фронта сбивает автобус. Что дальше? У разработчиков всё хорошо, но автобус добрался до вас. Что дальше? Bus factor в прямом виде редко бывает, но в вариантах постоянно: болезни, семья, государство (смешные кейсы, когда руководителя проекта с Болотной в автозаке на весь день), усталость (мужики, не могу больше, ухожу в отпуск на месяц), бабло (мужики, за углом на 10К больше, пока-пока) и т.п. Ваш бизнес остановится или нет? А почему?

---

Как-то так. Клеймить и размахивать шашкой не буду. Можете посмотреть вакансии и резюме. Посмотреть оклады (почему Иванов 100К, а Петров 200К). Прикинуть, с какой командой и какой стартап хотя бы в теории может выжить в период разработки. Всё просто считается. Ну а потом ещё раз перечитать список и прикинуть, что такое хорошо, что такое плохо.
