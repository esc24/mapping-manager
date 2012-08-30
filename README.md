mapping-manager
===============

PLEASE NOTE: This is pre-alpha software and is in a continuous state of flux. Please do not rely on it for anything.

Dependencies
------------
* Django - https://www.djangoproject.com/
* Backend database e.g Sqlite - http://www.sqlite.org/

Initial setup
-------------
Things you need to do before running the application:

1. Create a 'settings_local.py' file containing
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.sqlite3',
            'NAME': '/path/to/databasefile'  # If this does not exist it will be created by the syncdb command
        }
    }

    TEMPLATE_DIRS = ('<absolute path to this app>/manager/templates',)

If you are not using SQLite3, please consult the Django documentation for
details of other supported databases.

2. run `python ./manage.py syncdb` to create and populate your Django database

Starting/stopping the app
-------------------------
1. To start the application run `python ./manage.py runserver`
2. To view the application, point your web browser at http://localhost:8000/mapping-manager 
3. To stop the application type `Ctrl-D` in the terminal used to start the application.

