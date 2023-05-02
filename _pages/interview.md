---
layout: page
title: interview questions
permalink: /interview/
description: Interview Questions Answered.
nav: false
horizontal: true
---
<div class="projects">
  <!-- Display projects without categories -->
    {% assign sorted_interviews = site.interview | sort: "title" | reverse %}
    <!-- Generate cards for each writing -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-3">
        {% for interview in sorted_interviews %}
          {% include interview.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for interview in sorted_interviews %}
          {% include interview.html %}
        {% endfor %}
      </div>
    {% endif %}

</div>
