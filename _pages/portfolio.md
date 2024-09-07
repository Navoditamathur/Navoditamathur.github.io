---
layout: archive
title: "Projects"
permalink: /portfolio/
author_profile: true
redirect_from:
  - /portfolio
---

{% include base_path %}


{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}
