---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Editable parametric dense foliage from 3D capture"
      author:  "G. Chaurasia, P. Beardsley"
      journal: "IEEE International Conference on Computer Vision"
      note:    "ICCV"
      year:    "2017"
      url:     "https://www.disneyresearch.com/publications/parametric-foliage/"
      doi:     "http://openaccess.thecvf.com/content_iccv_2017/html/Chaurasia_Editable_Parametric_Dense_ICCV_2017_paper.html"
      media:
        - name: TechCrunch
          url:  https://techcrunch.com/2017/10/23/the-dream-of-customizable-virtual-3d-foliage-is-alive-at-disney/

    - title:   "Deep joint demosaicking and denoising"
      author:  "M. Gharbi, G. Chaurasia, S. Paris, F. Durand"
      journal: "ACM Transactions on Graphics"
      note:    "SIGGRAPH Asia"
      year:    "2016"
      url:     "https://groups.csail.mit.edu/graphics/demosaicnet/"
      doi:     "http://dx.doi.org/10.1145/2980179.2982399"

talks:

    - venue:  "Microsoft Research Redmond"
      date:   "July 19, 2013"
      url:    "http://research.microsoft.com/apps/video/dl.aspx?id=198331"

    - venue:  "MIT CSAIL"
      date:   "Sept 11, 2013"
      url:    "/research/talks/csail_2013/"
      internal: "1"


journal_reviews:

    - title: "ACM Transactions on Graphics"
      url:   "http://tog.acm.org"
      years:
        - year: 2016
        - year: 2017

    - title: "ACM Transactions on Applied Perception"
      url:   "http://tap.acm.org"
      years:
        - year: 2014


conference_reviews:

    - title: "SIGGRAPH"
      years:
        - year: 2012
          url:  "http://s2012.siggraph.org/"
        - year: 2016
          url:  "http://s2016.siggraph.org/"

    - title: "SIGGRAPH Asia"
      years:
        - year: 2013
          url:  "http://sa2013.siggraph.org/en/"
        - year: 2016
          url:  "http://sa2016.siggraph.org/en/"
        - year: 2017
          url:  "http://sa2017.siggraph.org"
          
---

Jump to [Publications](#peer-reviewed-publications), [Thesis](#doctoral-thesis), [Media](#media-coverage), [Reviewing](#professional-service)

---

## Peer reviewed publications

{% assign thumbnail="right" %}

{% for pub in site.data.cv.publications %}
<!-- {% if pub.image %}
{% include image.html url=pub.image caption="" height="80px" align=thumbnail %}
{% endif %} -->
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}*  [[web]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})] {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}

{% endfor %}

-----

## Doctoral thesis

**Algorithms & perceptual analysis for interactive free viewpoint image-based navigation** [[web]({{ "/research/thesis/" | prepend: site.baseurl}})]<br />
*Adviser: [George Drettakis](http://www-sop.inria.fr/members/George.Drettakis)* <br />
[INRIA](http://www.inria.fr/sophia), 2014

------

## Media coverage

{% for pub in site.data.cv.publications %}
{% if pub.media %}
- {{pub.title}} ({{pub.note}}, {{pub.year}}){% for article in pub.media %}
    - [{{article.url}}]({{article.url}}){% endfor %}
{% endif %}

{% endfor %}

------

## Professional service

- Conference reviews{% for review in site.data.cv.reviews.conference %}
    - {{review.title}} {% for y in review.years %} [{% if y.url %}[{{y.year}}]({{y.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %}

- Journal reviews{% for review in site.data.cv.reviews.journal %}
    - {{review.title}} {% for y in review.years %} [{% if review.url %}[{{y.year}}]({{review.url}}){% else %}{{y.year}}{% endif %}] {% endfor %}<br />{% endfor %}

