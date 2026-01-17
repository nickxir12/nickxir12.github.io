---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=10' | relative_url }}">
{% include nav.html %}

---

<section class="section-box">
  <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/">See more of my photos</a></p>
  <div class="photo-single">
    <img id="random-image" src="assets/css/img/photos/Col_1.jpg" alt="Photography">
  </div>
</section>

<script>
  // Array of all photo paths
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

  // Pick a random photo on page load
  const randomIndex = Math.floor(Math.random() * photos.length);
  document.getElementById('random-image').src = photos[randomIndex];
</script>

