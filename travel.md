---
layout: default
title: Travel
---
<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
        <h2 class="category-head">{{ category_name }}</h2>
        <a name="{{ category_name | slugize }}"></a>
        {% for post in site.categories[category_name] %}
            <article class="archive-item">
            <h3><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h3>  
            <div class="thumbnail">
                <img src="{{ site.baseurl }}/images/{{ post.thumbnail }}" />
            </div>
            {{ post.excerpt }}
            </article>
        {% endfor %}
    </div>
{% endfor %}
</div>