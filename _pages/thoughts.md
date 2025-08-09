---
title: "thoughts"
layout: archive
permalink: /thoughts/
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/cover-thoughts.jpg
excerpt: "rambling on..."
entries_layout: grid
---

{% assign entries_layout = page.entries_layout | default: 'list' %}

<section class="taxonomy__section">
  <div class="entries-{{ entries_layout }}">
    {% for post in site.posts %}
      {% include archive-single.html type=entries_layout %}
    {% endfor %}
  </div>
  <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
</section>
