---
title: News
permalink: /news/
---

### **Latest news from BCNU**
<br>
<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'news' %}
    <div class="list-item">
    <p class="list-post-title">
        <small>{{post.date | date: "%d/%m/%y" }}</small>: <b><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></b>
        {{post.content}}
        </p>
    </div>
    {% endif %}
  {% endfor %}
</div>


<br>
<hr>
{% include footer.html %}