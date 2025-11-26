# Ex02 Django ORM Web Application
## Date:

## AIM
To develop a Django Application to store and retrieve data from a E-Commerce Website Database for Amazon or Flipkart using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/e835b588-f619-4461-b820-141e1ca59a22" />

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
```python
model.py
from django.db import models
from django.contrib import admin

class Movie(models.Model):
    title = models.CharField(max_length=50)
    director = models.CharField(max_length=50)
    release_date = models.DateField()
    genre = models.CharField(max_length=30)
    rating = models.FloatField(default=0.0)

class MovieAdmin(admin.ModelAdmin):
    list_display = ('title', 'director', 'release_date', 'genre', 'rating')

admin.py
from django.contrib import admin
from .models import Movie, MovieAdmin

admin.site.register(Movie, MovieAdmin)

```


## OUTPUT

<img width="1282" height="676" alt="Screenshot 2025-11-27 011627" src="https://github.com/user-attachments/assets/9b20c865-eccf-42b1-895f-8a2c56bdfc1c" />


## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
