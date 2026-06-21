---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can also find my publications on [Google Scholar](https://scholar.google.com/citations?user=HvWTE0IAAAAJ&hl=zh-CN).

## Profile

My work has appeared in leading venues in computer vision, medical image analysis, and machine learning, including CVPR, ICCV, MICCAI, TPAMI, TIP, IEEE Transactions on Medical Imaging, and IEEE Journal of Biomedical and Health Informatics.

{% include base_path %}

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
