---
layout: page
permalink: /research/
title: Research
wp:

    - title:   "Regulation, Innovation, and the Porter Hypothesis: Examining Outcomes in Chinese Pollution Control Policy Areas"
      author:  "Richard B. Freeman, Matthew T. Higgins, Liqun Zhuge"
      journal: "A Journal"
      note:    "at R&R"
      year:    "2018"
      
wip:
    - title:   "Firm Dynamics of Hi-Tech Start-ups: Does Innovation Matter?"
      author:  "Dongyang Zhang, Liqun Zhuge"
      note:    "in Process"
      year:    "2018"

---

## Working Paper

{% assign thumbnail="left" %}

{% for wp in page.wp %}
{% if wp.image %}
{% include image.html url=wp.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{wp.title}}**]({% if wp.internal %}{{wp.url | prepend: site.baseurl}}{% else %}{{wp.url}}{% endif %})<br />
{{wp.author}}<br />
*{{wp.journal}}*
{% if wp.note %} *({{wp.note}})*
{% endif %} *{{wp.year}}* {% if wp.doi %}[[doi]({{wp.doi}})]{% endif %}
{% if wp.media %}<br />Media: {% for article in wp.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}

# Work in Process

{% assign thumbnail="left" %}

{% for wip in page.wip %}
{% if wip.image %}
{% include image.html url=wip.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{wip.title}}**]({% if wip.internal %}{{wip.url | prepend: site.baseurl}}{% else %}{{wip.url}}{% endif %})<br />
{{wip.author}}<br />
*{{wip.journal}}*
{% if wip.note %} *({{wip.note}})*
{% endif %} *{{wip.year}}* {% if wip.doi %}[[doi]({{wip.doi}})]{% endif %}
{% if wip.media %}<br />Media: {% for article in wip.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
