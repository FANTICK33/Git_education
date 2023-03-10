![Git_images](Git_images.png)
# __Знакомство с Git.__

> ## __Содержание:__
* Что такое контроль версий и зачем он нужен.
* Git - программа для контроля версий.
* Команды Git.
* Создание Git-репозитория.
* Зачем нужны ветви.
* Работа с черновиками.
* Совмещение двух вариантов текста.
* Удаление веток.
* Добавление изображения.
* Конфликт изменений.
* Визуализация всех веток.


##  __Что такое контроль версий и зачем он нужен.__

### __Контроль версий (контроль исходного кода)__ — практика, которая позволяет отслеживать
изменения исходного кода и управлять ими.

__Рассмотрим практическую задачу.__

> Мы создали сайт, он работает, пользователи не испытывают проблем. Но прошло время и мы
решили изменить функциональность. Прежде чем вносить изменения, сохраняем рабочую версию
сайта на компьютере или сервере. Это будет архив «Рабочая версия нашего сайта». Спустя время
появляется еще одна версия нашего сайта, допустим, 2.0. При возникновении проблем всегда
можно откатиться до первой версии и запустить сайт заново.
### _Контроль версий необходим, чтобы:_
* _хранить разные версии проекта;_
* _возвращаться к разным версиям проекта._

_Примеры: версии сайтов (по датам) и документов._

Хранение версий сводится к созданию копий информации на компьютере или сервере.
Функцию возврата реализуют за счёт восстановления предыдущих версий.

Таким образом, __система контроля__ — это реализованная возможность замены информации
с использованием сохраненных версий.

>Когда вы работаете в команде, контроль версий помогает синхронизировать усилия.

### __Примеры использования контроля версий в жизни:__
 * Написание нескольких версий одного текста.

 * Сохранение в компьютерных играх.

>(Если вы сделали что-то неправильно, вы всегда можете вернуться к состоянию, когда вас всё устраивало).

 * Группа сотрудников пишет текст в течение
нескольких дней.

>(Когда готов первый черновик, его
отправляют на ревью коллеге. Пока он
читает, другие сотрудники продолжают
работу над текстом).

## __Git - программа для контроля версий.__

В программировании проблемы совместной
работы над проектами возникли ещё до
появления облачных сервисов.

>__Git__ — самая популярная система контроля
версий, но не единственная. Алгоритм
работы подобных систем схож.

Программа Git берёт на себя контроль версий
проекта и позволяет переключаться между
ними. Обратите внимание: Git хранит __не файлы целиком, а отличия между ними__. Это позволяет экономить память. Автор программы — Линус Торвальдс, создатель ОС Linux.

## __Команды Git.__

Осваивать Git проще процессе редактирования текстовых файлов. Markdown – язык разметки,
который позволяет форматировать текст. Для написания в редакторе VS Code используется
синтаксис языка.

Все команды задаём при помощи написания кода в терминале.

Прежде чем создавать репозиторий и инициализировать Git, проверим текущую установленную
версию пограммы. Для этого в терминале введём команду:
* __git --version__

Если Git установлен на компьютер, вы увидите его текущую версию.

Программа использует мнемонические команды, которые легко запомнить, если знать английский язык.

* __git log__ — вызывать список действий и сохранений,
* __git init__ — создать репозиторий в папке на локальной машине,
* __git add__ — отслеживать добавленные файлы,
* __git commit + комментарий__ — сохранить текущее состояние,
* __git diff__ — показать разницу между версиями,
* __git chechout__ — переключиться между разными версиями.

## __Создание Git-репозитория.__


* Берём локальный каталог, который не
находится под версионным контролем,
и превращаем его в репозиторий.
* Клонируем существующий репозиторий
из любого места.

>Чтобы вызвать ранее введённую команду,
пользуемся стрелками на клавиатуре.
Перебираем недавно введённые команды
нажатием стрелки «вверх».

__Команда git init__

* Инициализация: указываем папку, в которой
git начнёт отслеживать изменения
* В папке создаётся скрытая папка .git

__Команда git status__

