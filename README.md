# Ex.07 Design of Interactive Image Gallery
## Date:

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
index.html

```
{% load static %}

<!DOCTYPE html>
<html>
<head>
    <title>Interactive Image Gallery</title>

    <style>
        body {
            background: #e5e5e5;
            font-family: Arial;
            text-align: center;
            margin: 0;
        }

        h1 {
            background: darkblue;
            color: white;
            padding: 15px;
        }

        .gallery {
            width: 400px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            margin-top: 80px;
        }

        img {
            width: 300px;
            height: 200px;
            border-radius: 10px;
        }

        button {
            padding: 10px 20px;
            background: blue;
            color: white;
            border: none;
            border-radius: 5px;
            margin: 10px;
            cursor: pointer;
        }

        .footer{
           width: 320px;
           margin: auto;
           margin-top: 120px;
           background: #001f5c;
           color: white;
           padding: 10px;
           border-radius: 8px;
           font-size: 14px;
           font-weight: bold;

        }
    </style>
</head>

<body>

    <h1>Interactive Image Gallery</h1>

    <div class="gallery">

        <img id="image" src="{% static 'images/kid1.png' %}">

        <h3 id="caption">Kid Image 1</h3>

        <br>

        <button onclick="prev()">Previous</button>
        <button onclick="next()">Next</button>

    </div>

    <script>
        let images = [
            "{% static 'images/kid1.png' %}",
            "{% static 'images/kid2.png' %}",
            "{% static 'images/kid3.png' %}",
            "{% static 'images/kid4.png' %}",
            "{% static 'images/kid5.png' %}"
        ];

        let captions = [
            "Kid Image 1",
            "Kid Image 2",
            "Kid Image 3",
            "Kid Image 4",
            "Kid Image 5"
        ];

        let index = 0;

        function next() {
            index++;

            if (index >= images.length) {
                index = 0;
            }

            document.getElementById("image").src = images[index];
            document.getElementById("caption").innerHTML = captions[index];
        }

        function prev() {
            index--;

            if (index < 0) {
                index = images.length - 1;
            }

            document.getElementById("image").src = images[index];
            document.getElementById("caption").innerHTML = captions[index];
        }
    </script>
    <div class="footer">
       Designed & Developed by MIRDULA D (25014905)
    </div>

</body>
</html>
```

## OUTPUT:
![alt text](<gallapp/Screenshot 2026-05-23 214529.png>)
![alt text](<gallapp/Screenshot 2026-05-23 214540.png>)
![alt text](<gallapp/Screenshot 2026-05-23 214558.png>)
![alt text](<gallapp/Screenshot 2026-05-23 214612.png>)
![alt text](<gallapp/Screenshot 2026-05-23 214627.png>)


DEVELOPED BY: MIRDULA D
REGISTRATION NO. 212225040234

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
