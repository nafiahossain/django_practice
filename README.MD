python3 -m venv venv
source venv/bin/activate

Installation:
pip install Django
python3 -m django --version

pip install psycopg2-binary python-dotenv

Django Project Setup:
django-admin startproject mysite

mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py

Run the project:
cd mysite
python manage.py runserver (Starting development server at http://127.0.0.1:8000/
                            Quit the server with CONTROL-C.)


Initiate and APP (App Setup):
create the app in the same directory as your manage.py file so that it can be imported as its own top-level module, rather than a submodule of mysite.

To create your app, make sure you’re in the same directory as manage.py and type this command:
python manage.py startapp polls

polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py


To access a view in browser, we need to map it to a URL - and for this we need to define a URL configuration, or “URLconf” for short. These URL configurations are defined inside each Django app, and they are Python files named urls.py. To define a URLconf for the polls app, create a file polls/urls.py .

Your app directory should now look like:

polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    urls.py
    views.py