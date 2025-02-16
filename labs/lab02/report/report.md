---
## Front matter
title: " Отчёт по лабораторной работе 2"
subtitle: "Исследование протокола TCP и алгоритма управления очередью RED"
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


# Выполнение лабораторной работы

Я построила пример с дисциплиной RED. Сеть состоит из 6 узлов, между всеми узлами установлено дуплексное соединение с различной пропускной способностью. Узел r1 использует очередь с дисциплиной RED максимальный размер очереди 25 (рис. [-@fig:001]).

![1 часть кода](image/1.jpg){#fig:001 width=70%}

За основу взяла код шаблона с 1 лабораторной (рис. [-@fig:002]).

![2 часть кода](image/2.jpg){#fig:002 width=70%}

Запустила Xgraph и посмотрела 2 графика : график изменения размера окна и график изменения размера очереди (рис. [-@fig:003]).

![Графики](image/3.jpg){#fig:003 width=70%}

Для выполнения упражнения я изменила на узле s1 тип протокола TCP  с Reno на NewReno (рис. [-@fig:004]).

![NewReno](image/4.jpg){#fig:004 width=70%}
 
 Получившийся график почти идентичен начальному (рис. [-@fig:005]).

![NewReno график ](image/5.jpg){#fig:005 width=70%}

Для выполнения упражнения я изменила на узле s1 тип протокола TCP с NewReno на Vegas (рис. [-@fig:006]).

![ Vegas](image/6.jpg){#fig:006 width=70%}

Получившийся график изменения размеров окна отличается, максимальный размер окна снизился с 30+ до 20, максимальный размер очереди также снизился (рис. [-@fig:007]).

![ Vegas график](image/7.jpg){#fig:007 width=70%}

Изменила цвет фона, цвет траекторий, подписи к осям, подпись траектории в легенде (рис. [-@fig:008]).

![ Код изменения](image/8.jpg){#fig:008 width=70%}

(рис. [-@fig:009]).

![ 2 часть](image/9.jpg){#fig:009 width=70%}

получившийся график (рис. [-@fig:010]).

![ Новый график](image/10.jpg){#fig:010 width=70%}

# Выводы

TCP Vegas обнаруживает перегрузку в сети до того, как случайно теряется пакет, и мгновенно уменьшается размер окна. TCP Vegas обрабатывает перегрузку без потерь пакета.

# Список литературы{.unnumbered}

::: {#refs}
:::
