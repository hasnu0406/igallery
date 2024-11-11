# Ex.07 Design of Interactive Image Gallery
## Date: 11/11/2024

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
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Heading for the Image Gallery -->
    <h1 class="gallery-heading">Interactive Image Gallery</h1>

    <div class="gallery-container">
        <div class="gallery-item">
            <img src="one.jpg" alt="Image 1">
            <div class="image-name">Sea</div>
        </div>
        <div class="gallery-item">
            <img src="twoo.jpg" alt="Image 2">
            <div class="image-name">Birds</div>
        </div>
        <div class="gallery-item">
            <img src="three.jpg" alt="Image 3">
            <div class="image-name">Cafe</div>
        </div>
        <div class="gallery-item">
            <img src="four.jpg" alt="Image 4">
            <div class="image-name">Vegetables</div>
        </div>
        <div class="gallery-item">
            <img src="piz.jpg" alt="Image 5">
            <div class="image-name">Pizza</div>
        </div>
        <div class="gallery-item">
            <img src="sixx.jpg" alt="Image 6">
            <div class="image-name">Cold Coffee</div>
        </div>
    </div>

    <!-- Modal for displaying the full-size image -->
    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">×</span>
        <img id="modal-image" class="modal-content" alt="Full-size image">
    </div>

    <script src="script.js"></script>
</body>
</html>
```

```

CSS

/* Basic reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Body styling */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    padding: 20px;
}

/* Gallery container */
.gallery-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 columns layout */
    gap: 20px;
    max-width: 1000px;
    margin: 0 auto;
}

/* Gallery item */
.gallery-item {
    position: relative;
    cursor: pointer;
    overflow: hidden;
    border-radius: 8px;
    width: 300px; /* Fixed width */
    height: 200px; /* Fixed height */
}

/* Fixed width and height for the images */
.gallery-item img {
    width: 100%; /* Ensure image fills the container width */
    height: 100%; /* Ensure image fills the container height */
    object-fit: cover; /* Make sure the image covers the container without distortion */
    transition: transform 0.3s ease-in-out;
}

/* Hover effect */
.gallery-item:hover img {
    transform: scale(1.1); /* Slight zoom effect on hover */
}

/* Image name overlay */
.image-name {
    position: absolute;
    bottom: 10px;
    left: 10px;
    background-color: rgba(0, 0, 0, 0.6);
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    font-size: 16px;
    opacity: 0; /* Hide by default */
    transition: opacity 0.3s ease;
}

/* Show image name on hover */
.gallery-item:hover .image-name {
    opacity: 1;
}

/* Modal Styling */
.modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    align-items: center;
    justify-content: center;
}

.modal-content {
    max-width: 90%;
    max-height: 80%;
    margin: auto;
    display: block;
}

.close {
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 36px;
    color: white;
    cursor: pointer;
    z-index: 1001;
}

.close:hover {
    color: #ff6347;
}

```

```

JS

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <div class="gallery-container">
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x200?text=Image+1" alt="Image 1">
            <div class="image-name">Image 1</div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x200?text=Image+2" alt="Image 2">
            <div class="image-name">Image 2</div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x200?text=Image+3" alt="Image 3">
            <div class="image-name">Image 3</div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x200?text=Image+4" alt="Image 4">
            <div class="image-name">Image 4</div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x200?text=Image+5" alt="Image 5">
            <div class="image-name">Image 5</div>
        </div>
        <div class="gallery-item">
            <img src="https://via.placeholder.com/300x200?text=Image+6" alt="Image 6">
            <div class="image-name">Image 6</div>
        </div>
    </div>

    <!-- Modal for displaying the full-size image -->
    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">×</span>
        <img id="modal-image" class="modal-content" alt="Full-size image">
    </div>

    <script src="script.js"></script>
</body>
</html>
```
## OUTPUT:
![exp7](https://github.com/user-attachments/assets/64dd54c1-2bfe-4d4c-9733-6e825b3f6c36)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
