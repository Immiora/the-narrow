---
permalink: /gods/
---

{% assign cat = "gods" %}

### {{ cat }}
<ul>
  {% for page in site.pages %}
    {% for pc in page.categories %}
      {% if pc == cat %}
        <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
      {% endif %}   <!-- cat-match-p -->
    {% endfor %}  <!-- page-category -->
  {% endfor %}  <!-- page -->
</ul>
