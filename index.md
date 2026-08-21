---
title: "Home"
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=34' | relative_url }}">
<link rel="preload" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" as="style" onload="this.onload=null;this.rel='stylesheet'">
<noscript><link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet"></noscript>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" media="print" onload="this.media='all'">
<noscript><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"></noscript>

{% include nav.html %}

---

<section class="hero-banner">
  <div class="hero-inner has-pic">
    <aside class="profile-side">
      <img src="/assets/css/img/mine/pic2.webp" alt="Nikolas Xi̱ros" class="hero-pic" width="215" height="215" fetchpriority="high">
      <div class="profile-info">
        <h2 class="profile-name">Nikolas Xi̱ros</h2>
        <p class="profile-role">AI Researcher @ ISLP, Athena RC</p>
        <p class="profile-location"><i class="fas fa-map-marker-alt"></i> Athens, Greece</p>

        <div class="profile-links">
          <a href="https://github.com/nickxir12" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a>
          <a href="https://www.linkedin.com/in/nikolaos-xiros-972b531a7" target="_blank" rel="noopener" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
          <a href="https://scholar.google.com/citations?user=gxXUPUkAAAAJ&hl=el" target="_blank" rel="noopener" aria-label="Google Scholar"><i class="fas fa-graduation-cap"></i></a>
          <a href="mailto:nikolasxiros2002@gmail.com" aria-label="Email"><i class="fas fa-envelope"></i></a>
        </div>
      </div>
    </aside>

    <div class="hero-content">
      <h1>Hi, I'm Nikolas </h1>
      <p class="tagline">AI & Multimodal Learning Researcher</p>
      <p class="subtext">
      As a Associate Researcher at the Athena Research Center and a recent graduate in Electrical and Computer Engineering from the National Technical University of Athens, I’m passionate about Machine Learning and Natural Language Processing.
      <br><br>
      My research interests involve investigating the reasoning capabilities of NLP and VLM models, designing interpretability algorithms, and enhancing the safety and reliability of AI systems. Beyond technical development, I am dedicated to analyzing how AI interacts with society by evaluating fairness, transparency, and ethical implications in real-world deployment scenarios.
      </p>

      <h3 class="news-heading">News</h3>
      <div class="news-section">
        <div class="news-item">
          <span class="news-date">August 2026</span>
          <p>Our paper <strong>"Beyond Magnitude: Contrastive Routing for Modular Mixture-of-Experts"</strong> was accepted at EMNLP 2026 Main Conference</p>
        </div>
        <div class="news-item">
          <span class="news-date">October 2025</span>
          <p>Started research internship in ISLP, Athena RC</p>
        </div>
        <div class="news-item">
          <span class="news-date">October 2025</span>
          <p>Graduated from ECE-NTUA with honors</p>
        </div>
      </div>
    </div>
  </div>
</section>
