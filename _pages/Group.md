---
layout: page
title: Group
permalink: /Group/
nav: true
nav_order: 2
student_categories: [Post Doc, PhD Students, Master Students]
imageless_categories: [Undergraduated Students, Graduated Students]
horizontal: true
---

<!-- pages/group.md -->
<div class="projects">
<!-- Display categorized student -->
{%- for category in page.student_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_group = site.group | where: "category", category -%}
  {%- assign sorted_group = categorized_group | sort: "order" %}
  <!-- Generate cards for each student -->
  <div class="container">
    <div class="row row-cols-1">
    {%- for student in sorted_group -%}
      {% include group_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
{% endfor %}
<h2 class="category">Undergraduated Students</h2>
<ul>
<li>Rongchen Liu</li>
<li>Wenjiong Wang</li>
<li>Xinyu Chen</li>
<li>Haoyang Qu</li>
<li>Ruidong Zhang</li>
</ul>
<h2 class="category">Graduated Students</h2>
<ul>
<li>Shuaiben Chen (Graduated in 2022; Next position: Momenta)</li>
<li>Peiyi Hong (Graduated in 2023; Next position: Ant Group)</li>
<li>Shuang Hu (Graduated in 2023; Next position: State Grid)</li>
</ul>
</div>
