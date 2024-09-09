---
layout: page
title: projects
permalink: /projects/
description: A growing collection of past and current research projects.
nav: true
nav_order: 2
display_categories: [Snow, CLM, Noise]
horizontal: true
---

## Snow Hydrology in Peatland Dominated Catchments
*NSF Hydrological Sciences Grant #2153802 Forest, Frost, and Flow: Snow Hydrology of Spatially Heterogeneous and Hydrologically Connected Peatland Catchments*

Peatlands, a subset of wetlands that store organic carbon in the form of peat, cover only 3% of the globe but are responsible for storing more than 30% of all soil carbon. They are one of the most efficient carbon stores on the planet and are a critical buffer against global warming. Many of these peatlands are found along two latitudes: right above the equator in areas like Florida, Malaysia, and Southeast Asia; and right below the Arctic Circle in Canada, Scandinavia, and Russia. My research focuses on the latter for another critical climate change reason: winter. A peatland's ability to maintain vast carbon stores is driven by its hydrology, specifically the water table. As winter temperatures and snowfall regimes change due to global warming, peatland hydrology shifts too, in ways that may decrease the carbon-trapping potential of these essential ecosystems. To figure out if and how peatlands are responding to these changes, we study the shifts in hydrologic connectivity under different snow regimes in peatland dominated watersheds. Some of our recent results are published or described below. 

<!-- Projects with 'Snow' designation -->
<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in {{ Snow }} %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-8">
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
    <div class="row row-cols-8">
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
