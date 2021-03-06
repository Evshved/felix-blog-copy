---
layout: post
title: "Разработка и бизнес"
date: 2019-06-20 20:30:00 +0300
categories: talk
---
Ща на одном дыхании выдам коротко о том, как разработчики ни фига не понимают в том, чего бизнес хочет, что ему важно, а что совершенно до балды. Я понимаю, слушать меня, только я открою вам глаза, коллеги, ну и правду скажу. Как обычно.

Сначала две вводных, с которыми смириться.

**Во-первых**, вы, ваш менеджер, ваш лид и прочая вертикаль — это не тот бизнес, о котором говорим. Мы говорим про тех, кто даёт деньги тем, кто объясняет вам на вашем языке, что вам надо сделать. Ну и вообще оплачивает банкет и танцы вокруг столов. Инвесторы, банки, владельцы, всё такое. Люди, которые обычно не понимают в разработке, но понимают в деньгах (потому вы разработчик, а при деньгах бизнес).

**Во-вторых**, в человеческом обществе на любое правило и наблюдение находится кто-то, кто стоит на голове, кушая кашу из песка. Потому к тексту ниже стоит относиться не просто вдумчиво и серьёзно, но и с пониманием *«из любого правила про людей есть исключения, не отменяющие правило, но показывающие, что в белом стаде бывают чёрные овечки, а стадо всё равно белое»*.

---

Так вот, бизнес — он про деньги. Точнее, когда на входе X денег, а на выходе Y денег, при этом Y больше X.

Я сейчас рубану очень кирпичными и угловатыми утверждениями, постарайтесь включить что-нибудь, что позволит вам от этих кирпичей добраться до миллиарда примеров реальности этой планеты.

Опишу идеал.

Бизнесу очень интересно:
1. Не потратить на разработку ни копейки.
2. Не потратить на эксплуатацию ни копейки.
3. Не потратить на развитие ни копейки.
4. Вообще не тратить не копейки.
5. Получить продукт за тысячу лет до конкурента, вчера задумавшегося об этом продукте.
6. Получить сегодня миллион прибыли.
7. Получить завтра миллиард прибыли.
8. Получать ежедневно миллиард прибыли следующие тысячу лет.

Конечно, хорошо бы и закон при этом не нарушить. И какую-нибудь мораль. С этим, впрочем, так себе получается, потому регулярно вспыхивают интересные скандалы в области больших дядек (типа *«ой, да неужели такая уважаемая компания покупает железо, источником которого рабские лагеря в Бразилии? что, это дешевле раз в десять, чем выхлоп от свободного человека? ай-ай!»*).

Но так не получается. Потому идеал прислоняется к реальности:
1. Потратить на разработку меньше.
2. Потратить на эксплуатацию меньше.
3. Потратить на развитие меньше.
4. Получать прибыль.

Обратите внимание на ключевую особенность обоих списков: деньги. Везде фигурируют деньги. Бизнесу пофиг, **как** разработка сделает то, что будет приносить прибыль. Бизнесу не пофиг только на разницу между входом и выходом в контрольных точках.

---

Выделю в отдельный блок. Это прям вот огромных масштабов клин в головах разработки.

Ещё раз большими корпулентными буквами: **БИЗНЕС НЕ ИНТЕРЕСУЕТСЯ ТЕМ, КАК ИМЕННО ВЫ СДЕЛАЕТЕ ТО, ЧТО ПРИНЕСЁТ ПРИБЫЛЬ БИЗНЕСУ**. Понимаете?

Безусловно, не все вокруг дураки, потому границы у вас есть и будут. От выбора техностека (рынок труда, оклады специалистов и т.п.) до прямого вмешательства, если бизнес строит узкий нишевой бизнес, который могут строить только специалисты (и владельцы бизнеса таковыми являются). Суть в одном:
* бизнесу пофиг на красоту языка, если решение на нём приносит прибыль;
* бизнесу пофиг на качество кода, если пучок рублёвых джуниоров несёт сервис на руках;
* бизнесу пофиг на прогресс, если столетние решения приносят прибыль, а ваши новые свистелки не приносят её больше;
* бизнесу пофиг на .., если .. прибыль.

