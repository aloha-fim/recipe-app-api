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


# docker commands
docker build . or docker-compose build with docker yml file

# docker to create django app mapped to yml volumes
docker-compose run --rm app sh -c "django-admin startproject app ."

# run services on localhost:8000
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
