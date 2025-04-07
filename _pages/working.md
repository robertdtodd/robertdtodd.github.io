---
layout: single
title: Working with AI
permalink: /working/
classes: wide
---
Any list of LLMs and other ML model-powered tools and their capabilities is certain to be out of date as soon as it is published. These tables are primarily shortcuts for students and new LLM users.  Check the 'last updated' date for confidence.

{% for category in site.data.tools %}
  <h2>{{ category.category }}</h2>
  <p>{{ category.description }}</p>
  
  <table class="resources-table">
    <thead>
      <tr>
        <th>Resource</th>
        <th>Type</th>
        <th>Source</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      {% for resource in category.resources %}
        <tr>
          <td><a href="{{ resource.url }}">{{ resource.name }}</a></td>
          <td><span class="badge badge-{{ resource.type }}">{{ resource.type }}</span></td>
          <td>{{ resource.source}}</td>
          <td>{{ resource.description }}</td>
        </tr>
      {% endfor %}
    </tbody>
  </table>
{% endfor %}