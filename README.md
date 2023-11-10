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

# docker for delinting 
docker-compose run --rm app sh -c "flake8"

# docker to run tests 
docker-compose run --rm app sh -c "python manage.py test"

