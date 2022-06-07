# Foodgram -- сайт, где пользователь может опубликовать собственный рецепт, подписаться не рецепты/авторов рецептов, скачать готовый список рецептов. 
## Подготовка виртуальной машины
sudo apt update<br>
sudo apt upgrade -y<br>
sudo apt install python3-pip python3-venv git -y<br>
sudo apt install docker.io -y <br>
sudo apt install docker-compose -y<br>
## Установка
Склонируйте репозиторий git clone https://github.com/TrokhinMaxim/foodgram-project-react.git

Перейдите в папке infra и создайте .env файл.<br>
Находясь в той же папке собираем  и запускаем образы docker-compose up -d --build<br>
Открываем контейнер: sudo docker exec -it infra_backend_1 bash<br>
Заполняем БД: python manage.py make migrations/migrate <br>
Собираем статику: python manage.py collectstatic <br>
Создаём суперюзера: python manage.py createsuperuser <br>
Загружаем ингредиенты: python manage.py loadjson --path 'recipes/data/ingredients.json' <br>
Загружаем теги: python manage.py loadjson --path 'recipes/data/tags.json'<br>







130.193.40.60

Superuser

login - admin
pw - admin

User

login - maxim@yandex.ru
pw - 111111aaa ( а английские)
