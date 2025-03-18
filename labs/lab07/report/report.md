---
## Front matter
title: "Отчёт по лабораторной работе 7"
subtitle: "Модель М|M|1"
author: "Натадья Андреевна Сидорова"

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

Создать модель системы массового обслуживания данного типа

# Задание

1. Создать суперблок моделирования поступления заявок в систему по пуассоновскому распределению
2. Создать суперблок моделирования обработки заявок
3. Создать саму модель

# Теоретическое введение

Заявки поступают в систему по пуассоновскому распределению, заявки обслуживаются в очереди по экспоненциальному распределению. 

# Выполнение лабораторной работы

Установила необходимые для наших распределений параметры (рис. [-@fig:001]).

![параметры](image/1.jpg){#fig:001 width=70%}

Суперблок поступления заявок в систему по пуассоновскому распределению (рис. [-@fig:002]).

![поступление заявок](image/2.jpg){#fig:002 width=70%}

Установка функции экспоненциального распределения (рис. [-@fig:003]).

![функция](image/3.jpg){#fig:003 width=70%}

Суперблок обработки заявок (рис. [-@fig:004]).

![обработка заявок](image/4.jpg){#fig:004 width=70%}

Общая модель с двумя суперблоками (рис. [-@fig:005]).

![сама модель](image/5.jpg){#fig:005 width=70%}

График поступления и обработки заявок (рис. [-@fig:006]).

![поступление и обработка](image/6.jpg){#fig:006 width=70%}

График изменения размера очереди (рис. [-@fig:007]).

![размер очереди](image/7.jpg){#fig:007 width=70%}

# Выводы

Создала модель системы массового обслуживания и изучила полученные графики

# Список литературы{.unnumbered}

::: {#refs}
:::
