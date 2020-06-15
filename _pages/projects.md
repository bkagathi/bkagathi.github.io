---
layout: page
title: projects
permalink: /projects/
description: Here a few of my projects and experiences
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail" style="background-image: url('{{ project.img | prepend: site.baseurl | prepend: site.url }}'); background-size: contain; background-repeat: no-repeat;">
        <a href="{{ project.redirect }}" target="_blank">
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail" style="background-image: url('{{ project.img | prepend: site.baseurl | prepend: site.url }}'); background-size: contain; background-repeat: no-repeat;">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
