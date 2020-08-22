## Making Web Pages in Django

In using django, after creating app and making migrations the next step is to make your application more interactive and user friendly by adding more features in form of pages.

In Django, making Web pages is made up of three steps:

- Defining URLs
- Writing views
- Writing templates

This steps do not follow any order, you can chose to start with any of the steps.

The separation between the steps make it easy to think about each aspect of project and gives better understanding of web development. 
In larger projects, it also allow people focus on their strength.

In this article, I will going through all the steps.


## Step 1

### Writing a View

In Django after running the command python manage.py startapp "name of app"
A views.py file gets generated automatically as part of the files in the application.


![views1.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1598092159889/naawapu_d.png)

The views.py file when it is generated comes with an imported render() function and this function renders response based on the information provided by the views.
The view function works with the request and the request is imported after importing the HttpResponse as seen below

![views2.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1598092336342/_3ZaAaYOW.png)


The views then takes in information from the imported request, prepares it, generates the page and sends it to the browser.

The render function in the views.py takes two arguments, the request and the template used to build the page.

** Example in writing the views for a home page. **

*** Steps: ***

Open the views.py file of the app
Add the following to the file:


 
```
from django.shortcuts import render

def index(request):

"""The home page of appname"""
     return render(request, 'appname/index.html')

``` 

From the above, Django first looks for index(), it passes the request.
Then returns the render().
If the index() have code, it gets processed and returns the render().

## Step 2

### Writing a Template

In Django, the templates allows any data provided in the views to be accessed, it defines how and what the page should look like.

To write a template, first make a folder called templates in the created app, then create a folder call it the appname inside the created templates folder.

![templates1.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1598092554687/BB0IWmrS9.png)

Creating the templates in this way, gives the project a structure easier to understand by django especially in a big projects with different apps.

The files in the templates folder are written in HTML.

Example to create a template for our home page, open the index.html file and write the following:

```
<p> Home Page for my site </p>

<p> We provide the best services at affordable prices </p>

``` 

The first **p** tag opens a paragraph, and the second **p** tag closes a paragraph. 

We have two paragraphs: the first acts as a title, and the second is a description of what the site does.


## Step 3

### Defining URLs


![url2.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1598093773893/uXCLsYzAt.png)

Defining URLs has two steps:

- Url Patterns
- Mapping URLs


### URL Patterns:

This defines the way the URLs are written, It tells Django which page to return when matching a browser request with a  written site URL.

After writing the URLs, each of them then maps to the particular view in which it was written for, the view function gets the data process it and renders the page using the written template which contains the main structure of the page, that is how the page should look like.

### Mapping  URLs

For users to see any page, they do so by entering the URL to the browser.
For django site the URL is:


```
http://localhost:8000
``` 

And it is the base URL and it returns the Django site.

To access the admin site, the URL will have to be mapped to the admin.
It will now be:

```    
 http://localhost:8000/admin
```

In URLs mapping, the URLs needed are decided and defined.

For each app created in a project, a python file called Urls.py is created in the app.

It only gets generated by the root app when the project is created.

Example to define the URL for a home page:

Open the urls.py file
Already some modules have already been imported as the files are generated.


![url1.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1598093839696/Y6q9_Vp3h.png)



The first two lines import a module and a function to manage URLs 
for the admin site. 

The body of the file defines the urlpatterns variable 
In this urls.py file, which represents the project as a whole, the urlpatterns
variable includes sets of URLs from the apps in the project. 
The admin.site.urls, defines all the URLs that can be 
requested from the admin site.

To include the URLs for our app home page we simply do:

```   
from django.contrib import admin
from django.urls import path, include
urlpatterns = [
 path('admin/', admin.site.urls),
 path('', include('appname.urls')),
]

```
The line to include the module appname.urls was added in line  5 
The default urls.py is in the project folder; 

We also need a second URLs.py and this will be created in the app folder.

### Steps:
- Create a python file called URLs.py in the app folder 


![URL.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1598099160009/hx7ZXdzzw.jpeg)

- Add the code below in it

```  
"""Defines URL patterns for appname"""
from django.urls import path
from . import views
app_name = 'appname'
urlpatterns = [
    #Home page
    path('', views.index, name='index')
]

```

From the code above, we first add a docstring at the 
beginning of the file to describe the urls.py we are working on, the **path** function is then imported which is needed in mapping the URLs to the views.
The views is also imported, the **.** in front of the views tells python to import the views.py which is in the same directory as the urls.py module.
The app_name tells django the name of the app it's working on and also to differentiate this urls.py from other urls.py files, urlpatterns variable is a list of individual pages 
that can be requested from the created app.
The path () takes in three arguments.
- a string that enables Django route the request correctly.
- the function to call in the views.py file
- the name index in the URL patterns so it can be referred to in other sections of the code.


> That is all for this article, I hope you enjoy reading this. Kindly like this article or leave a comment.
 Thank you



### References:
- [Cover Photo](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fcomplete-guide-python-django-framework%2F&psig=AOvVaw1Ulz2krgCLiBXzmZg4YWTj&ust=1598184808645000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCODO0NXkrusCFQAAAAAdAAAAABAD)
- [Python Crash course](https://ehmatthes.github.io/pcc/)