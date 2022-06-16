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

### Дополнительная информация

Пишу себе, чтобы не забыть откуда черпал информацию.

1. [Полная информация по языку разметки Markdown](https://www.markdownguide.org/basic-syntax/)

---

2. [![Наш любимый и незаменимый Google. Yandex -- держим за тебя кулачки!](/googlelogo_color_272x92dp.png "Наш любимый и незаменимый Google. Yandex -- держим за тебя кулачки!")](https://www.google.com)

3. Markdown: Open Preview to the Side command (⌘K V).
