---
title: "Projects"
permalink: /projects.html
---


<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=39' | relative_url }}">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/academicons/1.9.4/css/academicons.min.css">

{% include nav.html %}

---

<!-- ---
<section class="section-box">
  <h1>Projects</h1>
  <h3>Spirob Robot Modeling</h3>
  <p>Neural network–based dynamic modeling and control integration for a soft robot arm.</p>

  <h3>Computer Vision and Language Alignment</h3>
  <p>Exploring cross-modal representations between text and images using CLIP and DINO.</p>
</section> -->

<!-- <section class="hero-banner">
  <div class="hero-inner">
    <div class="hero-content">
      <h1>Projects</h1>
    </div>
  </div>
</section> -->

<section class="section-box">
  <div class="project-list">
    <div class="project-card card">
      <h3>More Capable, Less Faithful: A Multilingual Analysis of Mathematical (Un)Solvability Detection in LLMs</h3>
      <p>The first multilingual benchmark of paired solvable and unsolvable math problems, extending ReliableMath to French and Greek. Solvability is encoded as a largely language-agnostic feature, yet higher-resource languages like English are less faithful at flagging unsolvable problems.</p>
      <p class="conference-note">Accepted at MRL Workshop @ EMNLP 2026.</p>
      <div class="paper-links">
        <a class="paper-link" href="https://arxiv.org/abs/2608.30463" target="_blank" rel="noopener" title="arXiv preprint" aria-label="arXiv preprint"><i class="ai ai-arxiv"></i></a>
      </div>
    </div>

    <div class="project-card card">
      <h3>Disentangling Knowledge and Verbalization in LLMs</h3>
      <p>Paper showing that LLMs encode <em>knowing</em> a math problem is unsolvable separately from <em>saying</em> so, as distinct linearly decodable directions.</p>
      <div class="paper-links">
        <a class="paper-link" href="https://arxiv.org/abs/2607.05013" target="_blank" rel="noopener" title="arXiv preprint" aria-label="arXiv preprint"><i class="ai ai-arxiv"></i></a>
      </div>
    </div>

    <div class="project-card card">
      <h3>Contrastive Routing for Mixture-of-Experts</h3>
      <p>Instead of routing on absolute magnitude, CoRM contrasts each token against an EMA of the layer's hidden states, concentrating the routing signal onto a low-dimensional separable subspace.</p>
      <p class="conference-note">Accepted at EMNLP 2026 (Main).</p>
      <div class="paper-links">
        <a class="paper-link" href="https://arxiv.org/abs/2609.01100" target="_blank" rel="noopener" title="arXiv preprint" aria-label="arXiv preprint"><i class="ai ai-arxiv"></i></a>
      </div>
    </div>

    <div class="project-card card">
      <h3>Vision and Language Representational Alignment</h3>
      <p><em>Master's Thesis</em></p>
      <p>Exploring cross-modal representations between text and images using CLIP and DINOv2 models.</p>
    </div>

    <div class="project-card card">
      <h3>Multimodal Sentiment Analysis</h3>
      <p><em>Segregate, Refine, Integrate: Decomposing Multimodal Fusion for Sentiment Analysis</em></p>
      <p class="conference-note">Accepted at Interspeech 2026.</p>
      <div class="paper-links">
        <a class="paper-link" href="https://arxiv.org/abs/2607.12686" target="_blank" rel="noopener" title="arXiv preprint" aria-label="arXiv preprint"><i class="ai ai-arxiv"></i></a>
      </div>
    </div>

    <div class="project-card card">
      <h3>SpiRob Robot Modeling</h3>
      <p>Project developed during summer internship at USTC, China. I developed a neural network–based dynamic modeling and control integration for a novel soft robot.</p>
    </div>
  </div>
</section>