---
layout: page
title: news
permalink: /news/
nav: true
---

{% for post in site.announcements %} 
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>Posted on: {{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html }}</p> 
    <a href="{{ post.url }}" class="btn btn-sm z-depth-0">Read More</a>
  </article>
{% endfor %}

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>Posted on: {{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html }}</p> 
    <a href="{{ post.url }}" class="btn btn-sm z-depth-0">Read More</a>
  </article>
{% endfor %}