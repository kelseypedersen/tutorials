# tutorials
tutorials by kelsey

### Initial App Setup

- Check if you have Django installed
`$ python`

- Create a Django app with PostgreSQL
`$ django-admin startproject PROJECTNAME`
  - This will generate an initial django project

- Run the server
`$ python manage.py runserver`

- Now let's add Postgres as the database (currently sqlite3 by default)
  - Download Postgres 9.5.0 via the Graphical Installer (44.1MB)
  - Install psycopg2
    - `$ pip install psycopg2`
    - Add to your requirements/base.txt file and install it into all your environments

- Add a user to the database
  - `$ createdb leadgenius_django_db`
  - `$ psql`
    - `# CREATE ROLE dev WITH LOGIN PASSWORD 'leadgenius';`
    - `# GRANT ALL PRIVILEGES ON DATABASE leadgenius_django_db to dev;`
    - `# ALTER USER dev CREATEDB;`

Connecting to Postgres
- Open up postgres
  - `$ psql`
  - `\connect lg_db` --> as Kelsey
  - `\dt` to show all the tables in the database
  - `SELECT * FROM emails_email`

- Create database
  - `python manage.py makemigrations`
  - `python manage.py migrate`
  
- psql shortcuts
  - `\?` - help
  - `\d emails_submissions` - list all columns in a table


