---
## Front matter
lang: ru-RU
title: Презентация по пятой лабораторной. Предмет - Информационная безопасность.
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

Компилятор gcc был установлен за кадром с помощью команды: yum install gcc.

![](image/Screenshot_1.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_2.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_3.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_4.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_5.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_6.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_7.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_8.png){width=%50}

## Выполнение лабораторной

Теперь переходим к части со Sticky bit.

![](image/Screenshot_9.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_10.png){width=%50}

## Выполнение лабораторной

![](image/Screenshot_11.png){width=%50}

## Выполнение лабораторной

В итоге получается, что у пользователей вне группы guest есть права на
запись и чтение файла, но при этом, если у директории tmp есть Sticky
bit, удаление file01 запрещено.
