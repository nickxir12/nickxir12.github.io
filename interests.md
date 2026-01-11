---
title: "  Personal"
permalink: /Personal.html
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css?v=6' | relative_url }}">
{% include nav.html %}

---



<!-- Writing block (separate .section-box, stacked like projects) -->
<section class="section-box project-card">
  <div class="main-content">
    <h2>Writing</h2>
    <p class="subtext">I write short blogs and notes about AI and more.</p>
    <a class="subtext photo-link" href="https://medium.com/">Read blog →</a>
  </div>
</section>

<!-- Photos block (separate .section-box, stacked below Writing) -->
<section class="section-box project-card">
  <div class="main-content">
    <h2>Photography</h2>
    <p class="subtext">I try to capture moments with my camera.</p>
    <a class="subtext photo-link" href="https://www.flickr.com/people/203606562@N02/">See some of my photos here →</a>
  </div>
      <!-- <div class="photo-grid" style="max-width:900px;margin:1rem auto 0;">
        {% assign gallery = site.static_files | where_exp:"file","file.path contains 'assets/css/img/mine/photos/'" %}
        {% if gallery and gallery.size > 0 %}
          {% for file in gallery %}
            {% assign thumb_candidates = site.static_files | where:"name", file.name %}
            {% assign thumb = thumb_candidates | where_exp:"t","t.path contains 'assets/css/img/mine/photos/thumbs/'" | first %}
            {% if thumb %}
              {% assign img_src = thumb.path %}
            {% else %}
              {% assign img_src = file.path %}
            {% endif %}
            <a class="photo-item" href="{{ file.path | relative_url }}">
              <img src="{{ img_src | relative_url }}" loading="lazy" alt="Photo {{ forloop.index }}">
            </a>
          {% endfor %}
        {% else %}
          <p class="subtext">No photos found in <code>assets/img/photos/</code> or <code>assets/css/img/mine/photos/</code>. Make sure images are committed.</p>
        {% endif %}
      </div> -->
</section>
