# model

1. differentiate null=True, blank=True in django

   `null=True` sets NULL (versus NOT NULL) on the column in your DB. 
   
   `Blank values` for Django field types such as DateTimeField or ForeignKey will be stored as NULL in the DB.
   
   `blank=True` determines whether the field will be required in forms. If `blank=True` then the field will not be required, whereas if it's `False` the field cannot be blank.
   
   The combo of the two is so frequent because typically if you're going to allow a field to be blank in your form, you're going to also need your database to allow NULL values for that field. The exception is CharFields and TextFields, which in Django are never saved as NULL. Blank values are stored in the DB as an empty string ('').
   
   `CHAR` and `TEXT` types are `never` saved as `NULL` by Django, so null=True is unnecessary. 
   However, you can manually set one of these fields to None to force set it as NULL. If you have a scenario where that might be necessary, you should still include null=True.
