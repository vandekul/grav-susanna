---
process:
    markdown: true
    twig: true
cache_enable: true
child_type: default
robots:
    noindex: false
    nofollow: false
---
<header class="major">
    <h2>El meu estil <br /> </h2>
</header>  
<div class="row">
    <div class="12u">
        {% set images = page.media|sort %}
        <div class="box alt">
        {% for img in images %}
            {% if loop.index0 % 3 == 0 %}
                <div class="row no-collapse 30% uniform">
            {% endif %}
                    <div class="4u">
                        <span class="image fit">
                            <img src= {{ img.url }} alt="" />
                        </span>
                    </div>
            {% if loop.index % 3 == 0 %}
                </div>
            {% endif %} 
        {% endfor %}
        </div>
    </div>
</div>