# CI и CD проекта api_yamdb
REST API проект для сервиса YaMDb (Сервис сбора отзывов на произведения)

Просмотр документации API: http://51.250.69.91/redoc/

![example workflow](https://github.com/lichinin/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)


## Шаблон заполнения env-файла
```
DB_NAME=postgres # имя базы данных
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД
```

## Описание команд для запуска приложения в контейнерах
Соберите контейнеры и запустите их:  
```
docker-compose up -d --build
```

## Выполнение миграций
Запустите миграции:  
```
docker-compose exec web python manage.py migrate
```

## Создание суперпользователя:
Создайте суперпользователя:  
```
docker-compose exec web python manage.py createsuperuser
```

## Подготовка статики
Соберите статику:  
```
docker-compose exec web python manage.py collectstatic --no-input
```


### Автор
Личинин Виталий - https://github.com/Lichinin

