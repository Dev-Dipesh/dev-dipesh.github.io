---
layout: page
title: "Tutorials"
description: ""
group: navbar
weight: 1
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
  <li class="active">Tutorials</li>
</ol>

<div class="row">
  <div class="col-xs-12 col-sm-6 col-md-8">
    
    {% for post in site.posts %}
      <div class="row">
        <div class="col-md-3 one-edge-shadow1">
          <img src="{{ post.description }}" class="pull-left img-circle  tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="{{ post.author }}">
        </div>	
        <div class="col-md-9">
          <div class="row">
            <div class="col-md-5">
              <p>
                <small><strong>{{ post.date | date: "%B %e, %Y" }}</strong> . {{ post.category }}</small>
              </p>
            </div>

            <div class="col-md-3">
              <p class="fb-like" data-href="http://developers.facebook.com/docs/reference/plugins/like" data-width="450" data-layout="button_count" data-show-faces="false" data-send="true"></p>
            </div>

            <div class="col-md-2">
              <p class="g-plusone" data-size="medium"></p>
            </div>

            <div class="col-md-2">
              <p>
              	<a href="https://twitter.com/share" class="twitter-share-button">Tweet</a>
              </p>
            </div>
          </div>
          
          
          
          						 

          <h3><a href="{{ post.url }}" style="text-decoration: none;">{{ post.title }}</a><a href=""><img src="{{ ASSET_PATH }}twitter/images/download_icon.png" class="pull-right tooltip-test" style="width:50px; height:50px;"  data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Download as PDF"></a></h3>
          <p><em><small>by <a href="#" class="tooltip-test" data-toggle="tooltip" data-placement="right" title="" data-original-title="All Post by {{ post.author }}."><strong>{{ post.author }}</strong></a></small></em></p>
          <hr class="hr" />
          <p>{{ post.excerpt }}</p>
          <br />
          <p><strong>Continue reading <a href="{{ post.url }}">{{ post.title }}</a>.</strong></p>
          <p><strong>Tags <span class="glyphicon glyphicon-tags"></span>  <small>{{ post.tags }}</small></strong></p>
          <div id="post_bottom_border"></div>
        </div>
       </div>  

        <!-- <p class="pull-right">{% if page.previous.url %} <a href="{{page.previous.url}}" title="Previous Post: {{page.previous.title}}"><span class="glyphicon glyphicon-chevron-left"></span></a> 	{% endif %}   {% if page.next.url %} 	<a href="{{page.next.url}}" title="Next Post: {{page.next.title}}"><span class="glyphicon glyphicon-chevron-right"></span></a> 	{% endif %} </p>  -->
    {% endfor %}
    
  </div>
  <div class="col-xs-6 col-sm-6 col-md-4">
    
  </div> 
</div>  