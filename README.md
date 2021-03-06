# Шпаргалка по роботі з Git 

## Створення репозиторію
Репозиторій - це віддалена репрезентація твого проекту в інтернеті.

1. Створи нову папку локально. Використовуй лише латиницю, без пробілів.
2. Перейди у створену папку в терміналі: `cd ШЛЯХ/ДО/ПАПКИ`
3. Ініціалізуй новий локальний репозиторій:

```
git init // ініціалізує новий локальний репозиторій
git remote add origin URL_РЕПОЗИТОРІЯ // каже локальному репозиторію синхронізуватись із репо в інтернеті (віддаленого репо)
touch README.md
git add README.md
git commit -m ''
git push -u origin master // каже даній гілці локального репо слідкувати за гілкою "master" віддаленого репо
```

---

## Додавання змін
```
git add НАЗВА_ФАЙЛУ // додати файл(и) до черги в наступний коміт
git commit -m 'Наказовий опис змін' // створити новий коміт із заданим описом
git push // запушити зміни у відаленний репозиторій
```

## Створення гілки
Перед створенням нової гілки завжди переконайся ти свторюєш її із актуального `master`.
```
git checkout master // перейти на гілку мастер
git pull // підтягнути зміни з віддаленого мастеру
```
Потім, створити нову гілку:
```
git checkout -b НАЗВА_ГІЛКИ // створює гілку "НАЗВА_ГІЛКИ" і переходить на неї
...етапи "Додавання змін" ОКРІМ останнього "push"
git push -u origin НАЗВА_ГІЛКИ
```
кожна нова гілка потребую особливого першого пушу

Після даних команд працюй із гілкою як ваказано в [Додавання змін](#Додавання-змін).

Коли робота в гілці завершена, запевнись, що твоя гілка [актуалізована відповідно до тепершнім мастером](#Актуалізація-своєї-гілки). Потім, створити запрос на мердж (пул реквест).

---

## Актуалізація `master`
```
git checkout master // перейти на локальну гітку "master"
git pull // підтягнути зміни (pull - тягнути)
```

## Актуалізація своєї гілки
По аналогії з мастером, все схоже:
```
git checkout master // перейти на локальну гітку "master"
git pull // підтягнути зміни (pull - тягнути)
git checkout НАЗВА_ГІЛКИ // перейти на свою гілку
git merge master // додати в свою гілку актуалізований "master"
```

## React
1. Створи нову папку локально. Використовуй лише латиницю, без пробілів.
2. Перейди у створену папку в терміналі: `cd ШЛЯХ/ДО/ПАПКИ`
3. Ініціалізуй новий локальний репозиторій:

```
створити папку для проекту
git init // ініціалізує новий локальний репозиторій
git remote add origin URL_РЕПОЗИТОРІЯ // каже локальному репозиторію синхронізуватись із репо в інтернеті (віддаленого репо)
npx create-react-app . --template typescript
git add .
git commit -m 'initial commit'
git push -u origin master
npm start

npm install atomic-layout
npm install --save styled-components
npm install --save @types/styled-components
