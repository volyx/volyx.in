---
author: "volyx"
title:  "Javaswag выпуск 23"
date: "2016-12-02"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Привет! В выпуске усатый движок шаблонов, серверный рендеринг и миллиарды реквестов за 120$."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!
В выпуске усатый движок шаблонов, серверный рендеринг и миллиарды реквестов за 120$.

[http://www.javamagazine.mozaicreader.com/NovDec2016/Default/25/](http://www.javamagazine.mozaicreader.com/NovDec2016/Default/25/)

**Java Magazine - JUnit 5 Arrives!**

Свежий выпуск журнала Java Magazine. В первой части про изменения в Junit 5. Это самые большие обновления фреймворка с момента его выпуска. Во второй — обсуждение того, как выглядят дизайн паттерны с синтаксисом Java 8. 

[https://patrickgrimard.io/2016/11/24/server-side-rendering-with-spring-boot-and-react/](https://patrickgrimard.io/2016/11/24/server-side-rendering-with-spring-boot-and-react/)

**Server side rendering with spring boot and react**

Фреймворк Реакт уже победил всех на фронтенде и стремительно врываются в Java мир с рендерингом на сервере. Серверный рендеринг это когда джаваскрипт приложение рендерится в ХТМЛ на сервере и на клиент доставляется уже готовая ХТМЛ страница. JSP, JSF, Thymeleaf похоже уже устарели, давайте поспевать за динамичным фронтендом.  

[http://blog.joda.org/2015/12/explicit-receiver-parameters.html](http://blog.joda.org/2015/12/explicit-receiver-parameters.html)

**Explicit receiver parameters**
Коллега прислал в чатик вопрос: скомпилируется ли такой метод `public int compareTo(Currency this, Currency other) { ... }` ? Я ответил нет. Ведь очевидно же, что this ключевое слово и компилироваться метод с таким названием параметра не должен. Я ошибся. Метод скомпилировался. А перестал он компилироваться, когда я поменял параметры местами. Удивлены? В статье о незамеченной фиче джавы — Explicit receiver parameters.

[https://spring.io/blog/2016/11/21/the-joy-of-mustache-server-side-templates-for-the-jvm](https://spring.io/blog/2016/11/21/the-joy-of-mustache-server-side-templates-for-the-jvm)

**The Joy of Mustache: Server Side Templates for the JVM**

В статье рассказывается о движке шаблонов Мусташ, что переводится как "Усы". Действительно, если посмотреть под углом на фигурные скобки {},можно разглядеть перевернутые усы. Усатые шаблоны просты, документация практически не нужна. Если в Таймлифе без документации и строчки не написать, то мусташ до безобразия понятен. Достойная замена JSP для нового проекта.

[https://dzone.com/articles/the-internal-cache-of-integers](https://dzone.com/articles/the-internal-cache-of-integers)

**The Internal Cache of Integers**

Знали что выражение  Integer.valueOf(17) == Integer.valueOf(17) вернет true, а Integer.valueOf(200) != Integer.valueOf(200) вернет false?

Дело в том, что виртуальная машина хранит кэш целых чисел от -128 до 127 включительно. В статье рассказывается как можно увеличить этот кэш, а также его внутреннее устройство.

[https://engineering.linkedin.com/blog/2016/11/application-pauses-when-running-jvm-inside-linux-control-groups](https://engineering.linkedin.com/blog/2016/11/application-pauses-when-running-jvm-inside-linux-control-groups)

**Application Pauses When Running JVM Inside Linux Control Groups**

В Линкадине используют самописные контейнеры и свое приватное облако  LPS. Если вы хотите понять как джава взаимодействует с cgroups добро пожаловать в статью. К сожалению даже блог Линкадина заблокирован, так что лучше заходить через VPN.

[https://habrahabr.ru/post/316370/](https://habrahabr.ru/post/316370/)

**12 млрд реквестов в месяц за 120$ на java**

Всем кто начинает стартап проект обязательно прочтению. Возможно после вы задумаетесь о том нужна ли вам база данных и сколько вы тратите денег на архитектуру. Статья из серии Minimalist architecture - как минимальным количеством денег сделать надежную архитектуру.
