---
## Front matter
lang: ru-RU
title: Лабораторная работа №8
subtitle: Модель TCP/AQM
author:
  - Оширова Ю. Н.
institute:
  - Российский университет дружбы народов, Москва, Россия

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Информация

## Докладчик

  * Оширова Юлия Николаевна
  * студентка группы НФИбд-01-22
  * Российский университет дружбы народов

## Цель работы

Реализовать модель TCP/AQM в xcos и OpenModelica.

## Задание

1. Построить модель TCP/AQM в xcos;
2. Построить графики динамики изменения размера TCP окна $W(t)$ и размера очереди $Q(t)$;
3. Построить модель TCP/AQM в OpenModelica;

## Реализация в xcos

![Установка контекста](image/1.jpeg){#fig:001 width=70%}

## Реализация в xcos

![Модель TCP/AQM в xcos](image/2.jpeg){#fig:002 width=70%}

## Реализация в xcos

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t)](image/3.jpeg){#fig:003 width=70%}

## Реализация в xcos

![Фазовый портрет (W, Q)](image/4.jpeg){#fig:004 width=70%}

## Реализация в xcos

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t) при С = 0.9](image/7.jpeg){#fig:005 width=70%}

## Реализация в xcos

![Фазовый портрет (W, Q) при С = 0.9](image/8.jpeg){#fig:006 width=70%}

## Реализация модели в OpenModelica

```
parameter Real N=1;
parameter Real R=1;
parameter Real K=5.3;
parameter Real C=1;

Real W(start=0.1);
Real Q(start=1);

equation

der(W)= 1/R - W*delay(W, R)/(2*R)*K*delay(Q, R);
der(Q)= if (Q==0) then max(N*W/R-C,0) else (N*W/R-C);
```

## Реализация модели в OpenModelica

![Динамика изменения размера TCP окна W (t) и размера очереди Q(t). OpenModelica](image/5.jpeg){#fig:007 width=70%}

## Реализация модели в OpenModelica

![Фазовый портрет (W, Q). OpenModelica](image/6.jpeg){#fig:008 width=70%}

## Выводы

В процессе выполнения данной лабораторной работы я реализовала модель TCP/AQM в xcos и OpenModelica.