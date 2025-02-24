---
## Front matter
title: "Отчёт по лабораторной работе 4"
subtitle: "Задания для самостоятельного выполнения"
author: "Сидорова Наталья Андреевна"

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

# Выполнение лабораторной работы

По заданию создала модель сети, состоящей из 20 TCP источников и 20 TCP приемников, двух маршрутизаторов между приемниками и источниками. Между TCP источниками и первым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с, задержкой 20мс и очередью DropTail. Между TCP приемниками и вторым маршрутизатором установлены дуплексные соединения с пропускной способностью 100 Мбит/с, задержкой 20мс и очередью DropTail. Между маршрутизаторами установлено симплексное соединение с пропускной способностью 20 Мбит/с, задержкой 15 мс и очередью типа RED, размер буфера 300 пакетов. В обратную сторону установлено симплексное соединение с пропускной способностью 15 Мбит/с, задержкой 20 мс и очередью типа DropTail (рис. [-@fig:001]).

![Создание модели](image/1.jpg){#fig:001 width=70%}

(рис. [-@fig:002]).

![Код моделирования](image/2.jpg){#fig:002 width=70%}

(рис. [-@fig:003]).

![Моделирование сети](image/3.jpg){#fig:003 width=70%}

Получилась модель, подходящая требованиям (рис. [-@fig:004]).

![Сама модель](image/4.jpg){#fig:004 width=70%}

График Xgraph изменения размера TCP окна на линке одного источника (рис. [-@fig:005]).

![График на одном источнике](image/5.jpg){#fig:005 width=70%}

График Xgraph изменения размера TCP окна на всех источниках (рис. [-@fig:006]).

![График на всех источниках](image/6.jpg){#fig:006 width=70%}

График Xgraph изменения размера очереди (рис. [-@fig:007]).

![График очереди](image/7.jpg){#fig:007 width=70%}

График Xgraph изменения размера средней очереди (рис. [-@fig:008]).

![График средней очереди](image/8.jpg){#fig:008 width=70%}

Создала те же графики, но в GNUPlot (рис. [-@fig:009]).

![Код в GNUPlot](image/9.jpg){#fig:009 width=70%}

(рис. [-@fig:010]).

![Код в GNUPlot 2](image/10.jpg){#fig:010 width=70%}

График GNUPlot изменения размера средней очереди (рис. [-@fig:011]).

![График средней очереди](image/11.jpg){#fig:011 width=70%}

График GNUPlot изменения размера очереди (рис. [-@fig:012]).

![График очереди](image/12.jpg){#fig:012 width=70%}

График GNUPlot изменения размера TCP окна на линке одного источника (рис. [-@fig:013]).

![График на одном источнике](image/13.jpg){#fig:013 width=70%}

График GNUPlot изменения размера TCP окна на всех источниках (рис. [-@fig:014]).

![График на всех источниках](image/14.jpg){#fig:014 width=70%}

# Выводы

Создала свою сеть в NS-2, смоделировала передачу данных по моей сети, создала графики изменения длины очереди, средней длины очереди, изменения размера TCP окна на линке одного источника, изменения размера TCP окна на всех источниках в GNUPlot и Xgraph

# Список литературы{.unnumbered}

::: {#refs}
:::
