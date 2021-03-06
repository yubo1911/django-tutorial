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

# PART III
 - add urls.py in apps dir. edit mysite/urls.py to point the related urls to the app urls.py to dispatch.
 - edit the view.py in apps dir. each function in view.py is related to a url. the parameters could be find in the regex in urls.py.
 - app's template file should be located in app_dir/templates/app_name/template_name.html.
 - use loader, RequestContext to render a HttpResponse.
 - or use shortcuts render with request, template path and a dictionary to return a HttpResponse.
 - use python code *url* to remove the hardcode urls in templates. namespace is needed if you have more than one apps.

# PART IV
 - for the post request, the parameter will be stored in dict request.POST.
 - for the post request, always use a HttpResponseRedirect to render a new page.
 - use generic views, such as DetailView, ListView, can simplify your view code. You just need to config template_name, model or some other attrs.

# PART V
 - each test case class must drived from TestCase. 
 - each test function's name must start with a 'test' string.
 - there are several assert functions you can use when write test functions. such as assertEqual, assertContains, assertQuerysetEqual...
 - the TestCase has an 'client' attr to simulate a client to test views.
 - you can get a response from a view using self.client.get(reverse('polls:index')).
 - for each test function, the TestCase would create a seperate new database for test. so don't worry about the previous test function would effect the current one.
 
