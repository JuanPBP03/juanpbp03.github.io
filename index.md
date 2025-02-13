---
layout: splash
title: "Welcome to My Portfolio"
permalink: /
header:
  overlay_image: /assets/images/banner.jpg
  overlay_filter: 0 # Adjust darkness (0 = none, 1 = full black)
  caption: "Your tagline or intro text here."
---

<section class="latest-posts">
  <h2>Latest Posts</h2>
  <ul>
    {% for post in site.posts limit:3 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <p>{{ post.date | date: "%B %d, %Y" }} – {{ post.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</section>

<section class="latest-projects">
  <h2>Latest Projects</h2>
  <ul>
    {% for project in site.projects limit:3 %}
      <li>
        <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
        <p>{{ project.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</section>