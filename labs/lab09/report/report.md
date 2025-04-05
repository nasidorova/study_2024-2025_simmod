---
## Front matter
title: "Отчёт по лабораторной работе 9"
subtitle: "Модель Накорми студентов"
author: "Наталья Андреевна Сидорова"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Реализовать модель "Накорми студентов" с помощью сетей Петри в программе CPN Tools.

# Задание

1. Реализовать модель
2. Провести симуляцию
3. Создать отчет о симуляции в State Space

# Выполнение лабораторной работы

Создала саму модель в виде сети Петри. В ней есть три позиции (в виде овалов), один переход (в виде квадрата) и соединения между этими элементами графа  (рис. [-@fig:001]).

![Сеть Петри](image/1.JPG){#fig:001 width=70%}

Добавила декларации: объявила множества s и p, а также названия входящих в него фишек, объявила переменные х и у и к какому множеству относится каждое из них, объявила начальные значения множеств (рис. [-@fig:002]).

![Декларации](image/2.JPG){#fig:002 width=70%}

Добавила в модель фишки, подписала пути (рис. [-@fig:003]).

![Готовая модель](image/3.JPG){#fig:003 width=70%}

Провела симуляцию сразу до конечного значения (рис. [-@fig:004]).

![Конец симуляции](image/4.JPG){#fig:004 width=70%}

Один шаг симуляции (рис. [-@fig:005]).

![Первый этап](image/5.JPG){#fig:005 width=70%}

Для создания анализа пространства состояний данной сети я воспользовалась разделом State Space и создала там наш граф. Можно увидеть мини отчет по каждой из вершин (рис. [-@fig:006]).

![State Space](image/6.JPG){#fig:006 width=70%}

Сам отчет включает в себя несколько разделов: статистика (число узлов, число дуг), ограниченность(верхние и нижние границы), домашние маркировки, живые маркировки (тупики и переходы), справедливость(тип справедливости переходов). (рис. [-@fig:007]).

![Отчет](image/7.JPG){#fig:007 width=70%}

(рис. [-@fig:008]).

![Отчет](image/8.JPG){#fig:008 width=70%}

# Выводы

Я смоделировала сеть Петри в CPN Tools и сделала отчет в State Space.

# Список литературы{.unnumbered}

::: {#refs}
:::
