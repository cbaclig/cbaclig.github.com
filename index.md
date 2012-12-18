---
layout: default
---
{% include JB/setup %}

<h1>{{ site.posts.first.title }}</h1>

{{ site.posts.first.content }}

{% assign current_post = site.posts.first %}
{% include themes/dinky/fwd_back_nav.html %}

{% include JB/comments %}
