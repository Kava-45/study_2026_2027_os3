---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа №1"
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

Целью данной работы является приобретение рпактических навыков установки операционной системы на виртуальную машину настрорйки минимально необходимых для дальнейшей работы сервисов

# Выполнение лабораторной работы

Для начала назовем нашу виртуальную машину Rocky3 и выберем установочный диск (рис. [-@fig:001]).

![1](image/1.png){#fig:001 width=70%}


Выделяем память и процессор (рис. [-@fig:002]).

![2](image/2.png){#fig:002 width=70%}

Выделяем размер диска (20 гб) (рис. [-@fig:003]).

![3](image/3.png){#fig:003 width=70%}

Далее выбираем язык,я выбрал русский язык (рис. [-@fig:004]).

![4](image/4.png){#fig:004 width=70%}

Выбираем диск куда устанавится система (рис. [-@fig:005]).

![5](image/5.png){#fig:005 width=70%}

Настроим рут пользователя указав пароль для него и разрешив ему ssh (рис. [-@fig:007]).

![7](image/7.png){#fig:007 width=70%}

Настром своего пользователя согласно об именовании (рис. [-@fig:008]).

![6](image/6.png){#fig:008 width=70%}


Теперь выполняем домашнее задание  находим версию ядра (рис. [-@fig:011]).

![8](image/8.png){#fig:011 width=70%}


2) Частота процессора  (рис. [-@fig:012]).

![9](image/9.png){#fig:012 width=70%}


3) Модель процессора (рис. [-@fig:013]).

![10](image/10.png){#fig:013 width=70%}

4) Количество доступной памяти  (рис. [-@fig:014]).

![11](image/11.png){#fig:014 width=70%}


5) Найти гипервизор  (рис. [-@fig:015]).

![12](image/11.png){#fig:015 width=70%}


6)Найти тип файловой системы корневого раздела (рис. [-@fig:016]). 


![13](image/12.png){#fig:016 width=70%}

7) Нати последовательность монтирования файловых систем

![14](image/13.png){#fig:017 width=70%}

# Выводы

В результате выполнения лаборатоной работы была установлена система Rocky.

