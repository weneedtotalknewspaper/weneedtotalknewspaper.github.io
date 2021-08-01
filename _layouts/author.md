---
layout: default
---
<div class="container">
<div class="row justify-content-center">
    <div class="col-md-8">        
        <div class="row align-items-center mb-5">
            <div class="col-md-9">
            {% for author in site.authors %}
                {% if author.name == page.name%}
                    <h2 class="font-weight-bold">{{author.name}}</h2>
                    <p class="text-dark mb-0">{{author.position}}</p>
                    <p class="excerpt">{{ author.bio }}</p>
                    </div>
                    <div class="col-md-3 text-right">
                    {% if author.avatar %}
                        <img alt="{{ author.name }}" src="{{site.baseurl}}/{{ author.avatar }}" >
                    {% else %}
                        <img alt="{{ author.name }}" src="{{site.baseurl}}/assets/images/default_avatar.png" >
                    {% endif %}
                    </div>
                    </div>
                    <h4 class="font-weight-bold spanborder"><span>Posts by {{page.name}}</span></h4>
                    {% assign posts = site.posts | where:"author",page.name %}
                        {% for post in posts %}
                        {% include main-loop-card.html %}
                    {% endfor %}
                {% endif %}
            {% endfor %}
        </div>
</div>
</div>