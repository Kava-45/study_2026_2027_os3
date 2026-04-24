---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа №8"
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

Освоить на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом

# Выполнение лабораторной работы


Для начала откроем терминал и создадим два файла с текстом который указан в лабораторной работе 

![1](image/1.png){#fig:001 width=70%}

После чего просматриваем содержимого в hex 

![2](image/2.png){#fig:002 width=70%}

Далее создаем бинарный ключ 

![3](image/3.png){#fig:003 width=70%}

Затем мы копируем два файла в бинарные 

![4](image/4.png){#fig:004 width=70%}

После чего шифруем в XOR первое сообщение  и второе в шифрование XOR 

![5](image/5.png){#fig:005 width=70%}

Затем выводим зашифрованные данные 

![6](image/6.png){#fig:006 width=70%}

Далее делаем XOR двух шифротекстов P1 или P2 и восстановление P2 из предположения, что известен P1

![7](image/7.png){#fig:007 width=70%}

И проверяем результат 

![8](image/8.png){#fig:008 width=70%}



# Выводы

В результате выполнения лабораторной работы я освоил на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом
