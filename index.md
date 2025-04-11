---
layout: splash
title: "Welcome to my website!"
permalink: /
header:
  overlay_image: /assets/images/banner.jpg
---
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<section class="latest-posts">
  <h2>Latest Posts</h2>
  <ul>
    {% for post in site.posts limit:3 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <p>{{ post.date | date: "%B %d, %Y" }}{{ post.excerpt }}</p>
        <p></p>
      </li>
    {% endfor %}
  </ul>
</section>

<section class="latest-projects">
  <h2>Latest Projects</h2>
  <ul>
    {% for project in site.portfolio limit:3 %}
      <li>
        <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
        <p>{{ project.date | date: "%B %d, %Y" }}{{ project.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</section>

