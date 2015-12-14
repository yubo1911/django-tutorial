# django-tutorial
To study and use django with python3.

# PART I
 - django-admin.py startproject mysite // Create a new project
 - python3 manage.py migrate // Create default databases
 - python3 manage.py runserver 0.0.0.0:8000 & // Run test server
 - python3 manage.py startapp polls // Create an app
 - edit polls/models.py // Add some models
 - python3 manage.py makemigrations polls // Make migrations(not real migrate databases)
 - python3 manage.py migrate // Real migrate databases
 - python3 manage.py shell // Run the shell, and test models in it as using python shell

# PART II
 - python3 manage.py createsuperuser // Create a super user
 - edit yourapps/admin.py // Register models to the admin page
 - edit yourapps/admin.py // Change the admin page showing info and layout. Also add filter, search box and so on widgets to admin page.
 - mkdir templates in the manage.py dir. copy the default django templates(django/contrib/admin/templates/admin/base_site.html) to this templates dir.
 - add TEMPLATE_DIRS to mysite/settings.py
 - edit the template file(base_site.html) to customize the page.
