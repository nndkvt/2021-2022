---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе №6"
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

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство
с технологией SELinux.
Проверить работу SELinux на практике совместно с веб-сервером Apache.

# Выполнение лабораторной работы

За кадром:

![Установка httpd](image/download/Screenshot_1.png){width=70%}

![Строка ServerName](image/download/Screenshot_2.png){width=70%}

![Изменение прав доступа для перезаписи ServerName](image/download/Screenshot_3.png){width=70%}

![Перезапись ServerName](image/download/Screenshot_4.png){width=70%}

![Возвращаем изначальные права доступа](image/download/Screenshot_5.png){width=70%}

![Разрешение на INPUT и OUTPUT](image/download/Screenshot_6.png){width=70%}

Выполнение работы:

![](image/complete/Screenshot_1.png){width=70%}

![](image/complete/Screenshot_2.png){width=70%}

Отсюда видим, что контекст Apache - system_u:system_r:httpd_t:s0

![](image/complete/Screenshot_3.png){width=70%}

![](image/complete/Screenshot_4.png){width=70%}

![](image/complete/Screenshot_5.png){width=70%}

![](image/complete/Screenshot_6.png){width=70%}

![](image/complete/Screenshot_7.png){width=70%}

В папке www не было файлов, только две директории: http и cgi-bin.

Создание файлов в папке html доступно только пользователю root.

![](image/complete/Screenshot_8.png){width=70%}

![](image/complete/Screenshot_9.png){width=70%}

![](image/complete/Screenshot_10.png){width=70%}

![](image/complete/Screenshot_11.png){width=70%}

При попытке изменить порт с 80 на 81 не было ошибок. При дальнейшем выполнении
лабораторной станет понятно, что дело в обновленной политике. Для демонстрации
ошибки изменил порт с 81 на 82.

![](image/complete/Screenshot_12.png){width=70%}

"Порт tcp/81 определен на уровне политики" - об этом недопонимании говорилось
ранее.

# Выводы

В результате выполнения работы мы познакомились с SELinux и развили навыки
администрирования ОС Linux.
