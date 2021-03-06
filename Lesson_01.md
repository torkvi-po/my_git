# Инструкция по работе с GIT

Привет. Эту инструкция я пишу не столько для отчета, сколько для себя. Потому что это надо мне)) 

***Ставлю себе вопросы, на которые надо будет ответить через полгода:***

1. Ты начал наконец-то использовать git? 
2. Ты начал использовать git в команде на всех проектах?
3. Ты пишешь команды через консоль или через IDE?

Ну если ты вдруг забыл всё, то еще раз прочитай про **Markdown**. Вроде это не так страшно. Да вообще это год преодоления себя и возвращения к тому, что ты не хотел изучать в последние годы и попытки наверстать безнадежное отставание в этих сферах, языках и технологиях.

## Работа с Git

### Проверка установлен ли GIT
    git --version

Мой результат:

    po@MacBook-Air-Pavel GIT_01 % git --version 
    git version 2.23.0

### Изменение данных
    git config --global user.name "Pavel Ivanou"
    git config --global user.email "torkvi@gmail.com"

### Инициализация

И так. Для начала надо инициализировать хранилище. Для этого используется команда 
    
    git init

Пример:

    po@MacBook-Air-Pavel GIT_01 % git init
    Initialized empty Git repository in /Users/po/Desktop/GB/GIT_01/.git/

### Добавление файла в хранилище

После этого нам надо добавить файл в хранилище. 

    po@MacBook-Air-Pavel GIT_01 % git add Lesson_01.md

### Проверка всё ли у нас получилось

    po@MacBook-Air-Pavel GIT_01 % git status
    On branch master

    No commits yet

    Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
    new file:   Lesson_01.md

### Добавление изменения в хранилище

Ну и наконец-то мы можем добавить наши изменения! Закоммитить!))

    git commit -m "Первый пошел!"

Результат:

    po@MacBook-Air-Pavel GIT_01 % git commit -m "Первый пошел!"
    dquote> go 
    dquote> "
    [master (root-commit) 35e2177] Первый пошел go
     1 file changed, 23 insertions(+)   
    create mode 100644 Lesson_01.md
    po@MacBook-Air-Pavel GIT_01 % 
    
Здесь у меня пошел многострочный комментарий, хотя я вроде закрыл двойную кавычку.

## Работа с ветками

Команда **git branch** показывает какие ветки есть. 
    
    git branch
    po@MacBook-Air-Pavel GIT_01 % git branch
    * Second
    master

Чтобы переходить между ветками используем **git checkout ...**

    po@MacBook-Air-Pavel GIT_01 % git checkout Second
    Switched to branch 'Second'

## Слияние веток

Для слияния веток переходим в ветку **master** - **git checkout master** и используем команду **git merge** 


    po@MacBook-Air-Pavel GIT_01 % git checkout master
    Switched to branch 'master'
    Your branch is up to date with 'origin/master'.
    po@MacBook-Air-Pavel GIT_01 % git merge Second
    Updating 327420d..fcaa2e7
    Fast-forward
     Lesson_01.md | 15 ++++++++++++++-
     1 file changed, 14 insertions(+), 1 deletion(-)
    po@MacBook-Air-Pavel GIT_01 % 

# Проверка на конфликты

Помни! Если сразу во всех ветках вести изменения, то могут возникнуть конфликты!

    *!надо потом еще потренироваться!*
Можно создавать много веток

А можно всё лупить в master если ты работаешь один и ты не ошибаешься))

### Удаление ветки

Для этого надо **git branch -D branch_name**

    po@MacBook-Air-Pavel GIT_01 % git branch -D new
    Deleted branch new (was 8f7b5cf).

### Дополнительная информация

Пишу себе, чтобы не забыть откуда черпал информацию.

1. [Полная информация по языку разметки Markdown](https://www.markdownguide.org/basic-syntax/)

---

2. [![Наш любимый и незаменимый Google. Yandex -- держим за тебя кулачки!](/googlelogo_color_272x92dp.png "Наш любимый и незаменимый Google. Yandex -- держим за тебя кулачки!")](https://www.google.com)

3. Markdown: Open Preview to the Side command (⌘K V).
