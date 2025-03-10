---
## Front matter
title: "Отчёт по лабораторной работе 6"
subtitle: "Модель хищник-жертва"
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

Изучить данную модель.

# Задание

Смоделировать систему уравнений в программе xcos с использованием блока Modelica и без, смоделировать также в программе OpenModelica. Построить график изменения численности жертв и хищников, построить фазовый портрет системы.

# Теоретическое введение

Система уравнений, описывающая изменение численности жертв и хищников (рис. [-@fig:014]).

![Дифференциальные уравнения](image/14.jpg){#fig:014 width=70%}

# Выполнение лабораторной работы

В программе xcos установила коэффициенты рождаемости и смертности для жертв и хищников (рис. [-@fig:001]).

![Установка контекста](image/1.jpg){#fig:001 width=70%}

Схема дифференциальных уравнений с использованием блоков суммирования, интегрирования, умножения, и других (рис. [-@fig:002]).

![Простая схема](image/2.jpg){#fig:002 width=70%}

Установка изначального числа жертв в блоке интегрирования (рис. [-@fig:003]).

![Изначальное число жертв](image/3.jpg){#fig:003 width=70%}

Установка изначального числа хищников в блоке интегрирования (рис. [-@fig:004]).

![Изначальное число хищников](image/4.jpg){#fig:004 width=70%}

Получившийся фазовый портрет  (рис. [-@fig:005]).

![Фазовый портрет](image/5.jpg){#fig:005 width=70%}

График изменения численности жертв и хищников (рис. [-@fig:006]).

![График изменения численности](image/6.jpg){#fig:006 width=70%}

При создании модели с помощью Modelica generic добавила переменные в блок (рис. [-@fig:007]).

![Инициализация переменных](image/7.jpg){#fig:007 width=70%}

Написала в этом же блоке код для уравнений (рис. [-@fig:008]).

![Код на языке Modelica](image/8.jpg){#fig:008 width=70%}

Сама модель с блоком Modelica generic (рис. [-@fig:009]).

![модель Modelica](image/9.jpg){#fig:009 width=70%}

Получившиеся графики совпадают с графиками модели xcos (рис. [-@fig:010]).

![Графики](image/10.jpg){#fig:010 width=70%}

Код для моделирования в OpenModelica (рис. [-@fig:011]).

![OpenModelica](image/11.jpg){#fig:011 width=70%}

График изменения численности (рис. [-@fig:012]).

![График](image/12.jpg){#fig:012 width=70%}

Фазовый портрет (рис. [-@fig:013]).

![График](image/13.jpg){#fig:013 width=70%}

# Выводы

Изменения численности жертв и хищников колеблется в некотором промежутке, то снимаясь до 1 особи, то повышаясь до некторого количества. Изменения периодичны.

# Список литературы{.unnumbered}

::: {#refs}
:::
