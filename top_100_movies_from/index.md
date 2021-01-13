---
title: Top 100 Movies from Year Lists
---

## Top 100 Movies from Year Lists

### Lists

{% assign movie_files = site.static_files | sort: 'basename' %}
{% for file in movie_files %}
  {% if file.path contains "/top_100_movies_from/" and file.extname == ".json" %}
  - [{{file.basename | replace: "top_100_movies_from_", "" }}](https://silentdot.github.io/radarr-lists/top_100_movies_from/{{file.name}})
  {% endif %}
{% endfor %}
