---
layout: splash
title: "Amy O'Donnell"
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/coverconcretewall.jpg
  caption: "Photo credit: [**freepik**](https://www.freepik.com)"
  actions:
    - label: "About Me"
      url: "/about/"
      class: "btn btn--primary"
    - label: "View Posts"
      url: "/posts/"
      class: "btn btn--primary"
    - label: "Let’s Connect"
      url: "/contact/"
      class: "btn btn--primary"
excerpt: >
  <img src="/assets/images/bio-photo.jpg" style="border-radius: 50%; width: 150px; margin-bottom: 10px;"><br>
  Digital Inclusion · Social Impact · Ethical Tech  
  <br>
  I'm a digital inclusion and online safety expert shaping ethical technology to benefit society.
---

<section class="recent-posts" style="margin-top: 3rem;">
  <h2>Recent Posts</h2>

  {% assign recent_posts = site.posts | slice: 0, 3 %}

  <div class="entries-plain">
    {% for post in recent_posts %}
      <article class="archive__item">
        <h3 class="archive__item-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        {% if post.excerpt %}
          <p class="archive__item-excerpt">
            {{ post.excerpt | strip_html | truncate: 160 }}
          </p>
        {% endif %}
        <p><a href="{{ post.url | relative_url }}" class="btn btn--primary">Read more</a></p>
      </article>
    {% endfor %}
  </div>
</section>

