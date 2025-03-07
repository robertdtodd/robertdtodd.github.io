---
layout: single
title: Understanding AI
permalink: /resources/
---

{% for category in site.data.resources %}
  <h2>{{ category.category }}</h2>
  <p>{{ category.description }}</p>
  
  <table class="resources-table">
    <thead>
      <tr>
        <th>Resource</th>
        <th>Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      {% for resource in category.resources %}
        <tr>
          <td><a href="{{ resource.url }}">{{ resource.name }}</a></td>
          <td><span class="badge badge-{{ resource.type }}">{{ resource.type }}</span></td>
          <td>{{ resource.description }}</td>
        </tr>
      {% endfor %}
    </tbody>
  </table>
{% endfor %}