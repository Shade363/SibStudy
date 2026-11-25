# Отчёт лабораторной работы №9

1) Использую git status для проверки текущей ветки и git log для просмотра действий:
![Текущая ветка main выведенная git status, изменения показанные командой git log](scrshots/status.png)

2) Создам функцию сортировки и снова проверю git status:
![git status после добавления функции сортировки:](scrshots/status2.png)
 
3) Добавлю файл в stage и проверю git status:
![git status после git add sort.c](scrshots/sortstage.png)

4) Выполню commit и проверю git status:
![git status после завершения коммита](scrshots/commit1.png)

5) Добавлю комментарий в sort.c и проверю git status:
![git status после добавления комментария](scrshots/comment1.png)

6) Добавлю изменение файла и проверю git status:
![git status после второго добавления изменения](scrshots/stage2.png)

7) Добавлю еще один комментарий в файл и выполню коммит:
![commit после изменения файла без добавления изменений](scrshots/commit2.png)

8) Посмотрю как сейчас выглядит git status и log:
![git status после совершения коммита](scrshots/status3.png)
![git log после совершения коммита](scrshots/log1.png)

9) Добавлю в изменения второй комментарий и сделаю коммит, после чего запушу на гитхаб:
![Добавление изменения, коммит и пуш на main](scrshots/pushsort.png)

## ВЕТКИ

1) Создам новую ветку mybranch и посмотрю список всех веток:
![git branch mybranch и git branch](scrshots/mybranchmade.png)

2) Посмотрю, как изменяется git status при переключениями между ветками:
![git status в main, git switch mybranch с git status после](scrshots/status4.png)
В строке вывода On branch main изменилось на On branch mybranch

3) Удостоверюсь, что нахожусь на ветке mybranch, после чего file1.txt со своим именем, затем добавлю файл в изменения и выполню коммит:
![git branch, проверка показывает * mybranch, командой echo с перенаправлением вывода создаю файл с именем внутри, добавляю его в изменения и выполняю коммит](scrshots/newfile1.png)

4) Использую git log --oneline --graph, чтобы увидеть, что наша ветка
указывает на новый коммит, после переключусь на ветку main и использую вышеупомянутю команду снова:
![git log --oneline --graph на ветке mybranch, переключение на main и повторение git log --oneline --graph](scrshots/loggraph.png)
Заметим, что в графе ветки main отсутствует последний коммит с файлом file1.txt

5) Создам новый файл file2.txt и закоммитчу его, после использую команду git log --oneline --graph чтобы убедиться в последнем коммите. Далее, переключусь на ветку mybranch:
![touch file2.txt, add and commit, git log graph, switch to mybranch](scrshots/newfile2.png)
Заметим, что при переходе на другую ветку пропал файл file2.txt, но зато появился file1.txt

6) Наглядно сравню ветки используя git diff:
![сравнение mybranch и main с импользованием git diff](scrshots/gitdiff.png)

7) Добавлю текстовый документ со скриншотами в mybranch, сделаю коммит и пуш этой ветки:
![добавление скриншотов и текстового документа, коммит и пуш ветки mybranch](scrshots/commitmybranch.png)

8) Запушу изменения ветки main, после, удостоверюсь что на github.com лежат обе ветки:
![пуш изменений main]()