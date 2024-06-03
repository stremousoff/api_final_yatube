### О проекте Yatube:
Проект Yatube – прототип социальной сети для публикаций постов. 

Посты размещены по тематическим группам. На данный момент API социальной сети поддерживает следующий функционал для зарегистрированных пользователей:
- публикация постов и изображения к ним;
- комментирование ранее опубликованных публикаций;
- оформление подписок.

По техническому заданию API к Yatube не должно поддерживать:
- создание групп. Группы создаёт администратор сайт через админ панель;
- регистрация пользователя. Пользователя регистрирует администратор сайта через админ панель.

### Стэк:
```
Python
Sqlite3
Django
Django Restframe Work(DRW)
Djoser
```
### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/stremousoff/api_final_yatube
```
```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv env
```
```
source env/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python3 manage.py migrate
```
Запустить проект:
```
python3 manage.py runserver
```
### Спецификация ReDoc:
```
http://127.0.0.1:8000/redoc/
```
### Примеры запросов:
1- GET - Get item list - HTTP Response Code: 200
```
javascript
    HTTP/1.1 200
    Content-Type: application/json

    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2019-08-24T14:15:22Z",
      "image": "string",
      "group": 0
    }
```
2- GET - Get item list - HTTP Response Code: **200**
```javascript
    HTTP/1.1 200
    {
      "count": 123,
      "next": "http://api.example.org/accounts/?offset=400&limit=100",
      "previous": "http://api.example.org/accounts/?offset=200&limit=100",
      "results": [
        {
          "id": 0,
          "author": "string",
          "text": "string",
          "pub_date": "2021-10-14T20:41:29.648Z",
          "image": "string",
          "group": 0
        }
      ]
    }
```
3- POST - Create a new item - HTTP Response Code: **201**
```javascript
    HTTP/1.1  201
    Content-Type: application/json
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2019-08-24T14:15:22Z",
      "image": "string",
      "group": 0
    }
```
Автор проекта  [Stremousoff](https://github.com/stremousoff/)