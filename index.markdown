---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: splash
title: "Welcome to Langua Lingua website"
header: 
    overlay_color: "#000"
    overlay_filter: "0.5"
    overlay_image: /assets/images/banner.png
excerpt: "Celebrate the language and cultural diversity at NYU Shanghai by inspiring conversations and sharing opportunities in language exchange and the study of linguistics."

---

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>

{% include paginator.html %}