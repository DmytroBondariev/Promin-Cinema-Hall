# Cinema API

API service for cinema halls

## Installing process

#### Open terminal
```
    git clone https://github.com/Dmytry95/cinema-API.git
    cd CinemaAPI
    python -m venv venv
    sourse venv/bin/activate
    pip install -r requirements.txt
    set SECRET_KEY=DJANGO_SECRET_KEY
    set POSTGRES_HOST=db
    set POSTGRES_NAME=your_db_name
    set POSTGRES_USER=db_user
    set PASSWORD=POSTGRES_PASSWORD
    python manage.py migrate
    python manage.py runserver
```

Change mocks to your native data inside .env.sample. Do not forget to change file name to ".env".

Migrate data to database and run the server:
```
    python manage.py migrate
    python manage.py runserver
```

## Run with docker
Docker should be installed

Change POSTGRES_HOST value to 'db' inside .env file.
#### Open terminal
```
    docker-compose build
    docker-compose up
```

## Getting access

* create user via /api/user/register
* get access token via api/user/token

## Features
* JWT authenticated
* Admin panel /admin/
* Documentation is located at api/doc/swagger
* Managing movies with genres, actors
* Creating cinema halls
* Adding movie sessions
* Filtering movies and movie sessions
* The ability to add photos to movies 