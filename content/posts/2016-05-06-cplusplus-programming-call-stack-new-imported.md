---
author: "volyx"
title:  "Стек вызовов"
date: "2016-05-06"
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

Задание 

[https://stepic.org/lesson/Стек-вызовов-538/step/10](https://stepic.org/lesson/Стек-вызовов-538/step/10)

Вам требуется написать программу, которая "переворачивает" последовательность положительных целых чисел. На вход подается последовательность разделенных пробелами положительных целых чисел. Последовательность заканчивается нулем. Требуется вывести эту последовательность в обратном порядке. 

На выводе числа нужно так же разделить пробелами. Завершающий ноль — это просто индикатор конца последовательности, он не является ее частью, т.е. выводить его не нужно. 

Требования к реализации: в данном задании запрещено использовать циклы, а также дополнительную память: массивы, строки или контейнеры (даже, если вы с ними уже знакомы). Вам разрешено заводить вспомогательные функции, если они вам нужны. 

Подсказка: используйте рекурсию.

Sample Input:
15 26 1 42 0

Sample Output:
42 1 26 15

Решение

{% highlight cpp %}
#include <iostream>

using namespace std;

void read() 
{
	int c;
	std::cin >> c;
		
	if (c != 0) {
	 	read();
	} else {
		return;
	}
	cout << c << ' ';
}

int main()
{
	read();
	return 0;
} 
{% endhighlight %}