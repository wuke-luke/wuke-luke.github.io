---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am currently pursuing my Ph.D. in Computer Science at Fudan University, fortunate to be advised by Prof. Wenchao Ding and to have many wonderful collaborators. My current research focuses on Embodied AI and Harness-level RSI.

## Research Interests

- Embodied AI
- Dexterous Manipulation
- Harness-level RSI
- 3D Vision

## Experience

<div class="exp-row">
  <img src="/images/tars.png" alt="TARS Robotics" class="exp-logo">
  <div class="exp-body">
    <strong>Research Intern</strong>, TARS Robotics, Feb. 2025 – Sep. 2026<br>
    World Action Models (WAM) &amp; ACWM hybrid architecture; dexterous hand manipulation with reinforcement learning; RSI Agent.
  </div>
</div>

<div class="exp-row">
  <img src="/images/dji.svg" alt="DJI" class="exp-logo">
  <div class="exp-body">
    <strong>Research Intern</strong>, DJI, Jun. 2024 – Sep. 2024<br>
    Autonomous driving simulation based on 3D Gaussian Splatting (3DGS) and diffusion models; pretraining for monocular / binocular depth estimation.
  </div>
</div>

## Honors and Awards

- National Scholarship for Ph.D. Students (Top 1%)
- National Scholarship for Undergraduate Students (Top 1%)
- National First Prize ×3, Chinese College Intelligent Vehicle Competition (Smart Transportation / Smart Logistics / Outdoor Driving Groups)

## Publications

{% include base_path %}
{% for category in site.publication_category %}
  {% assign title_shown = false %}
  {% for post in site.publications reversed %}
    {% if post.category != category[0] or post.first_author != true %}
      {% continue %}
    {% endif %}
    {% unless title_shown %}
<h3 class="pub-category-title">{{ category[1].title }}</h3>
      {% assign title_shown = true %}
    {% endunless %}
    {% include archive-single.html %}
  {% endfor %}
  {% for post in site.publications reversed %}
    {% if post.category != category[0] or post.first_author == true %}
      {% continue %}
    {% endif %}
    {% unless title_shown %}
<h3 class="pub-category-title">{{ category[1].title }}</h3>
      {% assign title_shown = true %}
    {% endunless %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
