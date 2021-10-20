---
permalink : /mathtalk/
title: "Math Talk"
layout: page 
slug: mathtalk
menu: true
---

I have some pure math courses in my curriculum and I have thoroughly enjoyed most of them. Sometimes I find a topic super interesting and try to write about it here. Note that these are dynamic and I will try to update them as my knowledge grows. Feel free to contact me for any feedback on these.

<div class="listOfPosts">
<ol class="listOfPosts">
{% for post in site.categories.mathtalk %}
    <li> <h4> <a href="{{ post.url }}">{{ post.title }}</a> </h4> <p>{{ post.description }}</p></li>
{% endfor %}
</ol>
</div>
