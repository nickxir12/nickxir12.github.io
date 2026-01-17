---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=6' | relative_url }}">
{% include nav.html %}

---

<section class="section-box">
  <div class="project-list">
    <!-- Writing block -->
    <!-- <div class="project-card card">
      <h3>Writing</h3>
      <p class="subtext">I write short blogs about AI and more. <a class="photo-link" href="https://medium.com/">Read blog</a></p>
    </div> -->

    <!-- Photography block -->
    <div class="project-card card photography-card">
      <h3>Photography</h3>
      <div class="photo-carousel">
        <img id="carousel-image" src="assets/css/img/photos/Col_1.jpg" alt="Photography">
      </div>
      <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/">See some of my photos</a></p>
    </div>
  </div>
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

  function changePhoto() {
    currentPhotoIndex = (currentPhotoIndex + 1) % photos.length;
    carouselImage.style.opacity = '0';

    setTimeout(() => {
      carouselImage.src = photos[currentPhotoIndex];
      carouselImage.style.opacity = '1';
    }, 300);
  }

  // Change photo every 5 seconds
  setInterval(changePhoto, 5000);
</script>

