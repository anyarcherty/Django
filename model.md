# model

1. differentiate null=True, blank=True in django

   `null=True` sets NULL (versus NOT NULL) on the column in your DB. 
   
   `Blank values` for Django field types such as DateTimeField or ForeignKey will be stored as NULL in the DB.
   
   `blank=True` determines whether the field will be required in forms. If `blank=True` then the field will not be required, whereas if it's `False` the field cannot be blank.
   
   The combo of the two is so frequent because typically if you're going to allow a field to be blank in your form, you're going to also need your database to allow NULL values for that field. The exception is CharFields and TextFields, which in Django are never saved as NULL. Blank values are stored in the DB as an empty string ('').
   
   `CHAR` and `TEXT` types are `never` saved as `NULL` by Django, so null=True is unnecessary. 
   However, you can manually set one of these fields to None to force set it as NULL. If you have a scenario where that might be necessary, you should still include null=True.


   Simply `null=True` defines database should `accept NULL values`, on other hand `blank=True` defines on `form validation` this field should accept blank values or not(If blank=True it accept form without a value in that field and blank=False[default value] on form validation it will show This field is required error.
   
   https://stackoverflow.com/questions/8609192/differentiate-null-true-blank-true-in-django

2. make migration of field in models

     change the field
     
     `publisher = models.CharField(max_length = 50)` to `publisher = models.CharField(max_length = 50, null=True)`
     
     open terminal 
     
     `python3 manage.py makemigrations` 
     
     check the file in migration folder to see the different, if all is right
     
     `python3 manage.py migrate` confirm migrate
