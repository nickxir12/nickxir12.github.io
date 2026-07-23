---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=30' | relative_url }}">
{% include nav.html %}

---

<section class="section-box personal-section">
  <div class="personal-header">
    <span class="personal-eyebrow">Beyond research</span>
    <h2 class="section-title">Photography</h2>
    <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/" target="_blank" rel="noopener">See more of my photos <i class="fas fa-arrow-right" style="font-size:0.72em;"></i></a></p>
  </div>

  <figure class="photo-frame">
    <img id="carousel-image" src="assets/css/img/photos/Col_1.webp" alt="Photography by Nikolas Xiros" loading="lazy" width="760" height="570">
  </figure>

  <figure class="pull-quote">
    <blockquote>If you look for a meaning, you'll miss everything that happens.</blockquote>
    <figcaption>— Andrei Tarkovsky</figcaption>
  </figure>
</section>

<script>
  const photos = [
    'assets/css/img/photos/Col_1.webp',
  ];
  const randomIndex = Math.floor(Math.random() * photos.length);
  document.getElementById('carousel-image').src = photos[randomIndex];
</script>
