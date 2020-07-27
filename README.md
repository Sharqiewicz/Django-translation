## step by step

install virtualenv

    python3 -m venv venv

install django

    pip install django==2.1.5

start project

    django-admin startproject translation

create app

    python3 manage.py startapp example

create index.html

    touch example/templates/index.html

    connect index in to the view


add text to translate in the index.html

    {% trans "My name is Kacper" %}

add translation loading to the file

    {% load i18n %}

install gettext

    brew install gettext

add french

    django-admin makemessages -l fr

translate by your own in the example/locale


compile messages

    django-admin compilemessagess


INSERT THIS IN THE SEETING.PY

    'django.middleware.common.CommonMiddleware',
        ---> 'django.middleware.locale.LocaleMiddleware', <---
    'django.middleware.csrf.CsrfViewMiddleware',

done!
    python3 manage.py runserver
