---
## Front matter
lang: ru-RU
title: Презентация по четвертой лабораторной. Предмет - Информационная безопасность.
author: |
	Попов Олег Павлович\inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
date: 2021, 18 Сентября -- 18 Сентября

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
mainfont: DejaVuSerif
romanfont: DejaVuSerif
sansfont: DejaVuSans
monofont: DejaVuSansMono
---

# Выполнение лабораторной

## Выполнеине команд

После создания файла file1 начинаем выполнять лабораторную:

![](image/Screenshot_1.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_2.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_3.png){width=%50}

## Выполнение лабораторной

Как мы видим, при задании атрибутов a и i взаимодействие с файлом через
обычного пользователя не представляется возможным, так как атрибут a -
это атрибут append only, то есть в файл можно добавлять информацию, но
нельзя удалять, переписывать, переименовывать и так далее. Атрибут i же
запрещает любые взаимодействия с файлом.
