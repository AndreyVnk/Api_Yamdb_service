# API YaMDB

**API YaMDB** - командный проект, поддерживающий обмен данными в формате *JSON*.

Cистема аутентификация реализована через получение JWT-токена. Функционал API предоставляет следующие ресурсы:

- Произведения
- Категории
- Жанры
- Отзывы
- Комментарии


**Технологии:**

* Python 3
* Django Rest Framework
* Simple JWT
* SQLite

## Запуск проекта ##
### 1. Склонировать репозиторий
```
git clone https://github.com/AndreyVnk/Api_Yamdb_service.git
```

### 2. Создать виртуальное окружение и активировать его
Перейти в папку с проектом _Api_Yamdb_service/_ выполнить команды
```
python -m venv venv
source venv/Scripts/activate (для Windows) | source venv/bin/activate (для Linux)
```
### 3. Создать в корневой папке проекта и заполнить файл _.env_
```
SECRET_KEY=secret_django_key
```
### 4. Установить необходимые пакеты
```
pip install -r requirements.txt
```
### 5. Выполнить миграции
Из папки *Api_Yamdb_service/api_yamdb/*, выполнить команду
```
python manage.py migrate
```
### 6. Запустить проект
```
python manage.py runserver
```
Эндпоинты, описанные в документации доступны на корневом адресе проекта: http://127.0.0.1:8000/api/v1/ . Документация к API доступна на http://127.0.0.1:8000/redoc/ .

**Авторы**

AndreyVnk, deorz, idudnikov
