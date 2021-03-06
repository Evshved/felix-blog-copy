---
layout: post
title: "Книги: Why Rust?"
date: 2015-11-05 21:16:53 +0300
categories: books
---
• Jim Blandy. *Why Rust? Trustworthy, Concurrent Systems Programming.* O’Reilly, 2015.

И снова книжка-минутка на вечер. Годная традиция у O’Reilly появилась — выпускать 50..70-страничные штуковины по небольшим темам.

По Rust мало печатных материалов. Да вообще нет, строго говоря. Есть лишь Packt’овая перепечатка ранней документации к первому релизу языка, а те же O’Reilly обещают первый учебник только в августе 2016 года. Потому радуемся и минутке.

Автор из Mozilla, близок к теме. С примерами кода объясняет, почему был придуман Rust и в чём его основные отличия (не считая забавного синтаксиса, конечно) от C / C++. Ничего нового, если читали новости и [rust-lang.org](http://rust-lang.org), но детальнее на ~50-ти страницах:
1. Бодрая безопасность типов с тотальной проверкой всего в compile time.
2. Безопасность работы с памятью: нет NP dereference, нет доступа к уже освобождённой памяти, нет buffer overrun.
3. Няшная многопоточность.

Всем, кому интересны новые языки мейнстрима, стоит почитать.

PS. С другой стороны, этого Rust’а в production’ах пока на копейку (если не считать ~100К LOC в Mozilla; update: упс, ещё есть даже [Redox: A Rust Operating System](https://github.com/redox-os/redox)), а нужных библиотек то нет, то они меняются раз в неделю. Сейчас у языка этап стабилизации и допиливания, потому смотреть-то на него стоит, а вот взросло использовать ещё рановато.
