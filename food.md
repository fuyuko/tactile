---
layout: default
title: Food
---
<div id="archives">
        <div class="archive-group">
            {% capture category_name %}food{% endcapture %}
            <div id="#food"></div>
            <h2 class="category-head">food</h2>
            <a name="food"></a>
            {% for post in site.categories['food'] %}
                <article class="archive-item">
                    <h3><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h3>  
                    <div class="thumbnail">
                        <img src="{{ site.baseurl }}/images/{{ post.thumbnail }}" />
                    </div>
                    {{ post.excerpt }}
                </article>
            {% endfor %}
        </div>
</div>