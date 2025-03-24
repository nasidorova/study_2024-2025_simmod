---
## Front matter
title: "Отчёт по лабораторной работе 8"
subtitle: "Модель TCP/AQM"
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

Изучить даннную модель.

# Задание

1. Построить модель TCP/AQM в xcos
2. Построить модель TCP/AQM в OpenModelica

# Теоретическое введение

Математическая модель (рис. [-@fig:013]).

![Уравнения](image/13.jpg){#fig:013 width=70%}

# Выполнение лабораторной работы

Установила в контексте переменные, принимающие конкретные значения: N - число сессий, R - время двойного оборота, K - параметр задержки, C - скорость обработки пакетов, W0 - размер окна, Q0 - размер очереди  (рис. [-@fig:001]).

![Константы](image/1.jpg){#fig:001 width=70%}

Установила параметры в блоки интегралов  (рис. [-@fig:002]).

![Размер окна](image/2.jpg){#fig:002 width=70%}

 (рис. [-@fig:003]).

![Размер очереди](image/3.jpg){#fig:003 width=70%}

Установила параметры в блок задержки  (рис. [-@fig:004]).

![Задержка](image/4.jpg){#fig:004 width=70%}

Получившаяся модель в xcos (рис. [-@fig:005]).

![Модель](image/5.jpg){#fig:005 width=70%}

Фазовый портрет, который показывает наличие колебаний в параметрах системы (рис. [-@fig:006]).

![Фазовый портрет](image/6.jpg){#fig:006 width=70%}

График динамики изменения размера окна и очереди (рис. [-@fig:007]).

![Динамика изменений окна и очереди](image/7.jpg){#fig:007 width=70%}

Уменьшила скорость обработки пакетов с 1 до 0.9 (рис. [-@fig:008]).

![Новый фазовый портрет](image/8.jpg){#fig:008 width=70%}

(рис. [-@fig:009]).

![Новый график](image/9.jpg){#fig:009 width=70%}

Код для реализации в OpenModelica (рис. [-@fig:010]).

![Код](image/10.jpg){#fig:010 width=70%}

График изменения размеров окна и очереди (рис. [-@fig:011]).

![График](image/11.jpg){#fig:011 width=70%}

Фазовый портрет (рис. [-@fig:012]).

![Фазовый портрет](image/12.jpg){#fig:012 width=70%}


# Выводы

Реализовала модель TCP/AQM в xcos и в OpenModelica.

# Список литературы{.unnumbered}

::: {#refs}
:::
