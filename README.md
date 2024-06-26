# Кошачий благотворительный фонд (0.1.0)

Фонд собирает пожертвования на различные целевые проекты: на медицинское обслуживание нуждающихся хвостатых, на обустройство кошачьей колонии в подвале, на корм оставшимся без попечения кошкам — на любые цели, связанные с поддержкой кошачьей популяции.

## Технологии

[![Python][Python-badge]][Python-url]
[![FastAPI][FastAPI-badge]][FastAPI-url]
[![SQLAlchemy][SQLAlchemy-badge]][SQLAlchemy-url]

## Возможности приложения

- Авторизация и аутентификация пользователей.
- Управление пользователями и благотворительными проектами.
- Совершение пожертвований на благотворительные проекты.
- Создание новых благотворительных проектов и редактирование уже существующих.

## Установка

Клонируйте репозиторий на ваш компьютер, в локальном репозитории создайте и активируйте виртуальное окружение, обновите менеджер пакетов pip и установите зависимости из файла requirements.txt.

```bash
git clone <адрес репозитория>
python -m venv venv
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Использование

В корне проекта создайте файл переменных окружения `.env` со следующими переменными:
```
APP_TITLE=<Укажите, если хотите придумать своё название приложения>
APP_DESCRIPTION=<Укажите, если хотите придумать своё описание приложения>
DATABASE_URL=<Укажите для использования своей БД (по умолчанию sqlite)>
SECRET_KEY=<ваш секретный ключ>
```
Примените миграции:
```bash
alembic upgrade head
```
Приложение готово к запуску по следующей команде:
```
uvicorn app.main:app --reload
```
Во время первого запуска будет создан первый суперюзер. </br>
Вы можете ознакомиться в функционалом доступных эндпоинтов по следующим адресам: </br>
- http://127.0.0.1:8000/docs (документация Swagger)
- http://127.0.0.1:8000/redoc (документация Redoc)


## Лицензия

[MIT](https://choosealicense.com/licenses/mit/)

<!-- MARKDOWN LINKS & BADGES -->

[Python-url]: https://www.python.org/
[Python-badge]: https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white

[FastAPI-url]: https://fastapi.tiangolo.com/
[FastAPI-badge]: https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white

[SQLAlchemy-url]: https://www.sqlalchemy.org/
[SQLAlchemy-badge]: https://img.shields.io/badge/SQLAlchemy-CC2927?style=for-the-badge&logo=sqlalchemy&logoColor=white
