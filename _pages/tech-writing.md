---
layout: page
title: tech-writing seminar
permalink: /tech-writing/
description: A seminar for students to share good sentences in papers or articles, practice and improve scientific writing skills.
nav: false
horizontal: true
---
<div class="projects">
  <!-- Display projects without categories -->
    {% assign sorted_writings = site.tech-writing | sort: "title" | reverse %}
    <!-- Generate cards for each writing -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-3">
        {% for writing in sorted_writings %}
          {% include tech_writing.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for writing in sorted_writings %}
          {% include tech_writing.html %}
        {% endfor %}
      </div>
    {% endif %}

</div>
