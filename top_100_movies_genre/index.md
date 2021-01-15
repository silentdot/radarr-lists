---
title: Top 100 Movies from Genre
---

## Top 100 Movies from Year Lists

### Lists

{% assign movie_files = site.static_files | reverse %}
{% for file in movie_files %}
  {% if file.path contains "/top_100_movies_genre/" and file.extname == ".json" %}
  - [{{file.basename}}](https://silentdot.github.io/radarr-lists/top_100_movies_genre/{{file.name}})
  {% endif %}
{% endfor %}
