---
# Remember to set production_url in your _config.yml file!
title : Sitemap
---
{% for page in site.pages %}
{{site.production_url}}{{ page.url }}{% endfor %}
{% for post in site.posts %}
{{site.production_url}}{{ post.url }}{% endfor %}