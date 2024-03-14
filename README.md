### Описание проекта
Сайт с возможностью публикации фотографий котиков и их достижений

## Инструменты и стек: 
#Python #Django #Docker-compose #API #Nginx #Pillow #Djoser #Gunicorn #Python-dotenv #JSON #YAML #Postman #PyCharm

## Запуск проекта из образов с Docker hub
cd frontend  # В директории frontend...
docker build -t username/kittygram_frontend .  
cd ../backend  
docker build -t username/kittygram_backend .
cd ../ nginx  
docker build -t username/kittygram_gateway .

Отправьте собранные образы фронтенда, бэкенда и Nginx на Docker Hub:
docker push username/taski_frontend
docker push username/taski_backend
docker push username/taski_gateway 



## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: 1231312wwww
kittygram_domain: https://hame.duia.eu
taski_domain: https://we.zapto.org
dockerhub_username: wertip
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Примеры запросов
Добавить питомца: POST /cats/add

Редактировать питомца: PUTCH /cats/edit

Просмотр питомца: GET /cats/{cat_id}
## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.
