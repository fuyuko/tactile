---
layout: default
title: Miscellaneous
---
<div id="archives">
        <div class="archive-group">
            {% capture category_name %}misc{% endcapture %}
            <div id="#misc"></div>
            <h2 class="category-head">Miscellaneous</h2>
            <a name="miscellaneous"></a>
            {% for post in site.categories['misc'] %}
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