---
layout: default
---
<div id="archives">
<h2>Recent Posts</h2>
{% for post in site.posts limit:10 %}
    <article class="archive-item">
        <h3><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h3>  
        <div class="thumbnail">
            <a href="{{ site.baseurl }}{{ post.url }}"><img src="{{ site.baseurl }}/images/{{ post.thumbnail }}" /></a>
        </div>
        {{ post.excerpt }}
    </article>
{% endfor %}
</div>

