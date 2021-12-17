---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе №8"
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

Освоить на практике применение режима однократного гаммирования
на примере кодирования различных исходных текстов одним ключом.

# Выполнение лабораторной работы

Перед реализацией новой функции в приложении нужно изучить теорию:

![](image/theory/Screenshot_1.png){width=80%}

![](image/theory/Screenshot_2.png){width=80%}

![](image/theory/Screenshot_3.png){width=80%}

![](image/theory/Screenshot_4.png){width=80%}

![](image/theory/Screenshot_5.png){width=80%}

В итоге можно сделать вывод, что расшифровать код невозможно без ключа или
одного из исходных текстов сообщений. Значит, можно реализовать функцию,
которая будет расшифровывать сообщение с помощью кодов всех сообщений и
текста одного из сообщений.

Функция:

![](image/complete/Screenshot_1.png){width=80%}

Эта функция основана на функциях, написанных в седьмой лабораторной: сначала
через xor получаем код, потом переводим сообщение в его исходный код, снова
перемножаем коды через xor и дешфруем полученный в итоге код.

Код main:

![](image/complete/Screenshot_2.png){width=80%}

Сначала на вход подаются две строки, генерируется ключ, строки шифруются через
ключ и в конце через написанную функцию переводим строки из шифрованных кодов.

Вывод:

![](image/complete/Screenshot_3.png){width=80%}

Как мы видим, из зашифрованных кодов и известного сообщения можно найти второе
сообщение.

# Выводы

В ходе данной работы я освоил на практике применение режима однократного гаммирования
на примере кодирования различных исходных текстов одним ключом.