* Показывает текущее состояние гита, есть
ли изменения, которые нужно закоммитить
(сохранить)


__Команда git add__
* добавляет содержимое рабочего каталога в индекс (staging area) для последующего коммита. Эта команда дается после добавления
файлов. Писать название целиком не обязательно: терминал дозаполнит данные автоматически.

__Команда git commit__
* зафиксировать или сохранить

По умолчанию git commit использует лишь этот индекс, так что вы можете использовать git add для сборки слепка вашего следующего коммита.
Команда git commit берёт все данные, добавленные в индекс с помощью git add, и сохраняет их
слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.

__Команда git log__
* Журнал изменений
* Перед переключением версии файла в Git
используйте команду git log, чтобы увидеть
количество сохранений
> Нажатие клавиши ‘q’ возвращает в исходное окно терминала.

__Команда git checkout__
* Переключение между версиями.
* Для работы нужно указать не только интересующий вас коммит, но и вернуться в тот, где работаем, при помощи команды

__Команда git diff__

* Показывает разницу между текущим файлом
и сохранённым
* Перед переключением версии файла в Git
используйте команду git log, чтобы увидеть
количество сохранений

>Git отслеживает файлы по имени!
>
>Если изменить имя файла, необходимо добавить файл с новый именем + git commit


## __Зачем нужны ветви.__

>Ветки позволяют легко управлять черновиками и чистовиками в Git.

Например, преподаватель создает для второй
лекции рабочую папку с названием lesson 2. Во
время лекции он пишет инструкцию для
Markdown, а затем вызывает команды __git init, git
stasus, git add, git commit.__

Работу с ветками начинаем с запуска Git в репозитории.

* Вводим __git init__ и __git status__, чтобы убедиться,
что репозиторий создан.
* Повторяем команды __git add, git log,
git status.__

Затем преподаватель вносит изменения в
редактируемый файл и дает команду git commit.

## __Работа с черновиками.__

## __Совмещение двух вариантов текста.__

>git branch

Если у нас несколько версий черновика, мы
можем вывести на экран ветку, где находимся,
командой git branch.

Создать ветку можно командой git branch.
Делать это надо в папке с репозиторием:
* git branch <название новой ветки>

Во время работы у нас будет ветка master с
черновиком и отдельная ветка — с чистовиком.

Если потребуется переключиться с одной ветки
на другую, вызовем команду git checkout <имя
ветки>

Команда git log покажет состояние более новых
версий проекта. Но если вызвать эту команду из
самой «свежей» ветки, мы не увидим исходного
файла.

Когда мы правим текст/код в текущей ветке,
автоматического слияния не происходит: можно
создавать один документ в разных версиях
в разных ветках.

Допустим, черновики нас полностью устраивают и нам нужно внести изменения, чтобы
информация появилась в чистовике. Для этого есть команда git merge.
## __Удаление веток.__

>git merge

Чтобы слить любую ветку с текущей, вызываем
__git merge__ <имя ветки для слияния с текущей>

После всех изменений дерево версий принимает следующий вид:


## __Добавление изображения.__

Если ветка text formatting больше не нужна, ее можно удалить

> __git branch -d__ <имя ветки для удаления>
Добавим изображение в файл-инструкцию

Чтобы вставить изображение в текст, достаточно написать следующее![Араратская_гора](Араратская_гора.jpg)
В Git не принято добавлять файлы
изображений, их хранят на сторонних
носителях. Чтобы исключить ненужные файлы
из загрузки, есть команда git ignore.

## __Конфликт изменений.__
При работе в двух ветках одновременно может
возникнуть ситуация, когда в одной и другой
ветке мы по-разному изменили блок текста.
Если затем мы попробуем слить эти ветки, Git
сообщит о конфликте и предложит выбрать,
какие же изменения записать.

Поэтому у проекта в репозитории должен быть один
ответственный пользователь, наделённый правом проводить
слияния и разрешать конфликты
## __Визуализация всех веток.__


* __git log --graph__

Ключ -graf в связке с командой log позволяет отобразить коммиты в виде дерева.
