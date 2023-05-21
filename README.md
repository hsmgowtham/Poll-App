# Poll-App


# Setup
- create project
```
django-admin startproject my_poll_site
```
- create polls app
```
python manage.py startapp polls
```
- install Postgre sql adapter
```
pip install psycopg2
```
- Login to postgresql as super user, create user and grant permissions
```
sudo -i -u postgres
psql
Create user hsmgowtham with SUPERUSER;
ALTER USER hsmgowtham WITH PASSWORD 'hsmgowtham';
```
- create table for the polls app
```
CREATE DATABASE poll_app
    WITH
    OWNER = hsmgowtham;
GRANT ALL ON DATABASE otoo_db TO hsmgowtham;
```
- Grant Per
- To create db tables for the installed apps
```
python manage.py migrate
```
- create migration files for the polls app model changes
```
python manage.py makemigrations polls
```
- to check what sql will get executed for models code
```
python manage.py sqlmigrate polls 0001
```
- to check for any problesm without making any migrations or touching the database
```
python manage.py check
```
- run migrate to create models in DB
```
python manage.py migrate
```
- to create python shell
```
python manage.py shell
```
## Create Django Admin User
```
python manage.py createsuperuser
```
