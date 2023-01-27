# djangoproject
MyExpencesOnIncome this is an entity of project. Here we create a dashboard by using django framework. 

Here I am creating a dashboard which shows the expenses and income. Also connecting with PostgreSQL and charts of python.

Step 1. Install python latest version by using https://www.python.org/downloads/ 

Step 2. while installing tick on add PATH. So, you no need to set path manually.

Step 3. click on advanced and tick on pip while installation.

Step 4. For Django installation, use below command

       pip freeze
       pip install django
Step 5. create folder for project
open CMD :

                 d:
                 mkdir djangoproject
                 django-admin
                 django-admin startproject name_of_project

            e.g.  django-admin startproject wscubetech
Step 6. Run the server

     open CMD :  a) python manage.py runserver
     Default pot no. is 8000
Step 7. (Optional) To change the port

    open CMD : a)python manage.py runserver 4444
Port will be change from 8000 to 4444.

Step 7. Create three folder inside djangoproject/wscubetech
i) templates (folder)
ii) static (folder)
iii) media (folder)

Steps 8. inside djangoproject/wscubetech there is again directory wscubetech which is known as app. There are some app settings and files.

          cd   djangoproject/wscubetech/wscubetech 
               __pycache__  <======= folder 
               __init__.py
               asgi.py
               settings.py
               urls.py
               wsgi.py 
