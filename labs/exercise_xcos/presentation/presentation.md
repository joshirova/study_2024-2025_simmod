---
## Front matter
lang: ru-RU
title: Презентация по выполнению упражнения
subtitle: Фигура Лиссажу
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
  * [1132222843@pfur.ru](mailto:11322228433@pfur.ru)

## Цель работы

Выполнить упражнение по ознакомлению с программой *xcos*.

## Задание

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) $A = B = 1, a = 2, b = 2, \, \delta = 0; \, \pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$

2) $A = B = 1, a = 2, b = 4, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi;$

3) $A = B = 1, a = 2, b = 6, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3π/4; \, π;$

4) $A = B = 1, a = 2, b = 3, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi.$

## Фигура Лиссажу

Математическое выражение для кривой Лиссажу:
$$
\begin{cases}
  x(t) = A sin(at + \delta),\\
  y(t) = B sin(bt),
\end{cases}
$$
где $A, B$ -- амплитуды колебаний, $a, b$ -- частоты, $\delta$ -- сдвиг фаз.

## Блоки в xcos

- CLOCK_c -- запуск часов модельного времени;
- GENSIN_f -- блок генератора синусоидального сигнала;
- CSOPXY -- анимированное регистрирующее устройство для построения графика
типа y = f(x);
- TEXT_f -- задаёт текст примечаний.

## Выполнение лабораторной работы

![Модель для построения фигуры Лиссажу в xcos](image/1.jpeg){#fig:001 width=70%}

## Выполнение лабораторной работы

![Ввод параметров для генератора синусоидальных колебаний](image/2.jpeg){#fig:002 width=70%}

## Выполнение лабораторной работы

![Ввод параметров для CSOPXY](image/3.jpeg){#fig:003 width=40%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 0$](image/4.jpeg){#fig:004 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /4$](image/5.jpeg){#fig:005 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /2$](image/6.jpeg){#fig:006 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 3\pi /4$](image/7.jpeg){#fig:007 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi$](image/8.jpeg){#fig:008 width=70%}

## Выполнение лабораторной работы

![Ввод параметров для генератора синусоидальных колебаний](image/9.jpeg){#fig:009 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 0$](image/10.jpeg){#fig:010 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /4$](image/11.jpeg){#fig:011 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /2$](image/12.jpeg){#fig:012 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 3\pi /4$](image/13.jpeg){#fig:013 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi$](image/14.jpeg){#fig:014 width=70%}

## Выполнение лабораторной работы

![Ввод параметров для генератора синусоидальных колебаний](image/15.jpeg){#fig:015 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 0$](image/16.jpeg){#fig:016 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /4$](image/17.jpeg){#fig:017 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /2$](image/18.jpeg){#fig:018 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 3\pi /4$](image/19.jpeg){#fig:019 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi$](image/20.jpeg){#fig:020 width=70%}

## Выполнение лабораторной работы

![Ввод параметров для генератора синусоидальных колебаний](image/21.jpeg){#fig:021 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 0$](image/22.jpeg){#fig:022 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /4$](image/23.jpeg){#fig:023 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /2$](image/24.jpeg){#fig:024 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 3\pi /4$](image/25.jpeg){#fig:025 width=70%}

## Выполнение лабораторной работы

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi$](image/26.jpeg){#fig:026 width=70%}

## Выводы

В результате выполнения данной лабораторной работы я выполнила упражнение по ознакомлению с программой *xcos*.