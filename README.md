# Ex.08 Design of Interactive Image Gallery
# Date:18/11/2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: rgb(70, 69, 69);
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            height: 100vh;
        }

        .gallery {
            display: flex;
            gap: 20px;
            margin-top: 20px;
        }

        .gallery img {
            width: 200px;
            height: 320px;
            border-radius: 10px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .gallery img:hover {
            transform: scale(1.2);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.8);
        }

        footer {
            margin-top: auto;
            width: 100%;
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            position: relative;
            bottom: 0;
        }

        footer p {
            margin: 0;
            font-size: 14px;
        }

        footer a {
            color: #00bfff;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <br><br><br>
    <div>
        <h1 style="font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif; font-style: italic;color: red; font: size 30px;;">
            Image Gallery
        </h1>
    </div>
    <br><br><br><br><br><br><br><br>
    
    <div class="gallery">
        {% load static %}
        <img src="{% static 'image 1.jpg' %}" alt="Image 1">
        <img src="{% static 'images 2.jpg' %}" alt="Image 2">
        <img src="{% static 'image 3.jpg' %}" alt="Image 3">
        <img src="{% static 'image 4.jpg' %}" alt="Image 4">
        <img src="{% static 'images 5.jpg' %}" alt="Image 5">
    </div>

    <footer>
        <p>&copy; 2024 Chan. All Rights Reserved. <a href="/privacy-policy/">Privacy Policy</a></p>
    </footer>
</body>
</html>

views.py

from django.shortcuts import render
def gallery (request):
    return render(request,'index2.html')

urls.py

from django.contrib import admin 
from django.urls import path 
from gallery import views
urlpatterns = [ 
    path('admin/', admin.site.urls), 
    path('gallery/',views.gallery),
]
```
# OUTPUT:
![Screenshot 2024-12-11 201847](https://github.com/user-attachments/assets/6fb6e329-d2e0-4715-a2e6-f7c14f513aeb)
![Screenshot 2024-12-11 202024](https://github.com/user-attachments/assets/e01bdb9e-3db7-4518-affd-cbe84b2d1b0d)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
