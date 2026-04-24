---
## Front matter
title: "Индивидуальный проект"
subtitle: "Часть 4"
author: "Казаначеев Сергей Ильич"

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

# Цель 

Изпользовать nikto


# Задачи

Для начала откровем терминал и установим nikto 

![1](image/1.png)

После чего проверим сканирование веб-сервера 

![2](image/2.png)

Далее проверим детальное сканирование с выводом в файл 

![3](image/3.png)

Затем сделаем сканирование с игнорированием ошибок SSL

![4](image/4.png)

После чего сделаем сканирование конкретного порта, я выбрал 8080

![5](image/5.png)

Далее сделаем ускоренное сканирование

![6](image/6.png)

Затем сделаем проверку конкретной уязвимости или файла 

![7](image/7.png)

И в последней проверке отсканируем конкретный сервер, сохраним отчет в формате html и максимально время 120

![8](image/8.png)

# Выводы

В результате выполнения лабораторной работы я получил навыки работы с nikto

