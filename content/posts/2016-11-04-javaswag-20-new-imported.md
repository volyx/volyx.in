---
author: "volyx"
title:  "Javaswag выпуск 20"
date: "2016-11-04"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске тонкости экзекъютор сервисов, сохранение объектов в Редис и способы упаковки приложения в исполняемый архив."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---
В выпуске - пишем UDP сервер, оптимизируем код для JIT с помощью JITWatch и разбираемся как работает ThreadLocalRandom.

[A Guide To UDP In Java](http://www.baeldung.com/udp-in-java)

В статье рассказывается как работать с UDP пакетами в Java. На примере простого UDP сервера и клиента автор рассказывает чем отличаются протоколы TCP от UDP и как это ложится на Java.


[Linked Array Queues, part 1: SPSC](http://psy-lob-saw.blogspot.ru/2016/10/linked-array-queues-part-1-spsc.html)

Нитсан разрабатывает библиотеку [JCTools](http://jctools.github.io/JCTools/) и предлагает реализации очередей, которых по его мнению не хватает в Java. В статье рассматривается несколько типов очередей с примерами реализаций из JCTools. 

[Why it rocks to finally understand Java JIT with JITWatch](http://zeroturnaround.com/rebellabs/why-it-rocks-to-finally-understand-java-jit-with-jitwatch/)

JitWatch - утилита которая показывает, как JIT компилятор работает с вашим кодом. В ней можно найти длинные методы в приложении и посмотреть во что компилируется класс. JITWatch поможет найти “узкие места” в коде и переписать их, чтобы код стал JIT-friendly.


[New Tricks with Dynamic Proxies in Java 8 (part 2)](https://opencredo.com/dynamic-proxies-java-part-2/)

В статье несколько примеров и трюков по использованию прокси-объектов, а также сравнение их производительности. 

[Do you really need instanceof?](https://www.javacodegeeks.com/2016/10/really-need-instanceof.html)

Автор предлагает присмотреться к местам, где в коде используется ‘instanceof’ и попробовать заменить его на паттерн “Визитор”. Станет ли код читабельней или производительней — открытый вопрос. В статье обсуждение и примеры замены.

[Generational disparity in garbage collection](http://mydailyjava.blogspot.ru/2016/10/generational-disparity-in-garbage.html)

Рафаэль — создатель известной библиотеки для работы с байт кодом - [ByteBuddy](http://bytebuddy.net). В статье он рассказывает как инструментировал ForkJoinPool и боролся со сборкой долгоживущих объектов в своей библиотеке.


[HTTP headers forwarding in microservices](https://blog.frankel.ch/http-headers-management-with-spring)

Николас рассказывает о том как можно написать свой “трейсирующий” фреймворк поверх Спринга. Фреймворк добавляет всего три заголовка в запросы к микросервисам. Фреймворк поможет отслеживать работу ваших сервисов и написать кастомный мониторинг для вашего приложения.


[Memory efficient HashSet implementation for Java](https://intelligentjava.wordpress.com/2016/10/22/memory-efficient-hashset-implementation-for-java/)

Автор поставил задачу — написать свой HashSet<String> для hex строк, который будет потреблять меньше памяти чем стандартный из Java. Что в итоге получилось читаем в статье.

[Netty Tutorial Part 1: Introduction to Netty](http://seeallhearall.blogspot.ru/2012/05/netty-tutorial-part-1-introduction-to.html)

Последние три недели плотно работал с библиотекой Netty - реализовывал RPC(Remote Procedure Call). Про RPC на Netty написано не мало, но как всегда нужен свой “узкозаточенный” мини-фреймворк. Это одна из двух частей статей, которые помогли мне вспомнить основные концепции Netty. 

[Java ThreadLocalRandom explained](http://videlalvaro.github.io/2016/10/inside-java-s-threadlocalrandom.html)

Автор разобрается в алгоритмах которые стоят за генерацией случайных чисел в джаве. Титанический труд прочитать все научные работы, стоящие за константами и “магией” в джаве.

Еженедельные выпуски Джавасвэга на почту — [http://javaswag.curated.co](http://javaswag.curated.co).

Еженедельные выпуски Джавасвэга в Телеграме — [http://telegram.me/javaswag](http://telegram.me/javaswag).

Удачи!

![dilbert-agile](/images/dilbert-agile.gif)
[http://dilbert.com/strip/2016-07-30](http://dilbert.com/strip/2016-07-30)