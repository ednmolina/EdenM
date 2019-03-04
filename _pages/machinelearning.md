---
layout: archive
<<<<<<< HEAD
permalink: /machine-learning/
title: "This page will contain all the posts"
=======
permalink: /posts/
title: "My Posts"
>>>>>>> e53b81718abacddcc1803c5a51e460bdda3c99bf
author_profile: true
header:
#  image:
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
