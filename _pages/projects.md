---
layout: page
title: projects
permalink: /projects/
description: some of the projects I have worked on.
nav: true
display_categories: [work, fun]
horizontal: true
---
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{category}}</h2>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-1">
          {% for project in sorted_projects %}
            {% include projects_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        {% for project in sorted_projects%}
        <div class="card mt-3">
            <div class="p-3">
              <div class="row">
                <div class="col-sm-2 text-left text-sm-right">
                  <span class="badge font-weight-bold global-theme-block text-uppercase align-middle">
                    <!-- {{ project.date}} -->
                  </span>
                </div>
                <div class="col-sm-6">
                  <h5 class="font-weight-bold">{{ project.title}}</h5>
                  <h6 class="font-italic mt-2 mt-sm-0">Yong Zhuang, Matt, Wei Ding</h6>
                  <article>
                    {{ project.description }}
                  </article>
                </div>
                <div class="col-sm-4">
                  <img src="{{ project.img | relative_url }}" alt="project thumbnail">
                </div>
              </div>
            </div>
        </div>
        {% endfor %}
      {% endif %}
    {% endfor %}

  {% else %}
  <!-- Display projects without categories -->
    {% assign sorted_projects = site.projects | sort: "start" | reverse%}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
        {% for project in sorted_projects%}
        <a href="{{ project.url | relative_url }}">
        <div class="card mt-3">
            <div class="p-3">
              <div class="row">
                <!-- <div class="col-sm-2 text-left text-sm-left">
                  <span class="badge font-weight-bold global-theme-block text-uppercase align-middle">
                    {{ project.start}}
                  </span>
                </div> -->
                <div class="col-sm-9">
                  <h4 class="font-weight-bold">{{ project.title}}</h4>
                  <h6 class="font-italic mt-2 mt-sm-0">{{project.collaborators}}</h6>
                  <article>
                    {{ project.description }}
                  </article>
                </div>
                <div class="col-sm-3">
                  <img src="{{ project.img | relative_url }}" alt="project thumbnail">
                </div>
              </div>
            </div>
        </div>
        </a>
        {% endfor %}
    {% else %}
      <div class="grid">
        {% for project in sorted_projects %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}

</div>
