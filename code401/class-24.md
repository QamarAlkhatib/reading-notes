# A Beginner's Guide to Docker

Docker is simply a sort of virtualization that uses Linux containers.

Virtualization can be traced back to the early days of computing, when enormous, expensive mainframe computers were the standard. How could a single machine be used by several programmers? Virtualization, specifically virtual machines, which are full clones of a computer system from the operating system on up, was the answer.

## Containers vs Virtual Environments

Python software packages are isolated locally using virtual environments. On the same machine, we may establish an isolated box for individual projects, allowing one to utilize Python 2.7 and Django 1.5 while another uses Python 3.5 and Django 2.1.

## Django for APIs - Library Website

### Chapter 2: Library Website and API

To construct online APIs, the Django REST Framework works in tandem with the Django web framework. Django Rest Framework cannot be used to create a web API; it must always be introduced to a project after Django has been installed and configured.

### Django REST Framework

Django REST Framework is added just like any other third-party app.

To install Django REST Framework inside the django project run this command:

```console
pipenv install djangorestframework~=3.11.0
```

Then we add to INSTALLED_APPS onfig in our settings.py file:

```python

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    # 3rd party
    'rest_framework', # new

]
```

- Then we add t URLS configs:

```python
# config/urls.py
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('api/', include('api.urls'))
]

```

- The other parts are technical, so i will skip it until i create one with it or the lab.

<https://djangoforapis.com/library-website-and-api/>
