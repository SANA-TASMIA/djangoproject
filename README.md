# djangoproject


MyExpencesOnIncome this is an entity of project. Here we create a dashboard by using django framework. 

Here I am creating a dashboard which shows the expenses and income. Also connecting with PostgreSQL and charts of python.

***Uploading project on github from git(working dir)**

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

***Installation :**

Step 1. Install python latest version by using https://www.python.org/downloads/ 

Step 2. while installing tick on add PATH. So, you no need to set path manually.

Step 3. click on advanced and tick on pip while installation.

Step 4. For Django installation, use below command

       pip freeze
       pip install django

*Create a project :

Step 1. create folder for project
open CMD :

                 d:
                 mkdir djangoproject
                 django-admin
                 django-admin startproject name_of_project

            e.g.  django-admin startproject MyExpencesOnIncome

***Run the Server:  **          

Step 1. Run the server

     open CMD :  a) python manage.py runserver

    *Note: Default port no. is 8000

    OR

Step 1. (Optional) To change the port

    open CMD : a) python manage.py runserver 4444
        *Note: Port will be change from 8000 to 4444.

***Create the three folder      **  

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
               
***for postgresql connectivity**

            pip install psycopg2               
               
               
