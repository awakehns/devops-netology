# Домашнее задание к занятию "`Системы контроля версий`" - `Демин Герман`

### Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе

Создан репозиторий devops-netology

![create](/img/create.png)

Создан авторизационный токен

![token](/img/token.png)

```
git clone https://github.com/awakehns/devops-netology.git

git config --global user.name German 

git config --global user.email awake1394hns@gmail.com

git status
```

    Текущая ветка: main
    Эта ветка соответствует «origin/main».

    нечего коммитить, нет изменений в рабочем каталоге

```
git add README.md

git status
```

    Текущая ветка: main
    Эта ветка соответствует «origin/main».

    Изменения, которые будут включены в коммит:
    (используйте «git restore --staged <файл>...», чтобы убрать из индекса)
            изменено:      README.md

    Неотслеживаемые файлы:
    (используйте «git add <файл>...», чтобы добавить в то, что будет включено в коммит)
            .README.md.kate-swp
            img/

```
git diff

git diff --staged
```

    diff --git a/README.md b/README.md
    index 647b370..49a51c0 100644
    --- a/README.md
    +++ b/README.md
    @@ -1 +1,26 @@
    -# devops-netology
    \ No newline at end of file
    +# Домашнее задание к занятию "`Системы контроля версий`" - `Демин Герман`
    +
    +### Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе
    +
    +Создан репозиторий devops-netology
    +
    +![create](/img/create.png)
    +
    +Создан авторизационный токен
    +
    +![token](/img/token.png)
    +
    +```
    +git clone https://github.com/awakehns/devops-netology.git
    +
    +git config --global user.name German 
    +
    +git config --global user.email awake1394hns@gmail.com
    +
    +git status
    +```
    +
    +    Текущая ветка: main
    +    Эта ветка соответствует «origin/main».
    +
    +    нечего коммитить, нет изменений в рабочем каталоге
    :

```
git add README.md

git diff

git diff --staged

git commit -m 'First commit'

git status
```

    Текущая ветка: main
    Ваша ветка опережает «origin/main» на 1 коммит.
    (используйте «git push», чтобы опубликовать ваши локальные коммиты)

    Неотслеживаемые файлы:
    (используйте «git add <файл>...», чтобы добавить в то, что будет включено в коммит)
            .README.md.kate-swp
            img/

    индекс пуст, но есть неотслеживаемые файлы
    (используйте «git add», чтобы проиндексировать их)


```
git diff

git diff --staged
```

    Пустой вывод

```
touch .gitignore

git status
```

```
git add .gitignore
```

    Текущая ветка: main
    Ваша ветка опережает «origin/main» на 1 коммит.
    (используйте «git push», чтобы опубликовать ваши локальные коммиты)

    Изменения, которые будут включены в коммит:
    (используйте «git restore --staged <файл>...», чтобы убрать из индекса)
            новый файл:    .gitignore

    Изменения, которые не в индексе для коммита:
    (используйте «git add <файл>...», чтобы добавить файл в индекс)
    (используйте «git restore <файл>...», чтобы отменить изменения в рабочем каталоге)
            изменено:      README.md

    Неотслеживаемые файлы:
    (используйте «git add <файл>...», чтобы добавить в то, что будет включено в коммит)
            .README.md.kate-swp
            img/

```
mkdir terraform

curl -o terraform/.gitignore https://raw.githubusercontent.com/github/gitignore/master/Terraform.gitignore
```

Файл .gitignore исключает из отслеживания Git временные файлы, кэш, директории .terraform, файлы переменных и состояние инфраструктуры.
