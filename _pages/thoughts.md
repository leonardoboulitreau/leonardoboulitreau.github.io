---
title: "thoughts"
layout: splash
permalink: /thoughts/
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/cover-thoughts.jpg
excerpt: "rambling on..."
entries_layout: grid
---

{% for post in site.posts%}
  {% include archive-single.html type=grid%}
{% endfor %}

