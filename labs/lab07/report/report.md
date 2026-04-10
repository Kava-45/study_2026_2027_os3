---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа №7"
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

Освоить на практике применение режима однократного гаммирования.

# Выполнение лабораторной работы


Для начала откроем  терминал, и перейдем в суперпользователя, и откроем питон 

![1](image/1.png){#fig:001 width=70%}

После чего пропишем команду для нахождения ключа, данная команда загружает заданный шифротекст, преобразует целевую фразу в ббайты и  с помощью операции XOR вычисляет ключ, который превращает данный шифротекст в фразу С Новым Годом 

![2](image/2.png){#fig:002 width=70%}

ЗаТем пропишем команду которая загружает шифротекст и полученный ключ, выполняет XOR между ними и выводит расшифрованный открытый  текст, Подтверждает, что при использовании найденного ключа расшифровывается именно нужная фраза 


![3](image/3.png){#fig:003 width=70%}

# Выводы

В результате выполнения лабораторной работы я освоил на практике применение режима однократного гаммирования 
