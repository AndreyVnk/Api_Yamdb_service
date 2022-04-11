<h2 align="center">API YaMDb</h2>

Данный проект - это backend и API портала YaMDb.
Он позволяет работать с данными портала YaMDb через API.

## Установка и использование

### Установка

Клонируйте файлы проекта в локальное хранилище и перейдите в папку с проектом:

`git clone https://github.com/GeneralMinimus/api_yamdb.git`

`cd api_yamdb`

Создайте и активируйте виртуальное окружение:

`python3 -m venv venv`

`source venv/bin/activate`

Установите зависимости:

`python3 -m pip install --upgrade pip`

`pip install -r requirements.txt`

Выполните миграции:

`python3 manage.py migrate`

Запустите проект:

`python3 manage.py runserver`

### Использование

Проект поддерживает следующие эндпоинты и методы запроса:

Запросы к API начинаются с `/api/v1/`

1. AUTH. Регистрация пользователей и выдача токенов

`/auth/signup/` POST - регистрация нового пользователя

`/auth/token/` POST - получение JWT-токена

2. CATEGORIES. Категории (типы) произведений

`/categories/` GET - получение списка всех категорий POST - добавление новой категории

`/categories/{slug}/` DELETE - удаление категории

3. GENRES. Категории жанров

`/genres/` GET - получение списка всех жанров POST - добавление жанра

`/genres/{slug}/` DELETE - удаление жанра

4. TITLES. Произведения, к которым пишут отзывы

`/titles/` GET - получение списка всех произведений POST - добавление произведения

`/titles/{titles_id}/` GET - получение информации о произведении PATCH - частичное обновление информации о произведении DELETE - удаление произведения

5. REVIEWS. Отзывы

`/titles/{titles_id}/reviews/` GET - получение списка всех отзывов POST - добавление нового отзыва

`/titles/{titles_id}/reviews/{review_id}/` GET - получения отзыва по id PATCH - частичное обновление отзыва по id DELETE - удаление отзыва по id

6. COMMENTS. Комментарии к отзывам

`/titles/{title_id}/reviews/{review_id}/comments/` GET - получение списка всех комментариев к отзыву POST - добавление комментария к отзыву

`/titles/{title_id}/reviews/{review_id}/comments/{comment_id}/` GET - получение комментария к отзыву PATCH - частичное обновление комментария к отзыву DELETE - удаление комментария к отзыву

7. USERS. Пользователи

`/users/` GET - получение списка всех пользователей POST - добавление пользователя

`/users/{username}/` GET - получение пользователя по username PATCH - изменение данных пользователя по username DELETE - удаление пользователя по username

`/users/me/` GET - получение данных своей учетной записи PATCH - изменение данных своей учетной записи
