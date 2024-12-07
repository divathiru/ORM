# Ex02 Django ORM Web Application
# Date:
02/12/2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM

models.py
~~~
from django.db import models
from django.contrib import admin

class Book(models.Model):
    Book_id = models.CharField(max_length=20, primary_key=True)
    Book_name = models.CharField(max_length=100)
    Mobile_no = models.IntegerField()
    Age = models.IntegerField()
    Email = models.EmailField()
    DoB = models.DateField()
    Book_amount = models.IntegerField()

class BookAdmin(admin.ModelAdmin):
    list_display = ('Book_id', 'Book_name', 'Mobile_no', 'Age', 'Email', 'DoB', 'Book_amount')
~~~
admins.py
~~~
from django.contrib import admin
from .models import Book, BookAdmin
admin.site.register(Book, BookAdmin)
~~~
# OUTPUT
Include the screenshot of your admin page.
![Screenshot 2024-11-22 172953](https://github.com/user-attachments/assets/cce521b6-76ab-4b11-8a92-0c721b0cd7b1)
![Screenshot 2024-11-23 103934](https://github.com/user-attachments/assets/56e68cee-f632-46bb-9de4-fcc0865d8cec)
![Screenshot 2024-12-02 143643](https://github.com/user-attachments/assets/d4041fd7-6621-4d0f-96f9-381b76735adc)



# RESULT
Thus the program for creating a database using ORM hass been executed successfully
