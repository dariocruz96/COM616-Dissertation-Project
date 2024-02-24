# Connecting to a PostgreSQL Database with Django

## Pre-requisites
- Django installed in your Python environment
- PostgreSQL server installed and running
- Knowledge of your PostgreSQL database credentials (username, password, host, port)
- Basic understanding of Django ORM (Object-Relational Mapping)

## Steps

### 1. Install PostgreSQL Adapter for Python
Ensure you have the `psycopg2` package installed, which is the PostgreSQL adapter for Python. You can install it via pip:

```bash
pip install psycopg2
```

### 2. Configure Database Settings in Django
In your Django project, navigate to the settings.py file located inside the project directory (<your_project>/settings.py).

Find the DATABASES setting and configure it to connect to your PostgreSQL database. Modify the DATABASES setting as follows:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_database_name',
        'USER': 'your_database_user',
        'PASSWORD': 'your_database_password',
        'HOST': 'localhost',  # or your database host
        'PORT': '5432',       # or your database port
    }
}
```
Replace 'your_database_name', 'your_database_user', and 'your_database_password' with your actual database credentials.

### 3. Run Django Migrations
Run Django's migrate command to create necessary database tables and schema:

```bash
python manage.py migrate
```
This command will synchronize the database state with the current set of models and create necessary tables.

### 4. Test the Connection
To test if Django can connect to the PostgreSQL database, run the Django development server:

```bash
python manage.py runserver
```
If there are no errors, Django successfully connected to the PostgreSQL database.

### 5. Perform Database Operations
You can now perform various database operations using Django's ORM, such as creating, reading, updating, and deleting records.

That's it! You have successfully connected your Django project to a PostgreSQL database.
