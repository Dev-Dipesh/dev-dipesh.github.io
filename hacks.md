---
layout: page
title: "Hacks"
description: ""
group: navbar
weight: 2
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

<ol class="breadcrumb alert-info">
  <li><a href="index.html"><span class="glyphicon glyphicon-home"></span></a></li>
  <li class="active">Hacks</li>
</ol>
<div>
<div class="input-group col-sm-3">
    <input type="text" class="form-control" id="typeahead" />
	<span class="input-group-addon">#</span>
</div>

<hr>
  <div class="row">  
    <h4>RECENT POSTS</h4>
    <hr>
    {% for post in site.posts %}
    	<h5><a href="{{ post.url }}">{{ post.title }}</a></h5>
    {% endfor %}
  </div>  
<div>
  <h4>ARCHIVE</h4>
  	<section id="archive">
		  {%for post in site.posts %}
		    {% unless post.next %}
		      <h3>{{ post.date | date: '%Y' }}</h3>
		      <ul class="this">
		    {% else %}
		      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
		      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
		      {% if year != nyear %}
		        </ul>
		        <h3>{{ post.date | date: '%Y' }}</h3>
		        <ul class="past">
		      {% endif %}
		    {% endunless %}
		      <li><time>{{ post.date | date:"%d %b" }}</time><a href="{{ post.url }}">{{ post.title }}</a></li>
		  {% endfor %}
		  </ul>
		</section>
  	</div>


</div> 