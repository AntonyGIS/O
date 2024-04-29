<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Image Slider</title>
<style>
    body, html { margin: 0; padding: 0; }
    .header-image {
        width: 100%;
        height: 300px; /* Adjust this value as needed */
        object-fit: cover; /* Ensures the image covers the area without stretching */
        display: block;
    }
</style>
</head>
<body>
<img id="headerImage" class="header-image" src="https://www.marionfl.org/home/showpublishedimage/22630/637483908880470000" alt="Header Image">

<script>
    const images = [
        "https://www.marionfl.org/home/showpublishedimage/22630/637483908880470000", // Image 1
        "https://www.blueskyinsure.com/images/logo-national-flood-insurance-program.png", // Image 2
        "https://www.marionfl.org/home/showpublishedimage/24853/638464565853830000" // Image 3
    ];
    let currentIndex = 0;

    function changeImage() {
        currentIndex = (currentIndex + 1) % images.length;
        document.getElementById('headerImage').src = images[currentIndex];
    }

    setInterval(changeImage, 5000); // Change image every 5 seconds
</script>
</body>
</html>
