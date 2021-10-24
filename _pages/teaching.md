---
layout: page
permalink: /teaching/
title: teaching
description: classes, workshops, and teaching material
nav: true
---

<h3 class="mt-4">The University of Massachusetts, Boston</h3>
<div class="projects">
{% assign sorted_teaching = site.teaching | sort: "semester_index" | reverse %}
{% for teaching in sorted_teaching %}
    {% include teaching.html %}
{% endfor %}
</div>
