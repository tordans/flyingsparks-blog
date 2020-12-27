---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Images for OpenStreetMap OSM

{% for image in site.static_files %}
  {% if image.path contains 'openstreetmap' %}
  {% unless image.path contains 'original' %}
<img src="{{ site.baseurl }}{{ image.path }}" alt="image" />
<pre>{{ site.baseurl }}{{ image.path }}</pre>
<pre>![Picture](https://tordans.github.io/flyingsparks-blog{{ site.baseurl }}{{ image.path }})</pre>
  {% endif %}
  {% endif %}
{% endfor %}
