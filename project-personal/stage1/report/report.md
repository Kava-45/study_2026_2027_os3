---
## Front matter
title: "Отчет о Индивидуальном проекте "
subtitle: "Индивидуальном проекте №1"
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

Установить дистрибутив Kali Linux в виртуальную машину 

# Выполнение индивидуального проекта

После того как настрои kali linux выберем язык 

![1](image/1.png){#fig:001 width=70%}

После чего выберем местонахождение 

![2](image/2.png){#fig:002 width=70%}

Далее выберем настройку клавиатуры 

![3](image/3.png){#fig:003 width=70%}

Затем настроим сеть

![4](image/4.png){#fig:004 width=70%}

После настоим учетную запись пользователя 

![5](image/5.png){#fig:005 width=70%}

И пароль к учетной записи 

![6](image/6.png){#fig:007 width=70%}

После чего выберем разметку дисков

![7](image/7.png){#fig:008 width=70%}

И выберем сам диск 

![8](image/8.png){#fig:011 width=70%}

Подтверждаем разметку дисков 

![9](image/9.png){#fig:012 width=70%}

И записываем изменения 

![10](image/10.png){#fig:013 width=70%}

Затем выбераем программные обеспечения

![11](image/11.png){#fig:014 width=70%}

Устанавливаем системного загрузчика GRUB

![12](image/12.png){#fig:015 width=70%}

После чего перезапускаем систему и входим в учетную запись 

![13](image/13.png){#fig:016 width=70%}



# Выводы

В результате выполнения индивидуального проекта был установлен kali linux.

