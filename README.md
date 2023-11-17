# recipe-app-api
recipe API project

# framework
Python
Django
Django REST
PostgreSQL
Docker
Swagger Documentation
GitHub Actions testing and linting automation


# docker commands to build image after requirements.txt
docker build . or docker-compose build with docker yml file

# docker to create django apps mapped to yml volumes
docker-compose run --rm app sh -c "django-admin startproject app ."
docker-compose run --rm app sh -c "python manage.py startapp user"
docker-compose run --rm app sh -c "python manage.py startapp recipe"


# run services on localhost:8000 and update any new migrations added
docker-compose up

# docker for delinting
docker-compose run --rm app sh -c "flake8"

# docker to run unit tests (TDD test driven development)
docker-compose run --rm app sh -c "python manage.py test"

# docker TDD with linting
docker-compose run --rm app sh -c "python manage.py wait_for_db && flake8"

# docker clear volumes and migrate
docker volume ls
docker volume rm []
docker-compose down
docker volume rm []
docker volume ls
docker-compose docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"
docker-compose run --rm app sh -c "python manage.py test"

# docker make migrations
docker-compose run --rm app sh -c "python manage.py makemigrations"
