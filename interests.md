---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=9' | relative_url }}">
{% include nav.html %}

---

<section class="section-box">
  <h3 class="photography-title">Photography</h3>
  <div class="photo-carousel">
    <img id="carousel-image" src="assets/css/img/photos/Col_1.jpg" alt="Photography">
  </div>
  <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/">See some of my photos</a></p>
</section>

<script>
  // Photo carousel
  const photos = [
    'assets/css/img/photos/Col_1.jpg',
    'assets/css/img/photos/Col_2.jpg',
    'assets/css/img/photos/Col_3.jpg',
    'assets/css/img/photos/Col_4.jpg',
    'assets/css/img/photos/Col_5.jpg',
    'assets/css/img/photos/Col_6.jpg',
    'assets/css/img/photos/Col_7.jpg',
    'assets/css/img/photos/Col_8.jpg',
    'assets/css/img/photos/Col_9.jpg',
    'assets/css/img/photos/Bl_1.jpg',
    'assets/css/img/photos/Bl_2.jpg',
    'assets/css/img/photos/Bl_3.jpg',
    'assets/css/img/photos/Bl_4.jpg',
    'assets/css/img/photos/Bl_5.jpg'
  ];

  let currentPhotoIndex = 0;
  const carouselImage = document.getElementById('carousel-image');

  // Preload next image to ensure smooth transition
  function preloadNextImage() {
    const nextIndex = (currentPhotoIndex + 1) % photos.length;
    const img = new Image();
    img.src = photos[nextIndex];
  }

  function changePhoto() {
    // Fade out current image
    carouselImage.style.opacity = '0';

    setTimeout(() => {
      // Update to next photo
      currentPhotoIndex = (currentPhotoIndex + 1) % photos.length;
      carouselImage.src = photos[currentPhotoIndex];
      // Fade in new image
      carouselImage.style.opacity = '1';
      // Preload the next image for smoother subsequent transition
      preloadNextImage();
    }, 300);
  }

  // Preload the first next image
  preloadNextImage();

  // Change photo every 5 seconds
  setInterval(changePhoto, 5000);
</script>

