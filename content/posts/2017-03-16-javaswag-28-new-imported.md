---
author: "volyx"
title:  "Javaswag выпуск 28"
date: "2017-03-16"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске запоминающие функции из Java 9, туториал по эластиксерчу и новый сборщик мусора - Эпсилон."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!
В выпуске запоминающие функции из Java 9, туториал по эластиксерчу и новый сборщик мусора - Эпсилон.

[http://www.baeldung.com/elasticsearch-full-text-search-rest-api](http://www.baeldung.com/elasticsearch-full-text-search-rest-api)

**Simple Full-Text Search with ElasticSearch**

Автор показывает, как с помощью нескольких команд из консоли можно добавить документы в эластиксерч и сразу же начать искать по ним. Простой и понятный туториал об эластиксерче. 

[http://carlmartensen.com/immutability-made-easy-in-java-9](http://carlmartensen.com/immutability-made-easy-in-java-9)

**Java 9’s Immutable Collections Are Easier To Create But Use With Caution**

В Java 9 появятся новые методы Set.of, Map.of, которые упростят создание неизменяемых коллекций. В Java 8  для этого требовалось несколько строк, а теперь одна.

[https://dzone.com/articles/memoizing-functions-with-core-java9](https://dzone.com/articles/memoizing-functions-with-core-java9)

**Memoizing Functions With Core Java 9**

Memoizing Functions или запоминающие результат функции в восьмой джаве приходилось писать самим. В девятой появится метод Memoizer.memoize, который сделает всю работу за разработчика.

[https://youtu.be/88-szpeNfrU](https://youtu.be/88-szpeNfrU)

**Getting C/C++ performance out of Java**

Джон Дэвис в своем докладе советует писать код на джаве как в 80-х, 90-х годах на Си.
Использовать бинарный формат хранения объектов, и как можно меньше памяти.

[http://www.javaspecialists.eu/archive/Issue245.html](http://www.javaspecialists.eu/archive/Issue245.html)

**Surprising += Cast**

Хейнз Кабутс рассказывает о скрытых преобразованиях типов в простых конструкциях.

Чтобы до конца в них разобраться придется заглянуть в спецификацию языка.

[https://mchernyavska.wordpress.com/2017/02/19/interview-questions-verify-the-braces/](https://mchernyavska.wordpress.com/2017/02/19/interview-questions-verify-the-braces/)

**Interview questions: verify the braces**

Часто встречающаяся задача с собеседований — «про скобки». Ее первое решение наверняка известно многим, а вот второе через while и replace гораздо лаконичней и проще.

[https://habrahabr.ru/post/321856/](https://habrahabr.ru/post/321856/)

**Новый GC Epsilon. У джавы может не быть сборки мусора. Шок. Сенсация**

В статье рассказывается о новом сборщике мусора под кодовым именем «Эпсилон». «Эпсилон» хоть и сборщик мусора, но мусор не собирает.  В статье — о том как он это делает.

[https://www.infoq.com/news/2017/02/java-memory-limit-container](https://www.infoq.com/news/2017/02/java-memory-limit-container)

**Java 9 Will Adjust Memory Limits if Running with Docker**

В джава 9 появится опция, которая поможет виртуальной машине понять запущена она в контейнере или нет. Теперь джава сможет управлять выделяемой памятью, зная что она запущена в контейнере.

[https://probablydance.com/2017/02/26/i-wrote-the-fastest-hashtable/](https://probablydance.com/2017/02/26/i-wrote-the-fastest-hashtable/)

**I Wrote The Fastest Hashtable**

Для любителей хардкора и языка Си лонгрид про самую быструю хеш-таблицу по словам автора.
