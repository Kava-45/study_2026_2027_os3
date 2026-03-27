---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа №3"
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

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей

# Выполнение лабораторной работы


Для начала переходим в супер пользователя и создаем пользователя guest2 и добавляем пользователя guest2 в группу guest

![1](image/1.png){#fig:001 width=70%}

После чего открываем новый терминал под guest, затем определеим директорию для пользователя guest и сравниваем команды id -Gn и id -G с пользователем guest2

![2](image/2.png){#fig:002 width=70%}

Теперь открываем еще один терминал и переходим в пользователя guest2, также определяем директорию и сравниваем команды id -Gn и id -G с пользователем guest

![3](image/3.png){#fig:003 width=70%}

После сравнения двух пользователей, сравниваем полученную информацию с содержимым файла /etc/group

![4](image/4.png){#fig:004 width=70%}

Далее от имени пользователя guest2 выполним регистрацию пользователя guest2 в группу guest командой newgrp guest

![5](image/5.png){#fig:005 width=70%}

Затем от пользователя guest меняем права директории /home/guest разрешив всех действия для пользователей группы 

![6](image/6.png){#fig:006 width=70%}

После чего от имени пользователя guest снимим с директории /home/guest/dir1 все атрибуты командой chmod 000 dirl и проверяем снятия атрибутов 

![7](image/7.png){#fig:007 width=70%}



# Выводы

В результате выполнения лабораторной работы я получил практические навыки работы в консоли с атрибутами файлов для групп пользователей 
