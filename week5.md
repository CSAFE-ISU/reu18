---
layout: default
title: "CSAFE @ ISU REU"
css: "/css/index.css"
---

<div class="list-filters">
  <a href="/reu18" class="list-filter">All posts</a>
  <a href="/reu18/assignments" class="list-filter">Assignments</a>
    <a href="/reu18/week1" class="list-filter">June 4-10, 2018</a>
  <a href="/reu18/week2" class="list-filter">June 11-17, 2018</a>
  <a href="/reu18/week3" class="list-filter">June 18-24, 2018</a>
  <a href="/reu18/week4" class="list-filter">June 25 - July 1, 2018</a>
  <a href="/reu18/week5" class="list-filter filter-selected">July 2-8, 2018</a>
  <a href="/reu18/week6" class="list-filter">July 9-15, 2018</a>
  <a href="/reu18/week7" class="list-filter">July 16-22, 2018</a>
  <a href="/reu18/week8" class="list-filter">July 23-30, 2018</a>
    <a href="/reu18/week8" class="list-filter">July 30 - August 3, 2018</a>
</div>

<div class="posts-list">
  {% for post in site.tags.week1 %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>
	
	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>