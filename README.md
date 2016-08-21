# Groceries List API


## Getting started

### Code setup
1. Clone this project in a local directory:
...`git clone https://github.com/smaniotto/groceries-api`
1. If necessary, install python and pip.
1. If necessary, install virtualenv:
...`pip install virtualenv`
1. Create a new virtualenv in the project directory and activate it:
...`virtualenv venv`
...`. venv/bin/activate`
1. Install dependencies:
...`pip install -r requirements.txt`

### Database setup
If you don't have a postgres database server running, I recommend using a Docker image. After installing Docker, simply run:
_Remember to replace what's marked as <...>_
`docker run --name <be-creative> -e POSTGRES_USER=<user> -e POSTGRES_PASSWORD=<password> -p 5432:<port> -d postgres`
And create a new database:
`psql -h localhost -U <user> postgres`
_type password_
`create database <db-name>;`
Follow the instructions on `.env.example` to build the URL referencing the database.

### Environment variables
1. Duplicate the `.env.example` file into a new `.env` file.
1. Add the required values for the environment you are working from.
1. The defined vars will be loaded with `python-dotenv` to your settings file.
1. If a new var should be added to the project, add it also to `.env.example` with a doc note.

### Add dependencies
You can either do it manually, by typing the dependency name and version to `requirements.txt`, or:
`pip install <dependency name>`
`pip freeze > requirements.txt`

### Run it
`python manage.py runserver 0.0.0.0:8000`