Иными словами, фантазии о том, что кому-то там где-то там хоть на секунду интересно, читабельный ли код, понимает ли чёт Васян, греются ли процессоры, жужжат ли диски... ну, пересказывать друг другу, да. Бизнесу пофиг. Я могу ещё сто раз это слово написать: пофиг.

Не пофиг что-либо только тогда, когда прибыль падает. Или не растёт. Вот тогда начинается поиск шаманских практик.

---

Шаманские практики в исполнении бизнеса на массовом рынке разработки выглядят так — как бы сделать так, чтобы **дешёвые** разработчики **дёшево** делали **дешёвый** софт, приносящий прибыль. В каждом блоке это подчёркиваю, подчеркну и в этом: речь ни фига не о том, как что-либо делать красиво, правильно или ещё чего там выдумают программисты. Речь о том, куда, сколько и когда денег.

Скажем, если завтра команда какой-нибудь тайной лаборатории выпустит в релиз автомат, клепающий сайты с дичайшим говнокодом внутри, но делающий то, что надо бизнесу, половина разработчиков мира окажется на улице. Возможно, вам даже грустно улыбнутся, пожмут руку, скажут ободряющие слова и вручат незабудку. Если этот сайт из-за говнокода надо будет раз в час ребутать, на кнопку посадят Senior Button Clicker с двумя дипломами. Он будет нажимать.

А за час до запуска этого автомата в вашей компании на верхнем этаже в светлом кабинете будет такой диалог:  
— Иван Семёнович, Yet Another Super Service Maker 2000 выполняет работу сотни разработчиков!  
— Дайте два!  
— А не десять?  
— Сколько будет стоить?  
— Миллион в месяц.  
— Сколько у нас программистов?  
— Тысяча.  
— Сколько стоят?  
— Десять миллионов в месяц.  
— Автоматы купить, программистов уволить.  
— Но есть нюанс.  
— Какой?  
— Автоматы генерируют адовый говнокод.  
— Кого это волнует?  
— Программистов.  
— А наших пользователей?  
— Нет.  
— Повторяю: автоматы купить, программистов уволить.  

Если считаете, что этого не произойдёт (при условии появления таких автоматов), ну... возможно, Иван Семёнович ваш папа.

---

Так вот. Закруглюсь. Не надо фантазировать на темы вроде *«бизнесу важно, чтобы я не писал говнокод»*. Это неправильная фантазия. Правильная нефантазия звучит так: *«бизнесу важно, чтобы ты писал то, что приносит бизнесу прибыль, а не отнимает её»*. Это две редко стыкующихся системы ценностей, но невероятно часто смешиваемых в сетевых дискуссиях.

В конце концов, если посмотреть на это всё со спутника... Гауди был один. И строил он шедевры. Все эти разговоры о том, как надо ориентироваться кодом на *«чтобы даже джуниор мог понять, чтобы легко было вносить изменения, чтобы вот это самое!»* — они о том, что индустрия клепает хрущёвки тысячами. Блок за блоком. И клепают их ни фига не Гауди. Отсюда и внедряемые в головы обычаи, практики, императивы. Только вот ни фига эти практики не про архитектуру уровня Гауди. Он, был бы разработчиком, каждым своим творением нарушал бы все пункты. Они именно для штамповщиков хрущёвок. То, что бизнесу хорошо — согнать с ближайших базаров армию гастарбайтеров одноразовых, застроить квартал, разогнать, оставив слегка испитых сантехников.

Да, это тоже архитектура. Тоже дома. Только хотя бы в контексте [Гамбургского счёта](https://ru.wikipedia.org/wiki/Гамбургский_счёт) полезнее не подменять линейку Гауди линейкой хрущёвок.

И, если говорите / думаете, что какой-либо код хороший / плохой, хорошо бы ясно представлять систему, внутри какой вы дали оценку. Плох для гастарбайтера (и для бизнеса)? Возможно. Хорошо для Гауди (и архитектуры)? Возможно.
