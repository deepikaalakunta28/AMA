### 1.Diff between module and class?
**Module**
- A module is a file that contains Python code.
- It can include functions, variables, and classes.
Example: math.py, views.py

**Class**
- A class is a blueprint for creating objects.
- It defines properties (variables) and behavior (methods).
Example: class Student:
 Used to create objects and represent real-world entities.
### 2. Why do we use cascade?
Cascade usually refers to CSS (Cascading Style Sheets).
- It decides which style rule applies when multiple rules affect the same element.
- Styles are applied based on priority:
1)Inline styles
2)Internal styles
3)External styles
### 3. What is the use of use.py?
urls.py is a file in Django that is used for URL routing.
**Purpose of urls.py**
- It connects a URL (web address) to a view function
- It tells Django which page to show when a user visits a specific URL
**Example**
  ```
  from django.urls import path
from . import views

urlpatterns = [
    path('home/', views.home),
    path('about/', views.about),
]

### 4. What is DOM?
- ORM (Object Relational Mapping)
- Django ORM lets you interact with the database using Python code instead of SQL.
- You use models to create tables.
**Example:**
```
Student.objects.all()

```
Makes database operations easy, safe, and readable.
### 5. Why do we use middleware in django?
- Middleware is a component in Django that works as a bridge between the request and the response.
- It sits between the browser and the view.
**What Does Middleware Do?**
  ```
  Browser → Middleware → View → Middleware → Response
``
**Simple Example of Custom Middleware**
```
class SimpleMiddleware:
    def __init__(self, get_response):
        self.get_response = get_response

    def __call__(self, request):
        print("Before view")
        response = self.get_response(request)
        print("After view")
        return response
```
### 6.What is django ORM?
- ORM (Object Relational Mapping)
- Django ORM lets you interact with the database using Python code instead of SQL.
- You use models to create tables.
**Example:**
```
Student.objects.all()
```
 Makes database operations easy, safe, and readable.
### 7. What is methods?
A method is a function that belongs to a class.
Example:
```
class Student:
    def study(self):
        print("Studying")
```
Methods define actions or behavior of an object.
### 8.What is manage.py used for?
manage.py is a command-line tool in Django.
It is used to:
- Run the server
- Create apps
- Apply migrations
- Create admin users
**Example:**
```
python manage.py runserver
```
Helps manage the Django project.
### 9. What is urls.py?
- It connects a URL (web address) to a view function
- It tells Django which page to show when a user visits a specific URL
**Example**
  ```
  from django.urls import path
from . import views

urlpatterns = [
    path('home/', views.home),
    path('about/', views.about),
]

### 10. What is JSON?
JSON (JavaScript Object Notation)
- A lightweight data format
- Used to send data between client and server
**Example:**
```
{
  "name": "John",
  "age": 25
}
```
Easy to read and widely used in APIs.
### 11.What is POST method?
- POST is an HTTP request method.
- Used to send data to the server
Commonly used in:
- Forms
- Login
- Registration
-  Data is sent securely in the request body.
