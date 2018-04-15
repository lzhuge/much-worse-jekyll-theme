---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Regulation, Innovation, and the Porter Hypothesis: Examining Outcomes in Chinese Pollution Control Policy Areas"
      author:  "Richard B. Freeman, Matthew T. Higgins, Liqun Zhuge"
      journal: "A Journal"
      note:    "at R&R"
      year:    "2018"
      url:     "http://publish-more-stuff.org"
      
    - title:   "Firm Dynamics of Hi-Tech Start-ups: Does Innovation Matter?"
      author:  "Richard B. Freeman, Matthew T. Higgins, Liqun Zhuge"
      journal: "A Journal"
      note:    "at R&R"
      year:    "2018"
      url:     "http://publish-more-stuff.org"
    
---

## Working Paper

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
