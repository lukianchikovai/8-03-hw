# Домашнее задание к занятию "Git" - Юлия Лукьянчикова


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw): done (https://github.com/lukianchikovai/8-03-hw)
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`: done
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя: done
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

1. Зарегистрируйте аккаунт на GitHub - done
2. Создайте новый отдельный публичный репозиторий. Обязательно поставьте галочку в поле «Initialize this repository with a README» - done
3. Склонируйте репозиторий, используя https протокол git clone - done
4. Перейдите в каталог с клоном репозитория - done
5. Произведите первоначальную настройку Git, указав своё настоящее имя и email: `git config --global user.name` и `git config --global user.email johndoe@example.com` - done
6. Выполните команду `git status` и запомните результат - done

```On branch main 
Your branch is up to date with 'origin/main'.
```

7. Отредактируйте файл README.md любым удобным способом, переведя файл в состояние Modified - done
8. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага - done

```On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")"
```

9. Посмотрите изменения в файле README.md, выполнив команды `git diff` и `git diff --staged - done`

`git diff`: вывод подсвечивает все изменения в файле README.md
`git diff --staged`: пустой вывод

10. Переведите файл в состояние staged или, как говорят, добавьте файл в коммит, командой `git add README.md` - done
11. Ещё раз выполните команды `git diff` и `git diff --staged` - done

`git diff`: пустой вывод
`git diff --staged`: вывод подсвечивает все изменения в файле README.md


`get status`:

```
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
```

12. Теперь можно сделать коммит `git commit -m 'First commit'` - done


13. Сделайте `git push origin main` - done 

[Ссылка на этот коммит в md-файле с решением](https://github.com/netology-code/sys-pattern-homework/commit/ecfeaa8)

---

### Задание 2

1. Создайте файл .gitignore (обратите внимание на точку в начале файла) и проверьте его статус сразу после создания.

```Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
```

2. Добавьте файл .gitignore в следующий коммит `git add`

```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore
```
3. Напишите правила в этом файле, чтобы игнорировать любые файлы `.pyc`, а также все файлы в директории `cache`.

```
# Ignore .pyc files
*.pyc

# Ignore all files within a 'cache' directory
cache/

```

4. Сделайте коммит и пуш - done

[Ссылка на этот коммит в md-файле с решением](https://github.com/netology-code/sys-pattern-homework/commit/cd5c8a99f7742d9f4ca3570b01794c79c9f65c89)

---

### Задание 3

1. Создайте новую ветку dev и переключитесь на неё

```
git checkout -b dev

```

2. Создайте в ветке `dev` файл `test.sh` с произвольным содержимым - done
3. Сделайте несколько коммитов и пушей в ветку `dev`, имитируя активную работу над файлом в процессе разработки - done
4. Переключитесь на основную ветку

```
git switch main

```
5. Добавьте файл `main.sh` в основной ветке с произвольным содержимым, сделайте комит и пуш . Так имитируется продолжение общекомандной разработки в основной ветке во время разработки отдельного функционала в `dev` ветке - done
6. Сделайте мердж `dev` ветки в основную с помощью `git merge dev`. Напишите осмысленное сообщение в появившееся окно комита - done

```
Merge made by the 'ort' strategy.
Merge made by the 'ort' strategy.
 README.md | 71 ++++++++++++++++-------------------------------------------------------
 test.sh   |  3 +++
 2 files changed, 19 insertions(+), 55 deletions(-)
 create mode 100644 test.sh

```

7. Сделайте пуш в основной ветке - done
8. Не удаляйте ветку `dev` - done

[Ссылка на граф коммитов `https://github.com/ваш-логин/ваш-репозиторий/network` в md-файле с решением](https://github.com/lukianchikovai/8-03-hw/network)
