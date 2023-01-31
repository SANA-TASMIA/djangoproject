# djangoproject

MyExpencesOnIncome this is an entity of project. Here we create a dashboard by using django framework.

Here I am creating a dashboard which shows the expenses and income. Also connecting with PostgreSQL and charts of python.

**\*Uploading project on github from git(working dir)**

How to upload project directory on github.

1. Create Github account then sign-in
2. Create Repository - **New** then YOUR_REPO_NAME
3. Select repo privacy a)public b)private

first initialize git

               git init
               git add .
               git commit -m "uploading project on github"
               git config --global user.name "YOUR_NAME"
               git config --global user.email "YOUR_EMAIL_ID@gmail.com"
               git config --list
               git branch -M main
               git remote add origin https://github.com/     /* copy your repository url
               git pull -u origin main
               git push -u origin main

               after this if you update on github then

               git pull
               git push

               if you update on working directory project(on your pc)

               git add .
               git commit -m "YOUR_MESSAGE_FOR COMMIT"
               git pull
               git push

**\*Installation :**

Step 1. Install python latest version by using https://www.python.org/downloads/

Step 2. while installing tick on add PATH. So, you no need to set path manually.

Step 3. click on advanced and tick on pip while installation.

Step 4. For Django installation, use below command

       pip freeze
       pip install django

**\*Create a project :**

Step 1. create folder for project
open CMD :

                 d:
                 mkdir djangoproject
                 django-admin
                 django-admin startproject name_of_project

            e.g. django-admin startproject MyExpencesOnIncome

**\*Run the Server:**

Step 1. Run the server

     open CMD :  a) python manage.py runserver

    *Note: Default port no. is 8000

    OR

Step 1. (Optional) To change the port

    open CMD : a) python manage.py runserver 4444
        *Note: Port will be change from 8000 to 4444.

**\*Create the three folder**

Step 7. Create three folder inside djangoproject/MyExpencesOnIncome
i) templates (folder)
ii) static (folder)
iii) media (folder)

Steps 8. Inside djangoproject/MyExpencesOnIncome there is again directory MyExpencesOnIncome which is known as app. There are already having some app settings and files.

          cd   djangoproject/wscubetech/wscubetech
               __pycache__  <======= folder
               __init__.py
               asgi.py
               settings.py
               urls.py
               wsgi.py

**\*Download SQL-postreSQL from below link**

https://sbp.enterprisedb.com/getfile.jsp?fileid=1258228

**_Installation Process of SQL-PostgreSQL_**

**_Setup for postgreSQL_**

1.  Welcome to postgreSQL wizard ===> click on **NEXT**
2.  Installation directory C:\Programfile\PostgreSQL\15 ===> click on **NEXT**
3.  Select Component (tick on it) ---> a. PostgreSQL Server
    b. pgAdmin 4
    c. Stack Builder
    d. Command Line Tools ===> Then click on **NEXT**

4.  Data directory C:\Programfile\PostgreSQL\15\data ===> click on **NEXT**
5.  Password => select and confirm an administrative password for the PostgreSQL **superuser** (called **postgres**):
    **Password**
    **Retype Password**
    ===> click on **NEXT**

6.  Port => **Port** 5432 ===> click on **NEXT** (\*Note: Port **5432** is **default** Port )
7.  Advance Option => pick the locale that your database will use:
    **Locale:** Default Locale
    ===> click on **NEXT**
8.  Pre-Installation summary ===> click on **NEXT**
9.  PostgreSQL is ready to be installed: => **Ready To Install** ===> click on **NEXT**
10. The installer will confirm completion when the process completes:
    **Completing PostreSQL setup wizard :**
    **Untick on it** ===> Stack Builder may be used to download and install the additional tools,
    drivers and applications to complement your postgreSQL Installation.
    ===> click on **FINISH**
11. Search on task Bar for **PgAdmin4** ===> click on it, it will going to **launch**
12. Dialogue Box : Please enter the enter your master password
    This is required to unlock saved password and reconnect to the database server
    **\*Note : Set passowrd for Pgadmin4**
13. Once set then click on **Servers** : (Note : Enter the **superuser's** password i.e. for **postgres**[superuser])
    Please enter the password for the user "Postgres" to connect the server 'PostgreSQL15'  
     **Password :** Enter the superuser password (see the 5th point)

14. Creating DataBase on PostgreSQL : tree format ===> Servers (1) --  
     |
    PostgreSQL 15 --
    |
    Databases --- click on it
    |
    Create
    |
    Database
    |
    Database: **incomeexpensesdb**
    owner: **postgres**
    click on it: **save**

15. **Setting Database Section**

    Go to your project **MyExpencesOnIncome** Then click on app **MyExpencesOnIncome**, Inside this application there is a file
    settings.py where all settings we can do easily.

         cd  MyExpencesOnIncome/MyExpencesOnIncome/settings.py

         **Then search for Database section** and make changes as per your database.**

         DATABASES = {
            'default': {
                'ENGINE': 'django.db.backends.postgresql',
                'NAME': 'incomeexpensesdb',
                'USER': 'postgres',
                'PASSWORD': '********',
                'HOST': 'localhost',
              }
         }

         **Important Note: ====> Security ====> But for security purpose we can't keep our database info openly So we create an .evn file outside the application of MyExpencesOnInmcome , that is on projectfile and set all as a variable then that variable we call here as a connection string**


         So , first of all we need to import a module on settings.py file on the top of the file.

         On settings.py ====> import os ====> this module helps to operating system.

         ***Note:===> import os ====> The functions OS module provides allows us to operate on underlying Operating System tasks, irrespective of it being a Windows Platform, Macintosh or Linux.**

         import os    <=== on top of settings.py

         DATABASES = {
            'default': {
                'ENGINE': 'django.db.backends.postgresql',
                'NAME': os.environ.get('DB_NAME'),
                'USER': os.environ.get('DB_USER'),
                'PASSWORD': os.environ.get('DB_USER_PASSWORD'),
                'HOST': os.environ.get('DB_HOST'),
              }
         }

         .evn file ===> we export all variable then that variable_name call on settings.py

          export Variable_name=Value_of_variable

         export DB_NAME=incomeexpensesdb
         export DB_USER=postgres
         export DB_USER_PASSWORD=********
         export DB_HOST=localhost

         ***Note:====> os.environ.get ====> This module provides a portable way of using operating system dependent functionality. os. environ in Python is a mapping object that represents the user's environmental variables. It returns a dictionary having user's environmental variable as key and their values as value.**

16. **Run the Server** ===>

    python manage.py runserver

    **\*ERROR: Error loading psycopg2 module: No module name 'psycopg2'**

**\*for postgresql connectivity**

     pip install psycopg2

**\*Note : Psycopg2 is a PostgreSQL database driver, it is used to perform operations on PostgreSQL using python, it is designed for multi-threaded applications.**
