---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=37' | relative_url }}">
{% include nav.html %}

---

<section class="section-box personal-section">
  <div class="personal-header">
    <span class="personal-eyebrow">Beyond research</span>
    <h2 class="section-title">Photography</h2>
    <p class="subtext photo-caption">I enjoy capturing moments with my camera. <a class="photo-link no-underline" href="https://www.flickr.com/photos/203606562@N02/" target="_blank" rel="noopener">See more of my photos <i class="fas fa-arrow-right" style="font-size:0.72em;"></i></a></p>
  </div>

  <div class="photo-carousel">
    <div class="carousel-stage">
      <div class="carousel-side carousel-side-prev">
        <div class="carousel-dots" id="dots-prev" aria-label="Previous photos"></div>
        <button class="carousel-arrow carousel-prev" type="button" aria-label="Previous photo">
          <i class="fas fa-chevron-left"></i>
        </button>
      </div>

      <figure class="photo-frame">
        <img id="carousel-image" src="assets/css/img/photos/Col_1.webp" alt="Photography by Nikolas Xiros" width="1400" height="935" fetchpriority="high">
      </figure>

      <div class="carousel-side carousel-side-next">
        <button class="carousel-arrow carousel-next" type="button" aria-label="Next photo">
          <i class="fas fa-chevron-right"></i>
        </button>
        <div class="carousel-dots" id="dots-next" aria-label="Next photos"></div>
      </div>
    </div>
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

  const SIDE = 3; // dots shown on each side of the photo
  const img = document.getElementById('carousel-image');
  const prevWrap = document.getElementById('dots-prev');
  const nextWrap = document.getElementById('dots-next');
  let index = 0;

  function wrap(i) {
    return (i % photos.length + photos.length) % photos.length;
  }

  function buildDots(container, offsets) {
    container.innerHTML = '';
    offsets.forEach(function (offset) {
      const target = wrap(index + offset);
      const dot = document.createElement('button');
      dot.type = 'button';
      dot.className = 'carousel-dot';
      // Nearer photos read as more prominent.
      dot.classList.add('step-' + Math.min(Math.abs(offset), SIDE));
      dot.setAttribute('aria-label', 'Go to photo ' + (target + 1) + ' of ' + photos.length);
      dot.addEventListener('click', function () { show(target); });
      container.appendChild(dot);
    });
  }

  function renderDots() {
    // Left column counts back from the photo, right column counts forward.
    buildDots(prevWrap, [-3, -2, -1]);
    buildDots(nextWrap, [1, 2, 3]);
  }

  // Warm the neighbours so arrow clicks feel instant.
  function preload(i) {
    const pre = new Image();
    pre.src = photos[wrap(i)];
  }

  function show(next) {
    index = wrap(next);
    img.classList.add('is-swapping');
    const loader = new Image();
    loader.onload = function () {
      img.src = photos[index];
      img.classList.remove('is-swapping');
    };
    loader.src = photos[index];

    renderDots();
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
  const stage = document.querySelector('.photo-carousel');
  stage.addEventListener('touchstart', function (e) { touchX = e.changedTouches[0].clientX; }, { passive: true });
  stage.addEventListener('touchend', function (e) {
    if (touchX === null) { return; }
    const delta = e.changedTouches[0].clientX - touchX;
    if (Math.abs(delta) > 45) { show(delta < 0 ? index + 1 : index - 1); }
    touchX = null;
  }, { passive: true });

  show(0);
})();
</script>
