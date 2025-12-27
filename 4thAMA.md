### 1.What is django?
Django is a high-level Python web framework used to build secure, scalable, and maintainable web applications quickly.
It follows the MVC/MVT architecture, includes built-in features like authentication, ORM, admin panel, and focuses on “don’t repeat yourself (DRY)” and rapid development.
### 2.What is views.py?
views.py is a file in a Django app where you define View functions or classes.
A view:
- Receives a request
- Processes data (optional: interacts with models)
- Returns a response (HTML, JSON, etc.)
**Example:**
```
from django.http import HttpResponse

def home(request):
    return HttpResponse("Hello, Django!")
```
### 3.What is the use of shell in django?
The Django shell is an interactive Python shell with your project context loaded.
You use it to:
- Test database queries
- Interact with models
- Debug logic
- Run scripts safely
### 4.What are the django project?
A Django project is the overall application container that may contain one or more apps.
It includes configuration files such as:
- settings.py — project settings
- urls.py — global routing
- wsgi.py / asgi.py — deployment entry points
A project = whole website
An app = module inside project (e.g., blog, users, payments)
### 5.Why do we use makemigration and migrate?
| Command          | Purpose                                           |
| ---------------- | ------------------------------------------------- |
| `makemigrations` | Detects model changes and creates migration files |
| `migrate`        | Applies migrations to the database                |

### 6.What is annotation and aggregate?
**Aggregate**
Used to compute values across entire querysets (sum, avg, min, max, count).
```
from django.db.models import Count
User.objects.aggregate(total=Count('id'))
```
**Annotation**
Adds calculated fields per record in the queryset.
```
from django.db.models import Count
Author.objects.annotate(book_count=Count('books'))
```
- Aggregate → summary for all rows
- Annotate → computed field per row
### 7.What is the diff b/w authentication and authorization?
| Feature        | Meaning                                                |
| -------------- | ------------------------------------------------------ |
| Authentication | Verifies **who the user is** (login, identity)         |
| Authorization  | Controls **what user can access** (permissions, roles) |

### 8.What is an event js?
An event is an action or occurrence detected by JavaScript in the browser.
**Examples:**
- Click
- Mouse hover
- Key press
- Page load
**Example handler:**
```
button.onclick = function() {
  alert("Button clicked");
}
```
### 9.What is the client–server architecture?
Client = sends request (browser, mobile app)
Server = processes request and sends response
**Example process:**
- Browser → sends request → Server
- Server → processes → returns data → Browser displays it
### 10.What is middleware?
Middleware is a layer between request and response that processes them globally.
**Uses include:**
- Authentication
- Logging
- Security checks
- Request/Response modification
