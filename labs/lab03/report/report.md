---
## Front matter
title: "Отчёт по лабораторной работе 3"
subtitle: "Моделирование стохастических процессов"
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

Реализовала на NS-2 модель системы массового обслуживания (рис. [-@fig:001]).

![Код реализации](image/1.jpg){#fig:001 width=70%}

Вторая часть кода (рис. [-@fig:002]).

![Код реализации часть 2](image/2.jpg){#fig:002 width=70%}

Теоретическая вероятность потери получилась равная 0,теоретическая средняя длина очереди получилась 9,09
(рис. [-@fig:003]).

![Вывод результата в консоль](image/3.jpg){#fig:003 width=70%}

Создала график в GNUplot, на нем изображен размер очереди в пакетах, приближение сплайном и приближение Безье (рис. [-@fig:004]).

![Код построения графика](image/4.jpg){#fig:004 width=70%}

Сделала файл исполняемым, дав необходимые права (рис. [-@fig:005]).

![Нужные файлу права](image/5.jpg){#fig:005 width=70%}

Вывод графика (рис. [-@fig:006]).

![Получившийся график](image/6.jpg){#fig:006 width=70%}

# Выводы

В этой лабораторной я создала модель системы массового обслуживания.

# Список литературы{.unnumbered}

::: {#refs}
:::
