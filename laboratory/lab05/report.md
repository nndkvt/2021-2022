---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе №5"
author: "Попов Олег Павлович"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: DejaVuSerif
romanfont: DejaVuSerif
sansfont: DejaVuSans
monofont: DejaVuSansMono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучение механизмов изменения идентификаторов, применения
SetUID- и Sticky-битов. Получение практических навыков работы в консоли с
дополнительными атрибутами. Рассмотрение работы механизма
смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.

# Выполнение лабораторной работы

За кадром был установлен компилятор gcc с помощью команды:

yum install gcc

Выполнение работы:

![](image/Screenshot_1.png){width=70%}

![](image/Screenshot_2.png){width=70%}

![](image/Screenshot_3.png){width=70%}

![](image/Screenshot_4.png){width=70%}

![](image/Screenshot_5.png){width=70%}

![](image/Screenshot_6.png){width=70%}

![](image/Screenshot_7.png){width=70%}

![](image/Screenshot_8.png){width=70%}

Дальше идет часть со Sticky bit:

![](image/Screenshot_9.png){width=70%}

![](image/Screenshot_10.png){width=70%}

![](image/Screenshot_11.png){width=70%}

В итоге получается, что у пользователей вне группы guest есть права на
запись и чтение файла, но при этом, если у директории tmp есть Sticky
bit, удаление file01 запрещено.

# Выводы

В результате выполнения работы мы узнали о SetUID, SetGID и Sticky bit.
