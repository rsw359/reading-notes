# Class 29

## Docker

Docker is a way to isolate and run entire applications. Docker can be shared among team members so everyone is working on the same setup.

Docker utilizes Linux containers, which are a type of virtualization. This gets rid of the need to run virtual environments.

Virtual environments are used to isolate Python software packages locally. With virtual environments, different versions of Python and Django can be run on the same machine. But virtual environments can only isolate packages.

An image is a snapshot in time of what a project *contains*. A container is a running instance of the image.

To create an Image define with ‘**Dockerfile**’, then add the **FROM python: version**

Dockerfiles are read from top-to-bottom. The first instruction **must** be the **FROM** command which lets us import a base image to use for our image.

To BUILD the image : **docker image build .**

To list all existing Docker images to confirm this new one has been built: **docker image ls**

Every image is made up of one or more image layers.Each image layer is immutable–unchanged–like a git commit. This helps ensure consistency when two developers build the same image.

A **Dockerfile** is a list of image instructions, and  there is also a **docker-compose.yml**
 file that is a list of container instructions.

To create a new Django project from scratch:

```docker
cd ..
mkdir djangoapp && cd djangoapp
pipenv install django==3.0
pipenv shell

django-admin startproject example_project .
python manage.py runserver
```

To “Dockerize” Django:

```python
touch Dockerfile
touch docker-compose.yml
```

```python
# Dockerfile

# Python version
FROM python:3.7-alpine

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory
WORKDIR /code

# Install dependencies
COPY Pipfile Pipfile.lock /code/
RUN pip install pipenv && pipenv install --system

# Copy project
COPY . /code/
```

Now time for **docker-compose.yml:**

```python
# docker-compose.yml
version: '3.10'

services:
  web:
    build: .
    command: python /code/manage.py runserver 0.0.0.0:8000
    volumes:
      - .:/code
    ports:
      - 8000:8000
```

Alternatively, instead of running separate commands to build the image and run the container we can do that with one: **docker-compose up --build**

The important takeaways from this tutorial are this:

- Docker is a way to run Linux containers
- Containers are a lightweight alternative to Virtual Machines
- **Dockerfile** is a list of instructions for creating an image
- Images are made up of one or more layers
- Containers are a running instance of an image
- **docker-compose.yml** controls how to run the container
- Containers are stateless and ephemeral in nature. We can link the local filesystem via **volumes** but things become more complex with databases (which we didn’t cover here).

## Django for APIs

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework. It always must be added to a project *after* Django itself has been installed and configured.

Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

A traditional Django website consists of a single *project* with multiple *apps* representing discrete functionality.

Adding Django REST Framework is just like installing any other third-party app:

`.venv) > python -m pip install djangorestframework~=3.13.0`

To formally notify Django of the new installation in our `django_project/settings.py`
 file. Scroll down to the `INSTALLED_APPS` section and add `rest_framework`.

A web API will expose a single endpoint that lists out all objects in JSON. To do this, a new URL route, a new view, and a new serializer file are necessary.

using the `startapp` command.

Apps should always have a plural name since Django will otherwise automatically add an `s`
in the admin and other locations:`.venv) > python manage.py startapp apis`

Then add it to `INSTALLED_APPS` in our “Local” section. There is no need to migrate.

Adding an API endpoint is just like configuring a traditional Django URL route. In the project-level `django_project/urls.py` file `include` the `apis` app and configure its URL route, which will be at `api/`.

```python
# django_project/urls.pyfrom django.contrib import admin
from django.urls import path, include

urlpatterns= [
    path("admin/", admin.site.urls),
    path("api/", include("apis.urls")),# newpath("", include("books.urls")),
```

Then create a new file called `apis/urls.py` with your text editor:

```python
# apis/urls.pyfrom django.urls import path

from .views import BookAPIView

urlpatterns= [
    path("", BookAPIView.as_view(), name="book_list"),
]
```

Django REST Framework views are similar to traditional django views, except the end result is serialized data in JSON format.

The only two steps required in our view are to specify the `queryset`, which is all available books, and then the `serializer_class` which will be `BookSerializer`.

```python
 apis/views.pyfrom rest_framework import generics

from books.models import Book
from .serializers import BookSerializer

classBookAPIView(generics.ListAPIView):
    queryset= Book.objects.all()
    serializer_class= BookSerializer
```

A serializer translates complex data like querysets and model instances into a format that is easy to consume over the internet, typically JSON

create a new file called `apis/serializers.py` and update:

```
# apis/serializers.pyfrom rest_framework import serializers

from books.models import Book

classBookSerializer(serializers.ModelSerializer):
classMeta:
        model= Book
        fields= ("title", "subtitle", "author", "isbn")
```

Deploying a web API is almost identical to deploying a traditional website, like in Heroku, for example.

Notes  taken from [https://djangoforapis.com/library-api/](https://djangoforapis.com/library-api/)
