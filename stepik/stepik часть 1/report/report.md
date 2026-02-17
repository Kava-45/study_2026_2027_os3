---
## Front matter
title: "Введение в linux"
subtitle: "Часть 1"
author: "Казанчеев Сергей Ильич"

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

Прохождение Первой части внешнего курса stepik

# Выполнение лабораторной работы

Задание 1

Обычно использую операционную систему Linux и Windows

![sc1](image/1.png)

Задание 2

Специальная программа для запуска OC на другой OC

![sc2](image/2.png)

Задание 3

Да смог смог запустить Linux

![sc3](image/3.png)

Задание 4

Создаем документ в OpenOffice/LibreOffice Write и далее записываем фразу Hello Linux! шрифтом FreeMono

![sc4](image/4.png)

Задание 5

Linux имеет установочные пакеты deb

![sc5](image/5.png)

Задание 6

После установки VLC запускаем файл и отрываем Help -> About и пишем ниже первую фамилию из вкладки Authors

![sc6](image/6.png)

Задание 7

Update Manager используют обычно для обновления установленных программ,для обновления всей системы до новой версии,дляобновления ссылок в Software Center

![sc7](image/7.png)

Задание 8

Синонимы командной строки являются- терминал, консоль 

![sc8](image/8.png)

Задание 9

Команда pwd напечатает в какой директории мы сейчас находимся 

![sc9](image/9.png)

Задание 10

Команды эквиваленты команде ls -A --human-readable -l /some/directory
Сами команды: 1)ls --human-readable -A -l/some/directory , 2) ls --almost-all --human-readable -l /some/directory 

![sc10](image/10.png)

Задание 11

Команды которые выведет содержимое /home/bi/Downloads
1)ls ./../Downloads
2)ls ~/Downloads
3)ls ../Downloads
4)ls /home/bi/Downloads

![sc11](image/11.png)

Задание 12

Команда  rm -r используется для удаления директорий 

![sc12](image/12.png)

Задание 13

Если ввести команду firefox а затем  exit, никто не закроется 

![sc13](image/13.png)

Задание 14

Команда & эквивалентна запуску Ctrl+z,bg

![sc14](image/14.png)

Задание 15

Сначала скачиваем файл,затем открываем его и копируем что в нем выведется

2023-11-15 14:30:45
Control sum: 1234

![sc15](image/15.png)

Задание 16

По умолчанию поток ошибок выводится из программ на экран 

![sc16](image/16.png)

Задание 17

Команды program 2>> file.txt,program 2> file.txt создадут файл и запишут в них program

![sc17](image/17.png)

Задание 18

Сообщения об ошибках программ, которые объединены в конвейр(pipe) выведутся на экран 

![sc18](image/18.png)

Задание 19

После следующих команда cd /home/alex/
wget -P /home/alex/Pictures -O 1.jpg http://example.com/example.jpg
картинка окажется в /home/alex/1.jpg

![sc19](image/19.png)

Задание 20

Чтобы не выводилась никаких сообщений на экран надо указать вот такую опцию:-q и -quiet

![sc20](image/20.png)

Задание 21

После запуска  wget -r -l 1 -A jpg и передачи аргумента ссылки на эту веб-страницу будут скачены jpg html файлы, но все будут html удалены 

![sc21](image/21.png)

Задание 22

Файлы отличаються gzip и zip, тем что gzip удаляет архив после его распоковки 

![sc22](image/22.png)

Задание 23

Из перечисленных программ-архиваторов могут создать архив из директории файлов zip и tar

![sc23](image/23.png)

Задание 24

Чтобы запаковать файл my_archive.tar.bz2 командой  -cjf

![sc24](image/24.png)

Задание 25

Маска *.jpg , *.? , alexey.* не гайдут файл alexey.jpeg

![sc25](image/25.png)

Задание 26

Команда grep "world" text.txt выведет на экран 
1) The beautifulworld is not enought
2)The beatiful-world is not enought
3)world
4) The "world" is not enoght
5) The "world" is not enoght

![sc26](image/26.png)

Задание 27

После скачивания архива генерируем файл в котором будут все строчки из этих произведений содержащие "love"

![sc27](image/27.png)


# Выводы

Я прошел первую часть внешнего курса stepik

