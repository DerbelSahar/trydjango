# trydjango


to setup django envirement: <br/>
```
mkdir trydjango
cd trydjango
python -m venv myenv
myenv\scripts\activate
python -m pip install --upgrade pip
pip install django

```
to check versions:
```
pip freeze

```
create source folder of the project in myenv folder:
```
cd myenv
mkdir src
cd src

```
to create a project called "my project":
```
django-admin startproject myproject .
```
to run the server:
```
python manage.py runserver
```
to sync database:
```
python manage-py migrate
```
to create a superuser:
```
python manage.py createsuperuser
```
to create an app component:
```
python manage.py startapp products
```
add 'products" into settings.p file
then run (every time you make changes in the model):
```
python manage.py makemigrations
python manage.py migrate
```
in admin.py add:
```
from .models import Product
admin.site.register(Product)
```

to open python shell:
```
python manage.py shell
```
in the shell you can create products:
```
from products.models import Product
Product.objects.create(title='new product2',description='new description2',price='22')
```
