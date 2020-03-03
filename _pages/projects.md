---
layout: page
title: Projects
permalink: /projects/
description: A growing collection of your cool projects.
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img style="height: auto; position: relative; left: 0%; top: 0%; width: 200px;" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
    <div style="margin-top:10px" align="center"><a href="{{ project.redirect }}" target="_blank">Direct link to {{ project.title }} website</a></div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img style="height: auto; position: relative; left: 0%; top: 0%; width: 200px;" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
            <p>JURI2</p>
        </span>
        </a>
    </div>
    <div style="margin-top:10px" align="center"><a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}" target="_blank">{{ project.title }}</a></div>
</div>

{% endif %}

{% endfor %}
