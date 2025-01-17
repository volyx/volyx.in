---
author: "volyx"
title:  "Shared Objects and Synchronization"
date: "2015-02-01"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Как сказал David Wheeler, все проблемы в Computer Science могут быть решены еще одним уровнем абстракции. Netty как раз предлагает такой уровень абстракции для клиент-серверных приложений, работающих через NIO(non-blocking input-output). Netty упрощает разработку TCP, UDP серверов, но также дает доступ к использованию низкоуровнего API, представляя свои высокоуровневые абстракции."
image: "../img/art_of_multiprocessor_programming.jpg"
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

:icons: font

:sectanchors:

== Shared Objects and Synchronization


----------------------
On the first day of your new job, your boss asks you to find all primes between
1 and 1010 (never mind why), using a parallel machine that supports ten concurrent
threads. This machine is rented by the minute, so the longer your program
takes, the more it costs. You want to make a good impression. What do
you do?
As a first attempt, you might consider giving each thread an equal share of the
input domain. Each thread might check 109 numbers, as shown in Fig. 1.1. This
approach fails, for an elementary, but important reason. Equal ranges of inputs do
not necessarily produce equal amounts of work. Primes do not occur uniformly:
there are many primes between 1 and 109, but hardly any between 9·109 and 1010.
To make matters worse, the computation time per prime is not the same in all
ranges: it usually takes longer to test whether a large number is prime than a

