---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=31' | relative_url }}">
{% include nav.html %}

---

<section class="section-box personal-section">
  <div class="personal-header">
    <span class="personal-eyebrow">Beyond research</span>
    <h2 class="section-title">Photography</h2>
    <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/" target="_blank" rel="noopener">See more of my photos <i class="fas fa-arrow-right" style="font-size:0.72em;"></i></a></p>
  </div>

  <div class="photo-carousel">
    <button class="carousel-arrow carousel-prev" type="button" aria-label="Previous photo">
      <i class="fas fa-chevron-left"></i>
    </button>

    <figure class="photo-frame">
      <img id="carousel-image" src="assets/css/img/photos/Col_1.webp" alt="Photography by Nikolas Xiros" width="1400" height="935" fetchpriority="high">
    </figure>

    <button class="carousel-arrow carousel-next" type="button" aria-label="Next photo">
      <i class="fas fa-chevron-right"></i>
    </button>

    <div class="carousel-dots" id="carousel-dots" role="tablist" aria-label="Choose photo"></div>
  </div>

  <figure class="pull-quote">
    <blockquote>If you look for a meaning, you'll miss everything that happens.</blockquote>
    <figcaption>— Andrei Tarkovsky</figcaption>
  </figure>
</section>

<script>
(function () {
  const base = 'assets/css/img/photos/';
  const photos = [
    'Col_1.webp',
    'Col_3.webp',
    'Col_7.webp',
    'Col_8.webp',
    'Col_9.webp',
    'Bl_1.webp',
    'Bl_2.webp'
  ].map(function (f) { return base + f; });

  const img = document.getElementById('carousel-image');
  const dotsWrap = document.getElementById('carousel-dots');
  let index = 0;

  const dots = photos.map(function (_, i) {
    const dot = document.createElement('button');
    dot.type = 'button';
    dot.className = 'carousel-dot';
    dot.setAttribute('role', 'tab');
    dot.setAttribute('aria-label', 'Photo ' + (i + 1) + ' of ' + photos.length);
    dot.addEventListener('click', function () { show(i); });
    dotsWrap.appendChild(dot);
    return dot;
  });

  // Warm the neighbours so arrow clicks feel instant.
  function preload(i) {
    const pre = new Image();
    pre.src = photos[(i + photos.length) % photos.length];
  }

  function show(next) {
    index = (next + photos.length) % photos.length;
    img.classList.add('is-swapping');
    const loader = new Image();
    loader.onload = function () {
      img.src = photos[index];
      img.classList.remove('is-swapping');
    };
    loader.src = photos[index];

    dots.forEach(function (dot, i) {
      dot.classList.toggle('is-active', i === index);
      dot.setAttribute('aria-selected', i === index ? 'true' : 'false');
    });

    preload(index + 1);
    preload(index - 1);
  }

  document.querySelector('.carousel-prev').addEventListener('click', function () { show(index - 1); });
  document.querySelector('.carousel-next').addEventListener('click', function () { show(index + 1); });

  document.addEventListener('keydown', function (e) {
    if (e.key === 'ArrowLeft') { show(index - 1); }
    else if (e.key === 'ArrowRight') { show(index + 1); }
  });

  // Swipe on touch devices.
  let touchX = null;
  const frame = document.querySelector('.photo-carousel');
  frame.addEventListener('touchstart', function (e) { touchX = e.changedTouches[0].clientX; }, { passive: true });
  frame.addEventListener('touchend', function (e) {
    if (touchX === null) { return; }
    const delta = e.changedTouches[0].clientX - touchX;
    if (Math.abs(delta) > 45) { show(delta < 0 ? index + 1 : index - 1); }
    touchX = null;
  }, { passive: true });

  show(0);
})();
</script>
