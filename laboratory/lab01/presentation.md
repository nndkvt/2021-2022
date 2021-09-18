---
## Front matter
lang: ru-RU
title: Презентация по первой лабораторной. Предмет - Информационная безопасность.
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

## Проблемы при выполнении

В ходе выполнения работы была обнаружена ошибка: версия CentOS, предлагаемая
для выполнения лабораторной, была устаревшей и больше не поддерживалась
создателями. Из-за этого пришлось использовать новейшую версию дистрибутива.

## Установка CentOS 8.4

Следуя указаниям в файле лабораторной нужно было создать виртуальную машину
на базе Linux Red Hat и установить для нее дистрибутив CentOS.

![Установка CentOS](image/centos.png){width=%10}

## Обновление системных файлов

После установки и запуска машины нужно было обновить системные файлы и установить
mc.

![Обновление](image/update.png){width=%25}

## Изменение Base

Чтобы Base можно было использовать, как базу для других виртуальных машин, нужно
изменить ее параметры, а именно освободить ее от соединения с собой и разрешить
множественное подключение к ней.

## Изменение Base

![Изменение атрибутов Base](image/base1.png){width=%80}

## Изменение Base

![Изменение атрибутов Base](image/base2.png){width=%80}

## Подключение Host2

Теперь мы можем создать новую виртуальную машину, которая будет "основана" на
Base.

![Подключенный Host2](image/host.png){width=%60}
