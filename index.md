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

# Latest Uploads
{: .text-center}
--- 
{% assign docs = site.documents %}
<div class="entries-grid">
{%- for post in docs limit: 6-%}
  {% include archive-single.html type="grid" %}
{%- endfor -%}
</div>