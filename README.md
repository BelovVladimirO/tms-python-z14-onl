# TMS-python-spring
Курс Python разработчик

## Как добавить домашку?
1. Скачиваем проект
```
git clone https://github.com/v-rolich/tms-python-z14-onl.git
```
или (если сделали fork репозитория)
```
git clone https://github.com/<your_username>/tms-python-z14-onl.git
```
2. Переключаемся на ветку <i>master</i>
```
git checkout master
```
3. Скачиваем последние изменения ветки <i>master</i> 
```
git pull origin master
```
4. Создаем ветку для домашнего задания
```
git checkout -b your_name_and_lesson_number
```
или 
```
git branch your_name_and_lesson_number
git checkout your_name_and_lesson_number
```
Например, 
``` git checkout -b rolich-3```

5. Выполняем домашнее задание или копируем уже готовое в папку **src/**

6. Фиксируем созданные файлы в git
```
git add .
```
или
```
git add src/filename.py
```
или (добавить все .py файлы)
```
git add src/*.py
```
7. Коммитим (добавляем комментарий) выполненные задания 
```
git commit -m "HW<NO>: Name LastName"
```
Например, ``` git commit -m "HW1: Vladimir Rolich"```

8. После выполнения домашнего задания, публекуем командой 
```
git push origin your_name_and_lesson_number
```
или (если хотите перетереть старые изменения)
```
git push origin -f your_name_and_lesson_number
```
9. Создаем Pull Request (отправляем домашку на проверку)

## Что делать если предыдущая домашка остается на ветке?

1. Добавляете ссылку исходного репозитория
```
git remote add upstream https://github.com/v-rolich/tms-python-z14-onl.git
```
2. Создаете временную ветку
```
git checkout -b tmp-branch
```
3. Удаляете master
```
git branch -D master
```
4. Качаете кэш веток с исходного репозитория
```
git fetch upstream
```
5. Переключаетечь на master с исходного репозитория
```
git checkout upstream/master
```
6. Создаем ветку master локально
```
git checkout -b master
```
7. Пункты от 4-ого до конца из раздела **Как добавить домашку?**

## Что делать если не могу запушить?
1. нужно изменить ссылку локальную
```
git remote set-url origin https://github.com/<your_username>/tms-python-z14-onl.git
```
2. Проставить свои данные
```
git config --global user.name <YOUR_NICKNAME>
git config --global user.email <YOUR_EMAIL>
```

## Как исправить ошибку squash commits
1. Если хотите склеить **2** коммита
```
git rebase -i HEAD~2
```
