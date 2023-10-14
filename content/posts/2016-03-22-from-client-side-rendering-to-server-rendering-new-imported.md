---
author: "volyx"
title:  "Переходим с клиентской генерации html к серверной"
date: "2016-03-22"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: ""
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Я использую ангуляр, как основной веб-фрейворк для проекта [http://wndlust.ru](http://wndlust.ru). В течение года работы с ним у меня возникли небольшие проблемы. Все они хорошо известны разработчикам хоть как-то знакомым с ангуляром: 

- производительность `ng-repeat`. Когда мы кладем `ng-repeat` в `ng-repeat`, а затем еще в `ng-repeat` - то `scope` будет скопирован ровно столько же раз, все слушатели теперь будут слушать друг друга. Обновление нижнего элемента повлечет за собой N^M обновлений. N - количество элементов в ng-repeat, M - количество ng-repeat'ов
- сложный синтаксис директив
- ng-transclude 
- индексируемость

Любой проект, хоть как-то связанный с контентом должен худо-бедно индексироваться. Хотя скорее всего, индексация не помешают любому сайту.