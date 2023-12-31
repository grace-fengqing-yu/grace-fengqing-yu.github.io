---
layout: page
title: projects
permalink: /projects/
description: Projects that I have worked on.
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: true
---

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row">
      {%- for project in sorted_projects -%}
        <div class="col-md-12">
          {% include projects_customized.html %}
        </div>
      {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row">
      {%- for project in sorted_projects -%}
        <div class="col-md-12">
          {% include projects_customized.html %}
        </div>
      {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects_customized.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
