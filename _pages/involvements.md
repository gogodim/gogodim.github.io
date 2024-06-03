---
layout: page
title: involvements
permalink: /involvements/
description: A growing collection of your cool involvements.
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

<!-- pages/involvements.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized involvements -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_involvements = site.involvements | where: "category", category %}
  {% assign sorted_involvements = categorized_involvements | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_involvements %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_involvements %}
      {% include involvements.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display involvements without categories -->

{% assign sorted_involvements = site.involvements | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_involvements %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_involvements %}
      {% include involvements.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
