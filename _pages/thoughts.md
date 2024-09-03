---
layout: archive
title: "thoughts"
permalink: /thoughts/
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/cover-thoughts.jpg
excerpt: "rambling on..."
---

{% for post in site.posts limit: 5 %}
  {% include archive-single.html %}
{% endfor %}

