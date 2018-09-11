---
layout: page
permalink: /research/
title: Research
wp:

    - title:   "Regulation and Innovation: Examining Outcomes in Chinese Pollution Control Policy Areas"
      author:  "Richard B. Freeman, Matthew T. Higgins, **Liqun Zhuge**"
      journal: "Economic Modelling"
      note:    "at R&R"
      year:    "2018"
      url: "https://docs.google.com/viewerng/viewer?url=https://raw.githubusercontent.com/lzhuge/lzhuge.github.io/master/paper/Regulation%2C%20Innovation%2C%20and%20the%20Porter%20Hypothesis.pdf&hl=en_US"
      
    - title:   "Are financial constraints an anxiety for firms to survive in the Chinese market?"
      author:  "Dongyang Zhang, **Liqun Zhuge**"
      note:    "Under Review"
      year:    "2018"
      url: "https://docs.google.com/viewerng/viewer?url=https://raw.githubusercontent.com/lzhuge/lzhuge.github.io/master/paper/Are%20financial%20constraints%20an%20anxiety%20for%20firms%20to%20survive%20in%20the%20Chinese%20market.pdf&hl=en_US"
      
    - title:   "Firm Dynamics of Hi-Tech Start-ups: Does Innovation Matter?"
      author:  "Dongyang Zhang, **Liqun Zhuge**"
      note:    "Under Review"
      year:    "2018"
      url: "https://docs.google.com/viewerng/viewer?url=https://raw.githubusercontent.com/lzhuge/lzhuge.github.io/master/paper/Firm%20Dynamics%20of%20Hi-Tech%20Start-ups.pdf&hl=en_US"
      
      - title:   "Do financial constraints curb a firm’s efforts to control pollution: Evidence from Chinese manufacturing firms"
      author:  "Dongyang Zhang, Wencui Du, **Liqun Zhuge**, Zheming Tong"
      note:    "Under Review"
      year:    "2018"
      url: "https://docs.google.com/viewerng/viewer?url=https://raw.githubusercontent.com/lzhuge/lzhuge.github.io/master/paper/Do%20financial%20constraints%20curb%20a%20firm%E2%80%99s%20efforts%20to%20control%20pollution.pdf&hl=en_US"
      


ow:
    - title:   "Science’s 1%: How income inequality is getting worse in research"
      author:  "Corie Lok, Richard B. Freeman, etc."
      journal: "Nature"
      note:    "Contributing Writer"
      year:    "2016"
      url:     "https://www.nature.com/news/science-s-1-how-income-inequality-is-getting-worse-in-research-1.20651?WT.ec_id=NATURE-20160922&spMailingID=52357585&spUserID=MTA3NDk2MzQzMzM2S0&spJobID=1003755044&spReportId=MTAwMzc1NTA0NAS2"

---

### Publication and Working Paper

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

### Work in Process

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

### Other Work

{% assign thumbnail="left" %}

{% for ow in page.ow %}
{% if ow.image %}
{% include image.html url=ow.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{ow.title}}**]({% if ow.internal %}{{ow.url | prepend: site.baseurl}}{% else %}{{ow.url}}{% endif %})<br />
{{ow.author}}<br />
*{{ow.journal}}*
{% if ow.note %} *({{ow.note}})*
{% endif %} *{{ow.year}}* {% if ow.doi %}[[doi]({{ow.doi}})]{% endif %}
{% if ow.media %}<br />Media: {% for article in ow.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
