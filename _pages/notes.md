---
title: "Notes"
layout: gridlay
sitemap: false
permalink: /notes/
---

# Notes

## Tools for Research
{% for note in site.notes %}
{% if note.type=="tool"%}
  <div class="well-sm publication-entry">
  <ul class="flex-container">
  <li class="flex-item1">
    {% if note.image %}
     <img src="{{ site.url }}{{ site.baseurl }}/notes/{{ note.image }}" class="img-responsive"/>
    {% endif %}
  </li>
  <li class="flex-item2">
    <a href="{{ note.link }}" target="_blank"><strong>{{ note.title }}</strong></a>
    <br/>{{ note.authors }}
    <br/>Intro: {{ note.intro }}
  </li>
  </ul>
  </div>
{% endif %}
{% endfor %}


