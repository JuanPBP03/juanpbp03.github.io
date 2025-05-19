---
layout: splash
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
---
# Latest Posts
---
{: .text-center}

<section class="grid__wrapper">
  <div class="entries-grid" style="clear: both; overflow: hidden;">
    {% for post in site.posts limit: 4 %}
      {% include archive-single.html type="grid" %}
    {% endfor %}
  </div>
</section>

# Latest Projects

---

<section class="grid__wrapper">
  <div class="entries-grid" style="clear: both; overflow: hidden;">
    {% for post in site.portfolio limit: 4 %}
      {% include archive-single.html type="grid" %}
    {% endfor %}
  </div>
</section>


