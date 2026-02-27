---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа №2"
author: "Казначеев Сергей Ильич"

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

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного раграничения доступа в современных системах с открытым кодом на базе OC Linux

# Выполнение лабораторной работы

Для начала откроем терминал и создадим пользователя  guest 

![1](image/6.png){#fig:001 width=70%}

После чего зайдем от нового пользователя guest, проверим в какой мы находимся директории, затем уточним имя, после чего id и группу

![2](image/1.png){#fig:002 width=70%}

Далее просмотрим файл  /etc/passwd

![3](image/2.png){#fig:003 width=70%}

Теперь проверяем какие  атрибуты установлены на поддиректориях находящихся в директории home 

![4](image/3.png){#fig:004 width=70%}

Затем создаем домашнюю директорию dir1 и проверяем  права данной директории 

![5](image/4.png){#fig:005 width=70%}

После чего снимаем с директории dir1 все атрибуты и проверяем,далее пытаемся создать в директории dir1 файл file1

![6](image/5.png){#fig:006 width=70%}

# Выводы

В результате выполнения лабораторной работы я получил навыки работы в консоли с атрибутами файлов закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе OC Linux

