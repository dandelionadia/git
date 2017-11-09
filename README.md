# Шпаргалка по роботі з Git 

## Створення репозиторію
```
git init // ініціалізує новий локальний репозиторій
git remote add origin URL_РЕПОЗИТОРІЯ // каже локальному репозиторію синхронізуватись із репо в інтернеті (віддаленого репо)
git push -u origin master // каже даній гілці локального репо слідкувати за гілкою "master" віддаленого репо
```

## Додавання змін
```
git add НАЗВА_ФАЙЛУ // додати файл(и) до черги в наступний коміт
git commit -m 'Наказовий опис змін' // створити новий коміт із заданим описом
git push // запушити зміни у відаленний репозиторій
```

## Створення гілки
```
git checkout -b НАЗВА_ГІЛКИ // створює гілку "НАЗВА_ГІЛКИ" і переходить на неї
...етапи "Додавання змін" ОКРІМ останнього "push"
git push -u origin НАЗВА_ГІЛКИ
```
Після даних команд працюй із гілкою як "Додавання змін".
