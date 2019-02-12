# Command line by line 

1. Find desktop path
    
    `cd desktop`
    
2. Create Django Folder

    `mkdir django`
    
    `cd django`
    
3. Create project under django folder

    `django-admin startproject ebb`
    
4. Create app under project

    `python manage.py startapp home`
    
5. Change admin folder setting

     view.py
     
6. change name/domain to production level

    ```
    python3 manage.py shell
    from django.contrib.sites.models import Site
    mysite,_=Site.objects.get_or_create(id=2, name='127.0.0.1:8000', domain='127.0.0.1:8000')
    print (mysite.id, mysite.name)
    ```
     `
