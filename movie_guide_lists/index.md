---
title: Top 100 Movies from Genre
---

## Rotten Tomatoes Movie Guides

These are some extracted lists from rottentomatoes movie guides. [Example.]("https://editorial.rottentomatoes.com/guide/all-a24-movies-ranked/")

### Lists

{% assign movie_files = site.static_files %}
{% for file in movie_files %}
{% if file.path contains "/movie_guide_lists/" and file.extname == ".json" %}

- [{{file.basename}}](https://silentdot.github.io/radarr-lists/movie_guide_lists/{{file.name}})
  {% endif %}
  {% endfor %}
