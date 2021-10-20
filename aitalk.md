---
permalink : /aitalk/
title: "AI Talk"
layout: page 
slug: aitalk
menu: true
---

Note that these are dynamic and I will try to update them as my knowledge grows. Feel free to contact me for any feedback on these.

<div class="listOfPosts">
<ol class="listOfPosts">
{% for post in site.categories.aitalk %}
    <li> <h4> <a href="{{ post.url }}">{{ post.title }}</a> </h4> <p>{{ post.description }}</p></li>
{% endfor %}
</ol>
</div>
