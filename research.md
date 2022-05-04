---
title: Research
layout: post
use_fontawesome: true
---

This page highlights several of my research projects. For a complete list of my publications, see my [publications page](./publications.html).

{% for category in page.categories %}
  <div class="border-bottom">
  <h1 class="section-title">{{ category | capitalize }}</h1>
  {%- for research in site.data.research -%}
    {%- if research.category != category -%}{% continue %}{%- endif -%}
    {%- if research.hidden -%}{%- continue -%}{%- endif -%}
    {% include research.html %}
  {%- endfor -%}
  </div>
{%- endfor -%}

