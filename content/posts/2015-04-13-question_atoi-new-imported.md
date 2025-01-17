---
author: "volyx"
title:  "Задача ATOI"
date: "2015-04-13"
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

== Задача ATOI

----
Write a function to convert a string into an integer. (This function is called A to I (or atoi()) because we are converting an ASCII string into an integer.) Good answer: Go through the string from beginning to end. If the first character is a negative sign, remember this fact. Keep a running total, which starts at 0. Each time you reach a new digit, multiply the total by 10 and add the new digit. When you reach the end, return the current total, or, if there was a negative sign, the inverse of the number. Okay answer: Another approach is to go through the string from end to beginning, again keeping a running total. Also, remember a number x representing which digit you are currently on; x is initially 1. For each character, add the current digit times x to the running total, and multiply x by 10. When you reach the beginning, return the current total, or, if there was a negative sign, the inverse of the number. Note: The interviewer is likely to ask you about the limitations of your approach. You should mention that it only works if the string consists of an optional negative sign followed by digits. Also, mention that if the number is too big, the result will be incorrect due to overflow.