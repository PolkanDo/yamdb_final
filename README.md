# yamdb_final 
![YaMDB-app workflow](https://github.com/PolkanDo/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

### Описание
Учебный проект для Я.Практикума

### Автор
Студент 18 когорты Я.Практикума: Павел Палютин

### Технологии
Python 3.7  
Django 2.2.6
Docker 3.8
Nginx
Gunicorn
Pytest

## Подготовка к запуску
Установите виртуальное окружение:
```
pip install virtualenv
```
Создайте виртуальное окружение:
```
python -m venv venv
```
Запустите виртуальное окружение:
```
source venv/bin/activate
```
Установите зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
В папке с файлом manage.py выполните команду:
```
python3 manage.py makemigrations
```
## Запуск проекта
Запускаем сборку контейнеров командой:
```
docker-compose up --build 
```
с флагом -d запуск произойдет в фоновом режиме.

Спустя некотрое время контейнер запустится и появится сообщение о запуске контейнеров:
```
Starting yamdb_db_1 ... done
Starting yamdb_web_1 ... done
Starting yamdb_nginx_1 ... done
```
## Проверка работоспобности
Создаем суперпользователя для работы с админкой. Указываем емейл, логин и пароль
```
docker-compose exec web python manage.py createsuperuser
```
```
Email: practikum@yandex.ru
Username: practikum
Password: 
Password (again): 
```
```
Superuser created successfully.
```

## Сервис доступен по ссылке: 
http://51.250.1.227/admin
