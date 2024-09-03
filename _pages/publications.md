---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
---

# Publications

{% assign yeartest = true %}
{% for publi in site.publications %}
  {% if publi.year %}{% else %}
   {% assign yeartest = false %}
  {% endif %}
{% endfor %}

## Conference/Journal Papers
{% for publi in site.publications reversed %}

  {% if publi.arxiv == true %}{% else %}

  {% assign pdfpresent = false %}
  {% if publi.pdf %}
    {% assign pdfpresent = true %}
    {% assign pdffile = publi.pdf  | append: ".pdf" %}
  {% endif %}

  {% assign bibpresent = false %}
  {% if publi.pdf %}
    {% assign bibpresent = true %}
    {% assign bibfile = publi.pdf  | append: ".txt" %}
  {% endif %}

  {% assign learning2hash = false %}
  {% if publi.learning2hash == true %}
    {% assign learning2hash = true %}
  {% endif %}

  <div class="well-sm publication-entry">
  <ul class="flex-container">
  <li class="flex-item1">
    {% if publi.image %}
     <img src="{{ site.url }}{{ site.baseurl }}/publications/{{ publi.image }}" class="img-responsive"/>
    {% endif %}
  </li>
  <li class="flex-item2">
    <!-- <strong>{{ publi.title }}</strong>. {% if publi.pdf %}[<a href="{{ pdffile }}" target="_blank">pdf</a>]{% endif %}{% if publi.github %}[<a href="{{ publi.github }}" target="_blank">github</a>]{% endif %}<br/> -->
    <strong>{{ publi.title }}</strong>. {% if publi.pdf %}[<a href="{{ pdffile }}" target="_blank">pdf</a>]{% endif %}{% if publi.github %}[<a href="{{ publi.github }}" target="_blank">github</a>]{% endif %}{% if publi.project %}[<a href="{{ publi.project }}" target="_blank">project</a>]{% endif %}<br/>
    {{ publi.authors }}<br/>
    <em>{{ publi.display }} ({{ publi.display_short }}).</em> {{ publi.year }}<br/>
    {% if publi.abstract %} <a data-bs-toggle="collapse" href="#{{publi.pdf}}"  class="btn-abstract" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}">ABSTRACT</a> {% endif %}
    {% if bibpresent == true %} <a data-bs-toggle="collapse" href="#{{publi.pdf}}2"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}2">BIB</a> {% endif %}
    {% if publi.learning2hash == true %} <a class="btn-l2h" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}2">Learning2Hash</a> {% endif %}
    {% if publi.ndvr == true %} <a class="btn-ndvr" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}2">Near-Duplicated Video Retrieval</a> {% endif %}
    {% if publi.fine_grained_retrieval == true %} <a class="btn-fgr" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}2">Fine-Grained Image Retrieval</a> {% endif %}
    {% if publi.cross_modal_retrieval == true %} <a class="btn-cmr" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}2">Cross-Modal Retrieval</a> {% endif %}
    {% if publi.multimodal == true %} <a class="btn-mml" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false" aria-controls="{{publi.pdf}}2">Multimodal Learning</a> {% endif %}
    <!-- {% if pdfpresent == true %}<a href="{{ pdffile }}" target="_blank"><button class="btn-pdf">PDF</button></a>{% endif %} -->
    <!-- {% if publi.arxiv %}<a href="https://arxiv.org/abs/{{ publi.arxiv }}" target="_blank"><button class="btn-arxiv">ARXIV</button></a> {% endif %} -->
    <!-- {% if publi.github %}<a href="{{ publi.github }}" target="_blank"><button class="btn-code">github</button></a> {% endif %} -->

  {% if publi.abstract %}
  <div class="collapse" id="{{publi.pdf}}"><div class="well-abstract">
   {{publi.abstract}}
  </div></div>
  {% endif %}

  {% if bibpresent == true %}
  <div class="collapse" id="{{publi.pdf}}2"><div class="well-bib">
   <iframe src='{{site.url}}{{site.baseurl}}/publications/{{publi.pdf}}.txt' scrolling="yes" width="100%" height="210" frameborder="0"></iframe>
  </div></div>
  {% endif %}

  </li>
  </ul>
  </div>
  {% endif %}
{% endfor %}

\* Equation contribution.


## Pre-Print
{% for publi in site.publications %}
  {% if publi.arxiv == true %}
  <div class="well-sm publication-entry">
  <ul class="flex-container">
  <li class="flex-item1">
    {% if publi.image %}
    <img src="{{ site.url }}{{ site.baseurl }}/publications/{{ publi.image }}" class="img-responsive"/>
    {% endif %}
  </li>
  <li class="flex-item2">
    <strong>{{ publi.title }}</strong>. [<a href="{{ publi.link }}" target="_blank">paper link</a>]<br/>
    {{ publi.authors }}<br/>
  </li>
  </ul>
  </div>
  {% endif %}
{% endfor %}
