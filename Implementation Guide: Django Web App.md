## Implementation Guide: Django Web App

### Project Setup


1. **Set Up Your Environment**:
   - Install Python: Make sure you have Python installed on your system. You can download it from the official website: [Python Downloads](https://www.python.org/downloads/).
   - Install Django: You can install Django using pip, the Python package manager:
     ```bash
     pip install django
     ```
   - Install Git: Install Git if you haven't already. You can download it from [Git Downloads](https://git-scm.com/downloads).

2. **Create Django Project**:
   - Use Django's command-line utility to create a new project.
     ```bash
     django-admin startproject CrewSchedule
     ```

3. **Create Django App**:
   - Inside the project directory, create a new Django app.
     ```bash
     python manage.py startapp myapp
     ```

### Directory Structure

Your directory structure should look like this:


- `CrewSchedule/`: Main project directory.
  - `CrewSchedule/`: Inner project directory.
    - `settings.py`: Project settings file.
    - `urls.py`: Main URL configuration.
  - `myapp/`: Django app directory.
    - `views.py`: Contains view functions.
    - `urls.py`: Defines URL patterns for the app.
    - `templates/`: Directory for HTML templates.
  

### Views and URLs

1. **Define Views**:
   - Implement view functions in `views.py`.
   ```python
   # myapp/views.py
   from django.shortcuts import render

   def home(request):
       return render(request, 'home.html')

2. **Define URLs**
   - Implement url functions in `urls.py`.
   ```python
   # myapp/urls.py
   from django.urls import path
   from . import views

   urlpatterns = [ path('', views.home, name='home'), ]

3. **Create a Home Page**
   
   ```html   
   <!-- myapp/templates/home.html -->
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Home Page</title>
   </head>
   <body>
       <h1>Welcome to My Django Web App!</h1>
       <!-- Add more HTML content as needed -->
   </body>
   </html>
### Run the app on port 8000

1. **Run the server**
   
   ```python
   python manage.py runserver

3. In your browser go to [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
