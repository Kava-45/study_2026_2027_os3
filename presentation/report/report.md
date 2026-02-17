---
## Front matter
title: "Настройка сети на базе SystemD"
subtitle: "Отчет"
author: "Казначеев Сергей Ильич "

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

# Реферат

Настройка сети на базе SystemD

# Введение

Современные операционные системы семейства Linux активно используют SystemD - систему инициализации и управления службами, пришедшую на смену традиционным  init-системам. Помимо управления службам, SystemD  включает в себя ряд подсистем, обеспечивающих настройку и управление сетевыми интерфейсами.Одним из ключевых компонентов для этих задач является systemd-networkd-демон, предназначенный для концигурарования сетей на низком уровне 


# Общие сведения SystemD

SystemD - это комплекс утилит и библиотек, предназначенных для управления процессами, службами и системными  ресурсами Linux. Он обеспечивает параллельную загрузку служб, журналирование(через journald), монтирование файловых систем и управелние сетью. Использование SystemD позволяет добиться более быстрой загрузки, лучшей управляемости и стандартизации конфигурации.

# Компоненты отвечающие за сеть 

Основными сетевыми компонентами в экосистеме SystemD являются:

1. systemd-networkd - служба, отвечающая за конфигурирование сетевых интерфейсов такие как (Ethernet,VLAN, Bording и др)
2. systemd-resolved - служба для настройки и кеширования DNS-запросов
3. networkctl - утилита для просмотра и управления сетевыми настройками 
4. udev - подсистема для автоматического обнаружения и именования сетевых устройств 


# Конфигурационные файлы systemd-networkd
 
Настройка сети с помощью SystemD осуществляется через  концигурационные файлы, размещенные в каталогах:

1. /etc/systemd/network/ - файлы пользовательских конфигураций
2. /usr/lib/systemd/network/ - системные конфигурации по умолчанию 

Основными типами являются:

1. .netdev - описание виртуальных сетевых устройств(bridge, bond, vlan и др)

	Пример .netdev (создание bridge):
	[NetDev]
	Name=br0
	Kind=bridge
	
2. .network - настройка параметров интерфейса(адресация,шлюз,DNS)

	Пример .network (настройка IP на интерфейсе):

	[Match]
	Name=eth0
	
	[Network]
	Address=192.168.1.10/24
	Gateway=192.168.1.1
	DNS=8.8.8.8
	DNS=1.1.1.1
	
3. .link - правила именования и параметров физических интерфейсов 

	Пример .link (изменение MAC-адреса):

	[Match]
	MACAddress=00:11:22:33:44:55

	[Link]
	Name=my-interface


Эти файлы позволят централизованно описывать поведение сетевых интерфейсов и обеспечивают единообразие настройки сети на разных системах 

# Типичный рабочий процесс настройки
1. Обнаружение: udev обнаруживает новое сетевое устройство.
2. Именование: Файлы .link (при наличии) переименовывают интерфейс.
3. Создание виртуальных устройств: Файлы .netdev создают bridge, bond и т.д.
4. Применение конфигурации: Файлы .network назначают IP-адреса, маршруты и DNS для соответствующих интерфейсов (сопоставление c MAC).
5. Разрешение имен: systemd-resolved обеспечивает работу DNS.

# Преимущества использования systemd-networkd

1. Централизованное управление сетевой конфигурацией
2. Логическая интеграция с другими компонентамии  SystemD
3. Минимальная зависимость от внешних утилит (в отличие от  NetworkManager)
4. Удобное применение на серверах контейнерах 

# Недостатки 

1. Более сложная конфигурация по сравнению с графическими инструментами 
2. Менее итуитивно понятно для начинающих пользователей
3. В некоторых дистрибутивах требуется отключение NetworkManager для корректной работы

# Заключение 

Использование Systemd-network и связанных инструментов позволяет системных администраторам гибко и эффективно управлять сетевой концигурацией  Linux-систем. Благодаря модульной структуре, поддержке различных типов сетей и тесной интеграции с другими сервисами SystemD, этот подход являет современным и перспективным решением для серверных и облачных инфраструктур 

# Список литературы

Arch Wiki — systemd-networkd, https://wiki.archlinux.org/title/Systemd-networkd

Debian Wiki — https://wiki.debian.org/SystemdNetworkd
