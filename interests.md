---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=24' | relative_url }}">
{% include nav.html %}

---

<section class="section-box">
  <h2 class="section-title" style="text-align: center;">Photography</h2>
  <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/">See more of my photos</a></p>
  <div class="photo-carousel">
    <img id="carousel-image" src="assets/css/img/photos/Col_1.webp" alt="Photography" loading="lazy" width="760" height="570">
  </div>

  <ul class="sayings-list" style="margin-top: 2rem;">
    <li>"If you look for a meaning, you'll miss everything that happens." — Andrei Tarkovsky</li>
  </ul>
</section>

<script>
  const photos = [
    'assets/css/img/photos/Col_1.webp',
  ];
  const randomIndex = Math.floor(Math.random() * photos.length);
  document.getElementById('carousel-image').src = photos[randomIndex];
</script>
