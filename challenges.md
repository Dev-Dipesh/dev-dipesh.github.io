---
layout: page
title: "Challenges"
description: ""
group: navbar
weight: 4
---
{% include JB/setup %}

{% for node in pages_list %}
  {% if group == null or group == node.group %}
    {% if page.url == node.url %}
      <li class="active"><a href="{{node.url}}" class="active">{{node.title}}</a></li>
    {% else %}
      <li><a href="{{node.url}}">{{node.title}}</a></li>
    {% endif %}
  {% endif %}
{% endfor %}
{% assign pages_list = nil %}
{% assign group = nil %}

<div class="bodybg">
<div class="container clear">
<header id="siteHeader">
  <div class="headerDescription">
    <p class="visibleH1"><a href="#" title="For the Home Blogs">Blog</a></p>
    <p class="visibleH2">Posts, tutorials, tips &amp; snippets about web design and social media. </p><p>
  </p></div>
</header>
</div>

<div class="container-narrow">
  <div class="content">
  	<div class="page-header">
  		<h1>{{ page.title }} {% if page.tagline %} <small>{{ page.tagline }}</small>{% endif %}</h1>
	</div>
<ol class="breadcrumb alert-info">
  <li><a href="index.html"><span class="glyphicon glyphicon-home"></span></a></li>
  <li class="active">Challenges</li>
</ol>
</div>
<hr />
</div>
</div>