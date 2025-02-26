---
## Front matter
title: "Отчёт по упражнению xcos"
subtitle: "Фигуры Лиссажу"
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

Я открыла программу xcos и смоделировала систему, состоящую из часов моедльного времени, регистрирующего устройства для построения графика и двух блоков генератора синусоидального сигнала (рис. [-@fig:001]).

![Сама система](image/1.jpg){#fig:001 width=70%}

В нашей системе есть параметры: амплитуды колебаний А и В, частоты а и b, сдвиг фаз %phi.
В первом случае  взяла А=В=1, а=2, b=2, %phi=0, %pi/4, %pi/2, 3*%pi/4, pi и получила одинаковые графики (рис. [-@fig:002]).

![Прямая](image/2.jpg){#fig:002 width=70%}

Во втором случае я взяла А=В=1, а=2, b=4, и для %phi=0, pi я получила одинаковые графики (рис. [-@fig:003]).

![График](image/3.jpg){#fig:003 width=70%}

Во втором случае для %phi= %pi/4, 3*%pi/4 я получила такой график (рис. [-@fig:004]).

![График](image/4.jpg){#fig:004 width=70%}

Во втором случае для %phi= %pi/2 я получила такой график (рис. [-@fig:005]).

![График](image/5.jpg){#fig:005 width=70%}

В третьем случае для А=В=1, а=2, b=6, и для %phi=0, pi я получила одинаковые графики (рис. [-@fig:006]).

![График](image/6.jpg){#fig:006 width=70%}

В третьем случае для %phi= %pi/4, 3*%pi/4 я получила такой график (рис. [-@fig:007]).

![График](image/7.jpg){#fig:007 width=70%}

В третьем случае для %phi= %pi/2 я получила такой график (рис. [-@fig:008]).

![График](image/8.jpg){#fig:008 width=70%}

В четвертом случае для А=В=1, а=2, b=3, и для %phi=0, pi я получила одинаковые графики (рис. [-@fig:009]).

![График](image/9.jpg){#fig:009 width=70%}

В четвертом случае для %phi= %pi/4, 3*%pi/4 я получила такой график (рис. [-@fig:010]).

![График](image/10.jpg){#fig:010 width=70%}

В четвертом случае для %phi= %pi/2 я получила такой график (рис. [-@fig:011]).

![График](image/11.jpg){#fig:011 width=70%}


# Выводы

В ходе выполнения работы я смоделировала различные фигуры Лиссажу в программе xcos.

# Список литературы{.unnumbered}

::: {#refs}
:::
