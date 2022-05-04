---
title: Research
layout: post
use_fontawesome: true
categories:
  - Model development for analyzing the diversification of clades of unknown diversity
  - Inference technique for fast and flexible, likelihood free diversification analyses
  - Diatoms diversification in light of their ecological niche space
---

This page highlights several of my research projects. For a complete list of my publications, see my [publications page](./publications.html).

{% for category in page.categories %}
  <div class="border-bottom">
  <h1 class="section-title">{{ category | capitalize }}</h1>
  {%- for project in site.data.projects -%}
    {%- if project.category != category -%}{% continue %}{%- endif -%}
    {%- if project.hidden -%}{%- continue -%}{%- endif -%}
    {% include project.html %}
  {%- endfor -%}
  </div>
{%- endfor -%}
