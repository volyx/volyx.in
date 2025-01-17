---
author: "volyx"
title:  "Обзор книги Java Concurrency in Practice"
date: "2015-01-12"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "by Brian Goetz, Tim Peierls, Joshua Bloch, Joseph Bowbeer, David Holmes, Doug Lea. I was fortunate indeed to have worked with a fantastic team on the design and implementation of the concurrency features added to the Java platform in Java 5.0 and Java 6. Now this same team provides the best explanation yet of these new features, and of concurrency in general. Concurrency is no longer a subject for advanced users only. Every Java developer should read this book. --Martin Buchholz"
image: "../img/concurrency_in_practice.jpg"
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---


После предисловия (Глава 1), книга разделена на четыре части:

* Основы. Первая часть (Глава 2-5) сфокусирована на основные концепции многопоточности и потокобезопасности, а так же на том, как из многопоточных блоков ,представленных библиотеками классов Java, составлять свои потокобезопасные классы. Так же в первой части вы найдете шпаргалку, суммирующую самые важные правила, приведенные в первой части.

* Главы 2 и 3 (Потокобезопасность _Thread Safety_ ,Обмен объектами _Sharing Objects_) составляют основу этой книги. Так же в них находятся все правила, которые позволяют избежать многопоточных опасностей, учат правильно создавать потокобезопасные классы, и проверяют на потокобезопасность. У читателей, которые предпочитают теории практику, может появиться соблазн пропустить Часть 2, но не забудьте вернуться к Главам 2-3 перед тем, как начать писать многопоточный код.

* Глава 4 рассказывает о том, как составлять из отдельных потокобезопасных классов более большие потокобезопасные конструкции.

* Глава 5 рассказывает о многопоточных реализациях коллекций и синхранизаторов, поставляемых самой Java. 

* Часть 2 посвящена структурированию многопоточных приложений. Рассказыват, как используя потоки увеличить пропускную способность и "отзывчивость" многопоточных приложений.

-------------------------------
Chapter 4 (Composing Objects) covers techniques for composing threadͲsafe classes into larger threadͲsafe classes.

Chapter 5 (Building Blocks) covers the concurrent building blocksͲthreadͲsafe collections and synchronizersͲprovided
by the platform libraries.
Structuring Concurrent Applications. Part II (Chapters 6Ͳ9) describes how to exploit threads to improve the throughput or responsiveness of concurrent applications. Chapter 6 (Task Execution) covers identifying parallelizable tasks and
executing them within the taskͲexecution framework. Chapter 7 (Cancellation and Shutdown) deals with techniques for
convincing tasks and threads to terminate before they would normally do so; how programs deal with cancellation and
shutdown is often one of the factors that separate truly robust concurrent applications from those that merely work.
Chapter 8 (Applying Thread Pools) addresses some of the more advanced features of the taskͲexecution framework.
Chapter 9 (GUI Applications) focuses on techniques for improving responsiveness in singleͲthreaded subsystems.
Liveness, Performance, and Testing. Part III (Chapters 10Ͳ12) concerns itself with ensuring that concurrent programs
actually do what you want them to do and do so with acceptable performance. Chapter 10 (Avoiding Liveness Hazards)
describes how to avoid liveness failures that can prevent programs from making forward progress. Chapter 11
(Performance and Scalability) covers techniques for improving the performance and scalability of concurrent code.
Chapter 12 (Testing Concurrent Programs) covers techniques for testing concurrent code for both correctness and
performance.
Advanced Topics. Part IV (Chapters 13Ͳ16) covers topics that are likely to be of interest only to experienced developers:
explicit locks, atomic variables, nonͲblocking algorithms, and developing custom synchronizers.
Co


