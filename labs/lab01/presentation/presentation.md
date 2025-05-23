---
## Front matter
lang: ru-RU
title: Лабораторная работа №1
subtitle: Простые модели компьютерной сети
author:
  - Оширова Ю. Н.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 16 февраля 2025

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

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Оширова Юлия Николаевна
  * студентка группы НФИбд-01-22
  * Российский университет дружбы народов

:::
::: {.column width="30%"}


:::
::::::::::::::

# Цель работы

Приобрести навыки моделирования сетей передачи данных с помощью средства имитационного моделирования NS-2, а также проанализировать полученные результаты моделирования.

# Задание

1) Создать шаблон сценария для NS-2;
2) Выполнить простой пример описания топологии сети, состоящей из двух узлов и одного соединения;
3) Выполнить пример с усложнённой топологией сети;
4) Выполнить пример с кольцевой топологией сети;
5) Выполнить упражнение.

# Выполнение лабораторной работы

## Шаблон сценария для NS-2

В своём рабочем каталоге создадим директорию mip, в которой будут выполняться лабораторные работы. Внутри mip создадим директорию lab-ns, а в ней файл shablon.tcl (рис. [-@fig:001]).

![Шаблон для сценария](image/1.jpeg){#fig:001 width=70%}

Откроем на редактирование файл shablon.tcl (рис. [-@fig:002]).

Сначала создадим объект типа Simulator. Затем создадим переменную nf и укажем, что требуется открыть на запись nam-файл для регистрации выходных результатов моделирования. Вторая строка даёт команду симулятору записывать все данные о динамике модели в файл out.nam. Далее создадим переменную f и откроем на запись файл трассировки для регистрации всех событий модели. После этого добавим процедуру finish, которая закрывает файлы трассировки и запускает nam. С помощью команды at указываем планировщику событий, что процедуру finish запустим через 5 с после начала моделирования, после чего запустим симулятор ns.

![Добавление кода](image/2.jpeg){#fig:002 width=70%}

Сохранив изменения в отредактированном файле shablon.tcl и закрыв его, запустим симулятор командой ns shablon.tcl. Увидим пустую область моделирования, поскольку ещё не определены никакие объекты и действия (рис. [-@fig:003]).

![Область моделирования](image/3.jpeg){#fig:003 width=70%}

## Простой пример описания топологии сети, состоящей из двух узлов и одного соединения

Требуется смоделировать сеть передачи данных, состоящую из двух узлов, соединённых дуплексной линией связи с полосой пропускания 2 Мб/с и задержкой 10 мс, очередью с обслуживанием типа DropTail. От одного узла к другому по протоколу UDP осуществляется передача пакетов, размером 500 байт, с постоянной скоростью 200 пакетов в секунду.

![Добавление кода](image/4.jpeg){#fig:004 width=70%}

Сохранив изменения в отредактированном файле и запустив симулятор, получим в качестве результата запуск аниматора nam в фоновом режиме (рис. [-@fig:005]).

![Область моделирования](image/5.jpeg){#fig:005 width=70%}

При нажатии на кнопку play в окне nam через 0.5 секунды из узла 0 данные начнут поступать к узлу 1.

## Пример с усложнённой топологией сети

Описание моделируемой сети:

![Добавление кода](image/6.jpeg){#fig:006 width=70%}

## Сохранив изменения в отредактированном файле и запустив симулятор, получим анимированный результат моделирования (рис. [-@fig:007]).

![Область моделирования](image/7.jpeg){#fig:007 width=70%}

## Пример с кольцевой топологией сети

![Добавление кода](image/8.jpeg){#fig:008 width=70%}

![Область моделирования](image/9.jpeg){#fig:009 width=70%}

## Передача данных при кольцевой топологии сети в случае разрыва соединения представлена на рис. [-@fig:010].

![Область моделирования](image/10.jpeg){#fig:010 width=70%}

Добавив в начало скрипта после команды создания объекта Simulator:

$ns rtproto DV

увидим, что сразу после запуска в сети отправляется небольшое количество маленьких пакетов, используемых для обмена информацией, необходимой для маршрутизации между узлами (рис. [-@fig:011]). Когда соединение будет разорвано, информация о топологии будет обновлена, и пакеты будут отсылаться по новому маршруту через узлы n(6), n(5) и n(4).

![Область моделирования](image/11.jpeg){#fig:011 width=70%}

## Упражнение

Внесем следующие изменения в реализацию примера с кольцевой топологией сети:

![Добавление кода](image/12.jpeg){#fig:012 width=70%}

## Запустим программу и увидим, что пакеты идут по кратчайшему пути через узел n(1) ([-@fig:013]).

![Область моделирования](image/13.jpeg){#fig:013 width=70%}

## При разрыве соединения часть пакетов теряется, но поскольку данные обновляются пакеты начинают идти по другому пути ([-@fig:014]).

![Область моделирования](image/14.jpeg){#fig:014 width=70%}

## После восстановления соединения пакеты снова идут по кратчайшему пути ([-@fig:015]).

![Область моделирования](image/15.jpeg){#fig:015 width=70%}

# Выводы

В процессе выполнения данной лабораторной работы я приобрела навыки моделирования сетей передачи данных с помощью средства имитационного моделирования NS-2, а также проанализировала полученные результаты моделирования.