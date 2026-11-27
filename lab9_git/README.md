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

### ВЕТКИ

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
![пуш изменений main](scrshots/pushmain.png)

![наличие обоих веток на гитхабе](scrshots/githubbranches.png)

## Оценка 4

1) Переключусь на ветку mybranch, добавлю в sort.c функцию main с массивом чисел и применю для него функцию сортировки. После, проверю вывод команды git diff, а также вывод diff --staged:
![Результат работы git diff описывающий изменения в sort.c](scrshots/sortwithmain.png)

![Пустой вывод git diff --staged](scrshots/diffstaged1.png)

2) Добавлю sort.c в staged, после снова проверю вывод git diff и git diff --staged:
![Вывод git diff после добавления sort.c в staged](scrshots/gitdiff2.png)

![Вывод git diff --staged после добавления sort.c в staged](scrshots/diffstaged2.png)

3) Удалю одно число из массива в sort.c, после снова проверю git diff и git diff --staged:
![git diff после удаления числа](scrshots/gitdiff3.png)

![git diff --staged после удаления числа](scrshots/diffstaged3.png)

git diff сравнивает текущее состояние с staged, а git diff --staged сравнивает staged с последним commit.

4) Запущу git status:
![git status, в котором два sort.c, в changes to be commited, и в changes not staged to commit](scrshots/status5.png)

Действительно, видим в выводе sort.c дважды.

5) Запущу git restore --staged sort.c для отмены индексации, и снова проверю git status:
![git status, теперь без вкладки changes to be commited](scrshots/gitrestore.png)

6) Индексирую изменение и совершаю коммит, после проверю журнал:
![git log --oneline с последним коммитом add main to sort.c](scrshots/sortcommitmain.png)

7) Добавлю printf(“hello git\n”) в sort.c, посмотрю его содержиое и проверю git status:
![содержимое sort.c с помощью cat](scrshots/cat1.png)

![ и вывод git status](scrshots/status6.png)

8) Запущу git restore sort.c, посмотрю содержимое файла и проверю статус, после чего запушу ветку на репо:
![содержимое sort.c после git restore](scrshots/cat2.png)

![git status после git restore](scrshots/status7.png)

![пуш на репо](scrshots/mybranchpush.png)

### Ветки и ff-merge

1) Создам файл greeting.txt, проиндексирую его и закоммитчу с
сообщением “Add file greeting.txt”. После добавлю в него слово hello, снова индексирую и коммитчу с текстом "Add content to greeting.txt":
![создание файла с помошью touch, индексирование, коммит, затем добавление hello с помощью перенаправления вывода echo и последующие шаги те же самые](scrshots/greeting.png)

2) Создам новую ветку feature/uppercase, переключусь на неё и проверю git status:
![git branch, git switch, и git status](scrshots/status8.png)

3) Отредактирую файл greeting.txt, индексирую и закомитчу его, посмотрю git branch и git log --oneline --graph --all:
![замена содержимого greeting.txt echo с перенаправлением вывода, индексирование, коммит, текущая ветка feature/uppercase и граф всех веток lab9_git](scrshots/bigloguppercase.png)

4) Переключусь на главную ветку, посмотрю содержимое greeting.txt, сравню ветки и объединю их, и снова посмотрю содержимое файла:
![Переключение веток, содержимое greeting.txt (файл в ветке отсутствует), сравнение веток](scrshots/diffmainupprcase.png)

![Слияние веток](scrshots/merge.png)

![просмотр файла после слияния](scrshots/HELLO.png)

5) Удаляю ветку feature/uppercase, мерджу mybranch в main, посмотрю вывод git log --oneline --graph --all:
![Удаление ветки с верхим регистром, слияние mybranch в main (already up to date), граф веток на текущий момент](scrshots/mybranchmerge.png)

6) Выполняю пуш ветки и документа на репо:
![Индексирование изменений, коммит и последующий пуш на репо](scrshots/lastpush.png)

## Оценка 5

1) Создам ветку branch1 и переключусь рна неё, после выполню команду echo "This is a relevant fact" > file.txt и закоммитчу это изменение:
![Создание новой ветки и переключение на неё, создание файла file.txt путем перенаправления вывода echo, последующее индексирование и коммит](scrshots/branch1.png)

2) Переключусь на главную ветку и выполню команду echo "This is an indispensable truth!" > file.txt, следом сделаю коммит:
![переключение на main, создание файла file.txt путем перенаправления вывода echo, последующее индексирование и коммит](scrshots/mainfile.png)

3) Посмотрю вывод git log --oneline --graph --all:
![Вывод git log c появлением новой ветки и двумя новыми коммитами](scrshots/gitlogbranch1.png)

4) Смерджу ветку branch1 в main, проверю git status:
![неудачный git merge при котором возникает конфликт и git status, сообщающий о незавершенном слиянии и несохраненных изменениях](scrshots/mergeconflict.png)

5) Посмотрю содержимое файла file.txt и исправлю конликт, проверю git log --oneline --graph, а после запушу изменения:
![Содержимое файла в котором показан конфликт](scrshots/fileconflict.png)

![Исправление конфликта с помощью Accept current change в VS Code](scrshots/fixconflict.png)

![Вывод git log --oneline --graph после исправления конфликта](scrshots/afterconflict.png)

![Пуш изменений](scrshots/pushmain2.png)

### Merge конфликты для сортировки MergeSort на python.

1) Создам файлы base.py, righty.py, lefty.py, а после создам файл mergesort.py с содержимым base.py, проиндексирую и закоммитчу:
![Содержимое base.py, запись этого в mergesort.py, индексирование](scrshots/mergesortbase.png)

![коммит](scrshots/commitms.png)

2) Создам новую ветку Mergesort-Impl и переключусь на неё, заменяю содержимое mergesort.py на содержимое righty.py, коммит изменений:
![Создание новой ветки, переключение, замена содержимого mergesort и коммит](scrshots/rightychange.png)

3) Переключусь на main и заменю всё содержимое mergesort.py на содержимое lefty.py, после сделаю коммит:
![Переключение, замена содержимого и коммит](scrshots/leftychange.png)

4) Посмотрю вывод git log --oneline --graph и git branch. Выполню мердж Mergesort-Impl в main, исправлю все конфликты и сделаю пуш изменений в main:
![git log с последними коммитами main](scrshots/gitlogmain.png)

![git branch показывает все ветки, Mergesort-Impl включительно. На данный момент нахожусь на main](scrshots/branchnow.png)

![Конфликт при слиянии веток](scrshots/merge2.png)

![Исправляю конфликты в mergesort.py](scrshots/fixxinn.png)

![Выполнение push]