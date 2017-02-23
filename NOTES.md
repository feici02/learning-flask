# Learning notes
This is my notes while learning this course.

## Sectoin 2

1. create a virtual env
```
python3 -m venv venv
source venv/bin/activate
```

2. add .gitignore, its contens are like this:
```
venv
__pycache__
```

3. start the Flask app
```
pip install flask
cd section-2
python routes.py
```

## Section 3
1. install Postgres.app on macOS

1. create a database
```
> psql
# CREATE DATABASE learningflask;
-- list db
# \l
-- connect to a db
# \c learningflask
-- quitÂ
# \q
```

1. create a table named users
```
> psql
# \c learningflask
CREATE TABLE  users (
uid SERIAL PRIMARY KEY,
firstname VARCHAR(100) NOT NULL,
lastname VARCHAR(100) NOT NULL,
email VARCHAR(120) NOT NULL UNIQUE,
pwdhash VARCHAR(100) NOT NULL
);
SELECT * FROM users;
```

1. insert a record to the table
```
INSERT INTO users(firstname, lastname, email, pwdhash)
VALUES ('Jon', 'Snow', 'jon.snow@gmail.com', 'learning-flask');

SELECT * FROM users;
```

1. install Flask extension: flask-sqlalchemy
```
pip install flask-sqlalchemy
```

## section 4

1. install Flask extension: flask-wtf
```
pip install flask-wtf
```
2. install psycopg2, which is Python-PostgreSQL Database Adapter
```
pip install psycopg2
```
3. start the app, and sign in as a new user
4. check the DB to see if the new user is added
```
> psql
# \c learningflask
# SELECT * FROM users;
# \q
```

## section 5
