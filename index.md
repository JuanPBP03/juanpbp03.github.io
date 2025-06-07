---
layout: posts
title: "Hey, I'm Juan!"
tagline: "I built this site to showcase my projects, explore new ideas, and share my thoughts. It's part blog, part portfolio, and 100% me."
permalink: /
header:
  overlay_image: /assets/images/banner.jpg
  actions:
    - label: Site Repo
      url: https://github.com/juanpbp03/juanpbp03.github.io
    - label: My Resume
      url: /assets/files/JuanPBP-Resume.pdf
author_profile: true
entries_layout: grid
---

<div style="display: flex; justify-content: space-between; align-items: center;">
  <h1>Latest Posts</h1>
  <a href="/blog" class="btn btn--primary btn--small">View All</a>
</div>
<hr style="margin-top: 0;">
<section class="grid__wrapper">
  <div class="entries-grid" style="clear: both; overflow: hidden;">
    {% for post in site.posts limit: 3 %}
      {% include archive-single.html type="grid" %}
    {% endfor %}
  </div>
</section>


<div style="display: flex; justify-content: space-between; align-items: center;">
  <h1>Latest Projects</h1>
  <a href="/portfolio" class="btn btn--primary btn--small">View All</a>
</div>
<hr style="margin-top: 0;">
<section class="grid__wrapper">
  <div class="entries-grid" style="clear: both; overflow: hidden;">
    {% for post in site.portfolio limit: 3 %}
      {% include archive-single.html type='grid' %}
    {% endfor %}
  </div>
</section>
<hr style="margin: 2rem 0;">



