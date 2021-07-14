# Django_Interview_Prep


#Django ORM 

1.Created Virtual Env.
2. pip install django
3. django-admin startproject BasicORM

4.cd BasicORM

5.python manage.py startapp College

6.BasicORM-->settings.py INSTALLED_APPS=['College']

7. College --> models.py

#Create your models here.
class student(models.Model):
    name=models.CharField(max_length=12)
    age=models.IntegerField()
    rollno=models.IntegerField()

    def __str__(self):
        return str(self.name)
        
8.College--> admin.py

from College.models import student

#Register your models here.

admin.site.register(student)

9. python manage.py migrate

10. python manage.py makemigrations

11.python manage.py createsuperuser

Email address: jeevanchavan143@gmail.com
Password:
Password (again):
Superuser created successfully.

12. python manage.py runserver  127.0.0.1:7000

Open Browser:  127.0.0.1:7000/Admin 
Enter Credentials
Add Data to student table

13. python manage.py shell 
>> from College.models import student
>>student.objects.all()




