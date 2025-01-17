---
author: "volyx"
title:  "Класс - обёртка"
date: "2014-11-05"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Напарник метода-оберки по оборачиванию, но на уровень выше - это класс - обертка. Он использует примерно такой же подход. Если нам требуется добавить новое поведение в систему, мы  можем добавить его в существующий метод, но также мы можем добавить его к чему-нибудь еще. К тому, кого тоже использует этот метод. Это что-нибудь другое и есть наш класс-обертка."
image: "../img/wrap_class.jpg"
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Давайте опять вернемся к нашему классу `Employee`
[source,java]
----
class Employee {
    public void pay() {
        Money amount = new Money();
        for (Iterator it = timecards.iterator(); it.hasNext(); ) {
            Timecard card = (Timecard)it.next();
            if (payPeriod.contains(date)) {
                amount.add(card.getHours() * payRate);
            }
		}
        payDispatcher.pay(this, date, amount);
    }
... 
}
----
Допустим мы хотим логировать тот факт, что мы платим какому-то определенному, особенному работнику. Первое, что мы можем сделать - это создать например, класс, который тоже будет иметь метод `pay()` и вызвать его. Экземпляр этого классу будет принадлежать `Employee`, и выполнять работу по логированию в своем методе `pay()`, а затем делегировать работнику, так что бы он совершил оплату. Обычно, самый простой способ сделать это, если вы не можете создать объект при тестировании, это выделить интерфейс от класса и реализовать его.

В следующем примере `LoggingEmployee` наследует `Employee` и таким образом после логирования мы можем выполнить метод оплаты от экземпляра `Employee`.
[source,java]
----
class LoggingEmployee extends Employee {
    public LoggingEmployee(Employee e) {
        employee = e;
	}
    public void pay() {
        logPayment();
        employee.pay();
    }
    private void logPayment() {
        ...
	}
... 
}
----
Эта техника называется - `Декоратор паттерн`. Мы создали объекты класс, которые "оборачивают" исходные объекты и позволяют добавить какое-то новое поведение. Класс-обертка должен иметь такой же интерфейс, что и исходный класс, чтобы клиенты даже не заметили, что работают с другим классом. В нашем примере `LoggingEmployee` - это декоратор `Employee`. Он должен иметь метод `pay()` и все остальные методы которые есть у `Employee`.

Декоратор - это хороший способ добавить функциональность,если редактируемый метод `pay()` уже вызывается из кучи мест. Однако есть еще способ обернуть метод без декоратора. Давайте представим, что нам нужно логировать вызовы метода 'pay()' всего из одного места. Вместо того ,чтобы оорачивать это все в декоратор, мы можем положитье его в другой класс, который принимает экземпляр `Employee`, производит оплату, а затем записывает инофрмацию об этом событии. Давайте напишем вот таклй маленький класс:

[source,java]
----
class LoggingPayDispatcher {
     private Employee e;
         public LoggingPayDispatcher(Employee e) {
            this.e = e;
         }
         
         public void pay() {
            employee.pay();
            logPayment();
         }
         
         private void logPayment() {
         ...
     }
     ...
}
----

Сейчас мы можем создать экземпляр `LogPayDispatcher`  одном месте, только в том,где нужно записывать сообщения о платежах.
Now we can create LogPayDispatcher in the one place where we need to log payments.
The key to Wrap Class is that you are able to add new behavior into a system without adding it to an existing
class. When there are many calls to the code you want to wrap, it often pays to move toward a decorator-ish
wrapper. When you use the decorator pattern, you can transparently add new behavior to a set of existing calls
like pay()all at once. On the other hand, if the new behavior only has to happen in a couple of places,
creating a wrapper that isn't decorator-ish can be very useful. Over time, you should pay attention to the
responsibilities of the wrapper and see if the wrapper can become another high-level concept in your system.

