---
## Front matter
lang: ru-RU
title: Лабораторная работа 
subtitle: Номер 1
author:
  - Казначеев С. И.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 01 января 1970

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}

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


---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Казначеев Сергей Ильич 
  * Студент
  * Российский университет дружбы народов
  * [1132240693@pfur.ru]

:::
::: {.column width="30%"}


:::
::::::::::::::

## Цель

Установить Linux Rocky и ознакомиться с его возможностями 
## Задание 

Установить OC и выполнить домашнее задание

## Выбор диска 

Для начала назовем нашу виртуальную машину Rocky2 и выберем установочный диск

![1](image/1.png)

## Выделение памяти и процессора 

Выделяем память и процессор

![2](image/2.png)

## Выделение диска 


Выделяем размер диска (40 гб)

![3](image/3.png){#fig:003 width=70%}

## Выбор языка 

Далее выбираем язык,я выбрал русский язык

![4](image/4.png){#fig:004 width=70%}

## Настройка сети 

Выбираем диск куда устанавится система

![5](image/5.png){#fig:005 width=70%}

## Название рисунка

Настроим сеть. В качестве имени узла выберем sikaznacheev.localdomain 

![6](image/6.png)

## Настройка пользователя 

Настроим рут пользователя указав пароль для него и разрешив ему ssh

![7](image/7.png)

## Экран об окончании установки 

Настром своего пользователя согласно об именовании

![8](image/8.png)

## Установка дополнений и завершение установки 


Ждем завершения установки. По завершении перезагружаем 

![9](image/9.png)

## Завершение установки 

После установки устанавливаем дополнение гостевой ОС вот так выглядит завершение установки 

![10](image/10.png)

## Версия ядра 

Теперь выполняем домашнее задание  находим версию ядра

![11](image/11.png)

## Частота процессора

2) Частота процессора

![12](image/12.png)

## Модель процессора

3) Модель процессора

![13](image/13.png)

## Доступная память 

4) Количество доступной памяти 

![14](image/14.png)

## Гипервизор

5) Найти гипервизор

![15](image/15.png)

## Порядок монтирования 

6)Найти порядок монтирования файловых систем вместе с их типами. Тип файловой системы вероятно xfs 5 версии 


![16](image/16.png)

## Выводы

В результате выполнения лаборатоной работы была установлена система Rocky.







:::

