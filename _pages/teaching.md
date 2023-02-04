---
layout: page
permalink: /teaching/
title: teaching
description: classes, workshops, and teaching material
nav: true
---
<h3 class="mt-4">Heros Team</h3>
<div class="projects">
{% assign sorted_teaching = site.teaching | where:"affiliation","heros" | sort: "semester_index" | reverse %}
{% for teaching in sorted_teaching %}
    {% include teaching.html %}
{% endfor %}
</div>

<h3 class="mt-4">The University of Massachusetts, Boston</h3>
<div class="projects">
{% assign sorted_teaching = site.teaching | where:"affiliation","umb" | sort: "semester_index" | reverse %}
{% for teaching in sorted_teaching %}
    {% include teaching.html %}
{% endfor %}
</div>
