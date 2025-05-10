# Ex.08 Design of Interactive Image Gallery
## Date:

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

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

## PROGRAM :
```
file.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>MARVEL</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="marvel.png" height="300px" width="300px">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="marvel1.png" height="300px" width="300px" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="marvel2.png" height="300px" width="300px">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="marvel3.png" height="300px" width="300px">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="marvel5.png" height="300px" width="300px">
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>

style.js
function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
style.css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    text-align: center;
    padding: 20px;
    background-color: #f4f4f4;
}

.gallery {
    display: flex;
    justify-content: center; /* Aligns items horizontally */
    flex-wrap: wrap;         /* Allows wrapping if the row is too long */
    gap: 10px;               /* Space between items */
    padding: 20px;
}

.gallery-item img {
    width: 200px; /* Set image width */
    height: 200px;
    cursor: pointer;
    border: 2px solid #ccc;
    border-radius: 5px;
    transition: transform 0.3s ease;
}

.gallery-item img:hover {
    transform: scale(1.05);
}

```
## OUTPUT:
![image](https://github.com/user-attachments/assets/25175442-7448-4795-a0c0-02b92fa01052)
![image](https://github.com/user-attachments/assets/6760826c-5852-48dc-94e3-2ce3e29df385)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
