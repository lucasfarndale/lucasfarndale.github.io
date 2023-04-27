---
layout: page
title: projects
permalink: /projects/
description: Predicting the prognosis of a patient with potentially cancerous growth is extremely difficult. Classical supervised machine learning requires large datasets with pre-scored ground truth labels, however these simply do not exist for many cancers and pre-cancerous growths, such as colorectal polyps. My work uses a set of emerging but relatively untested self-supervised machine learning techniques to investigate whether there exist as yet undiscovered features in pathology stains which can be used to predict cancer prognosis. These techniques require far less data than supervised methods, and no data labelling, leaving them free from human preconception, error, and bias. 

My work focuses mainly on cancer, however, the methods developed are broadly applicable to other areas of image analysis, both in medicine and further afield. I'm also working on the integration of multiple different data modalities, particularly -omics data, and methods of extracting information from digital pathology slides at different magnifications.
nav: true
nav_order: 2
display_categories: [PhD, Other]
horizontal: false
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
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
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
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
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
{%- endif -%}
</div>
