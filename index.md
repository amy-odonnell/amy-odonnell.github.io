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
  {% assign thumbnails = "" | split: "" %}

  {% for post in recent_posts %}
    {% assign thumbnails = thumbnails | push: 
      {
        "title": post.title,
        "excerpt": post.excerpt,
        "url": post.url,
        "image_path": post.image,
        "btn_label": "Read more",
        "btn_class": "btn--primary"
      } 
    %}
  {% endfor %}

  {% include feature_row items=thumbnails %}
</section>
