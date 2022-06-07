# Foodgram -- сайт, где пользователь может опубликовать собственный рецепт, подписаться не рецепты/авторов рецептов, скачать готовый список рецептов. 
## Подготовка виртуальной машины
sudo apt update 
sudo apt upgrade -y
sudo apt install python3-pip python3-venv git -y
sudo apt install docker.io -y 
sudo apt install docker-compose -y
## Установка
Склонируйте репозиторий git clone https://github.com/TrokhinMaxim/foodgram-project-react.git

Перейдите в папке infra и создайте .env файл.
Находясь в той же папке собираем  и запускаем образы docker-compose up -d --build
Открываем контейнер: sudo docker exec -it infra_backend_1 bash
Заполняем БД: python manage.py make migrations/migrate 
Собираем статику: python manage.py collectstatic 
Создаём суперюзера: python manage.py createsuperuser 
Загружаем ингредиенты: python manage.py loadjson --path 'recipes/data/ingredients.json' 
Загружаем теги: python manage.py loadjson --path 'recipes/data/tags.json'







130.193.40.60

Superuser

login - admin
pw - admin

User

login - maxim@yandex.ru
pw - 111111aaa ( а английские)
