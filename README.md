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

```
git add terraform/.gitignore README.md

git commit -m "Added gitignore"

echo "will_be_deleted" > will_be_deleted.txt

echo "will_be_moved" > will_be_moved.txt

git add will_be_deleted.txt will_be_moved.txt

git commit -m "Prepare to delete and move"

git rm will_be_deleted.txt

git mv will_be_moved.txt has_been_moved.txt

git commit -m "Moved and deleted"

git log --oneline
```

    acffc6a (HEAD -> main) Moved and deleted
    663b874 Prepare to delete and move
    242d658 Added gitignore
    0d6c3f2 First commit
    eb81a32 (origin/main, origin/HEAD) Initial commit

```
git add README.md

git push
```

https://github.com/awakehns/devops-netology



# Домашнее задание к занятию "`Основы Git`" - `Демин Герман`

### Задание 1. Знакомимся с GitLab и Bitbucket

Создан репозиторий gitlab

![createlab](/img/createlab.png)

Добавлен ssh ключ gitlab

![ssh](/img/ssh.png)

```
git remote -v
```

    origin  git@github.com:awakehns/devops-netology.git (fetch)
    origin  git@github.com:awakehns/devops-netology.git (push)

```
git remote add gitlab git@gitlab.com:awakehns/devops-netology.git

git push -u gitlab main

git remote -v
```

    gitlab  git@gitlab.com:awakehns1/devops-netology.git (fetch)
    gitlab  git@gitlab.com:awakehns1/devops-netology.git (push)
    origin  git@github.com:awakehns/devops-netology.git (fetch)
    origin  git@github.com:awakehns/devops-netology.git (push)

Изменена видимость проекта на "Public"

![visible](/img/visible.png)



### Задание 2. Теги

```
git tag v0.0

git push origin v0.0

git push gitlab v0.0
```

    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    To github.com:awakehns/devops-netology.git
    * [new tag]         v0.0 -> v0.0
    
    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    To gitlab.com:awakehns1/devops-netology.git
    * [new tag]         v0.0 -> v0.0

Запушен легковесный тег v0.0

![hubv0.0](/img/hubv0.0.png)

![labv0.0](/img/labv0.0.png)
    
```
git tag -a v0.1 -m "Version 0.1"
git push origin v0.1
git push gitlab v0.1
```

    Перечисление объектов: 1, готово.
    Подсчет объектов: 100% (1/1), готово.
    Запись объектов: 100% (1/1), 160 байтов | 160.00 КиБ/с, готово.
    Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    To github.com:awakehns/devops-netology.git
    * [new tag]         v0.1 -> v0.1

    Перечисление объектов: 1, готово.
    Подсчет объектов: 100% (1/1), готово.
    Запись объектов: 100% (1/1), 160 байтов | 160.00 КиБ/с, готово.
    Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    To gitlab.com:awakehns1/devops-netology.git
    * [new tag]         v0.1 -> v0.1

Запушен легковесный тег v0.1

![hubv0.1](/img/hubv0.1.png)

![labv0.1](/img/labv0.1.png)



### Задание 2. Теги

```
git log --oneline
```

    92459ba (HEAD -> main, tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab/main) .
    db71280 .
    acffc6a Moved and deleted
    663b874 Prepare to delete and move
    242d658 Added gitignore
    0d6c3f2 First commit
    eb81a32 Initial commit

```
git checkout 92459ba

git switch -c fix

git push -u origin fix
```

    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    remote: 
    remote: Create a pull request for 'fix' on GitHub by visiting:
    remote:      https://github.com/awakehns/devops-netology/pull/new/fix
    remote: 
    To github.com:awakehns/devops-netology.git
    * [new branch]      fix -> fix
    branch 'fix' set up to track 'origin/fix'.

```
git add README.md

git commit -m "Updated README in fix branch"

git push
```

    Перечисление объектов: 5, готово.
    Подсчет объектов: 100% (5/5), готово.
    При сжатии изменений используется до 8 потоков
    Сжатие объектов: 100% (3/3), готово.
    Запись объектов: 100% (3/3), 1.23 КиБ | 1.23 МиБ/с, готово.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    To github.com:awakehns/devops-netology.git
        92459ba..e89a6dd  fix -> fix

Изменения на странице https://github.com/awakehns/devops-netology/network

![graph](/img/graph.png)



### Задание 4. Упрощаем себе жизнь

Открыт проект в PyCharm IDE

![IDE](/img/IDE.png)

Сделаны два коммита через IDE

![IDEcommit2](/img/IDEcommit2.png)
