---
author: "volyx"
title:  "Веб-компоненты"
date: "2015-08-26"
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

:icons: font

:sectanchors:

== Веб-компоненты

Непонятно как затесавшийся доклад про веб-компоненты на JEEConf
- Less JS! Web components for back-end developers. (Olga Semeniuk, Belarus)

++++
<iframe width="854" height="480" src="https://www.youtube.com/embed/aoCzBIGtUj0" frameborder="0" allowfullscreen></iframe>
++++

Очень понравилась такая очевидная вещь:

++++
<blockquote class="twitter-tweet" lang="ru"><p lang="ru" dir="ltr">Не нужно писать собственные компоненты на JSF, PrimaFaces при миграции на новую версию они обязательно сломаются!</p>&mdash; Дима Волыхин (@volyihin) <a href="https://twitter.com/volyihin/status/634350154661937152">20 августа 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
++++

Веб-компоненты состоят из следующих частей:

1. **Templates**. Фрагменты HTML, которые программист собирается использовать в будущем. Содержимое тегов *<template>* парсится браузером, но не вызывает выполнение скриптов и загрузку дополнительных ресурсов (изображений, аудио…) пока мы не вставим его в документ.
2. **Shadow DOM**. Shadow DOM позволяет изменять внутреннее представление HTML элементов, оставляя внешнее представление неизменным. Отличный пример — элементы *<audio>* и <video>*. В коде мы размещаем один тег, а браузер отображает несколько элементов (слайдеры, кнопки, окно проигрывателя). В Chrome эти и некоторые другие элементы используют Shadow DOM.
3. **Custom Elements**. Позволяют создавать и определять API собственных HTML элементов. В HTML теперь будут такие теги как <menu>* или <user-info>*?
4. **Imports**. Импорт необходимых ресурсов для компонента - css например.

Хороший пример реализации компонентов это Polymer.

Пример объявления полимеровского элемента:
[source,html]
----
<dom-module id="element-name">

  <style>
    /* Импортируем css стили.*/
  </style>
  
  <template>
    <!--Шаблон элмента -->

    <div>{{greeting}}</div> <!-- динамические данные компонента-->
  </template>

  <script>
    //регистрируем элемент
    Polymer({
      is: "element-name",

      // переменные элемента 

      properties: {
        // публичные переменные, которые мы определяем снаружи
        greeting: {
          type: String,
          value: "Hello!"
        }
      }
    });
  </script>

</dom-module>
----

У полимера также есть библиотека уже готовых ((https://elements.polymer-project.org/ компонент)). 

image::../../img/polymer-cc.png[]

((https://elements.polymer-project.org/elements/gold-cc-input Компонент)) для ввода номера кредитной карты, естественно в материальном дизайне, куда без него.
 
Полимеровские компоненты очень похожи на ангуряровские директивы. 
В итоге синтаксис одинаковый, то есть сходу то и не отличить, что это полимер или ангуляр?

== ((https://www.polymer-project.org/1.0/ Polymer))

[source,html]
----
  <gold-email-input auto-validate value="batman@gotham.org"></gold-email-input>
----

== ((https://angular.io/ Ангуляр 2))
Обещает нам подобный синтаксис


image::../../img/angular2.png[]

Невооруженным взглядом видно, что они одинаковы.

== Какой же в итоге выберет гугл?

Сопутствующие статьи:
- ((http://habrahabr.ru/post/210058/ Составляющие веб-компонентов))
- ((https://github.com/GoogleWebComponents пример веб-компонентов от гугла))
- ((https://elements.polymer-project.org/ полимеровские компоненты))