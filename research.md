---
layout: page
permalink: /research/
title: Research
wp:

    - title:   "Paper title in 3-7 words that sound like Clingon"
      author:  "M. McFly, D. Kirk, L. Skywalker, H.J. Potter, I. Jones, H. Houdini"
      journal: "Transactions on Black Magic"
      note:    "(presented at Oz)"
      year:    "2016"
      url:     "http://publish-more-stuff.org"
      doi:     "http://dx.doi.org"
      image:   "https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fimages.moviepostershop.com%2Fthe-matrix-movie-poster-1999-1020518087.jpg&f=1"
      media:
        - name: "IMDB"
          url:  "http://www.imdb.com/title/tt0133093/"


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
