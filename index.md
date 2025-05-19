---
layout: posts
title: "Welcome to my website!"
tagline: "This site is powered by Jekyll, hosted  on GitHub Pages, and customized with Markdown, YAML, HTML, and Liquid, all version-controlled and deployed with GitHub Actions."
permalink: /
header:
  overlay_image: /assets/images/banner.jpg
  actions:
    - label: View on GitHub
      url: https://github.com/juanpbp03/juanpbp03.github.io
    - label: Download My Resume
      url: /assets/files/JuanPBP-Resume.pdf
author_profile: true
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
      {% include archive-single.html type="grid" %}
    {% endfor %}
  </div>
</section>
<hr style="margin: 2rem 0;">



