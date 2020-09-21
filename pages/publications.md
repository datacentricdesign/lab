---
layout: default
title: "Publications"
permalink: /publications/index.html
description: "Data-Centric Design Lab"
---

{% assign sorted = site.publications | sort: 'year' | reverse %}
{% for publication in sorted %}
[{{ publication.type }}] {{ publication.authors }}. {{ publication.title }}. {{ publication.venue }}. {{ publication.year }}
{% endfor %}

