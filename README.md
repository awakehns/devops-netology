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
git add README.git

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
