---
layout: page
permalink: /teaching/
title: teaching
description: classes, workshops, and teaching material
nav: true
---
<h4 class="mt-4">Lexington Youth STEM Team</h3>
<div class="projects">
{% assign sorted_teaching = site.teaching | where:"affiliation","lex" | sort: "semester_index" | reverse %}
{% for teaching in sorted_teaching %}
    {% include teaching.html %}
{% endfor %}
</div>

<h4 class="mt-4">The University of Massachusetts, Boston</h3>
<div class="projects">
{% assign sorted_teaching = site.teaching | where:"affiliation","umb" | sort: "semester_index" | reverse %}
{% for teaching in sorted_teaching %}
    {% include teaching.html %}
{% endfor %}
</div>
