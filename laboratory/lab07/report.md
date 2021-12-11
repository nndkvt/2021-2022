---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе №7"
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

Освоить на практике применение режима однократного гаммирования.

# Выполнение лабораторной работы

Ниже представлен код консольного приложения для работы с шестнадцатеричными
кодами символов.

![](image/Screenshot_1.png){width=80%}

Выше указан main файл программы, в котором находится исключительно реализация
всех функций, написанных в файле createcode.

Порядок выполнения команд в файле main следующий: на вход программе дается
ввод mes; все символы mes обрабатываются через функцию createCode(), которая
создает массив шестнадцатеричных кодов; генерируется рандомный ключ через
функцию generateDecryptionCode(); сообщение кодируется через функцию однократного
гаммирования xor(); все вышеперечисленное выводится на экран; и под конец
сообщение xorCode дешифруется через функцию xor() [newCode] и выводится на экран.

![](image/Screenshot_2.png){width=80%}

Данный код представляет собой файл createcode. Здесь, как уже было сказано ранее,
записаны все функции.

Функция createCode(): берет на вход сообщение типа string и для каждого символа
сообщения генерирует его шестнадцатеричный код ascii.

Функция generateDecryptionCode(): создает рандомный ключ определенного размера
s.

Функция xor(): реализует "исключающее или" для code1 и code2 и выводит зашифорованное
сообщение в виде массива кодов.

Функция decryptCode(): нужна для расшифровки кодов code и вывода сообщения.
Для реализации данной функции пришлось отдельно записывать символы кириллицы и
создавать для них массив кодов, так как функция bytes.fromhex() не распознает
трехзначные шестнадцатеричные коды (все коды кириллицы трехзначные). В итоге,
функция проверяет, есть ли код в массиве кириллицы, и выводит символы.

В итоге, вывод программы выглядит так:

![](image/Screenshot_3.png){width=80%}

# Выводы

В ходе данной работы я ознакомился с однократным гаммированием и реализовал его
в приложении командной строки.
