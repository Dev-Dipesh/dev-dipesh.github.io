---
layout: page
title: "Index"
description: ""
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
  <li><a href="/blog/index.html"><span class="glyphicon glyphicon-home"></span></a></li>
  <li class="active">Tutorials</li>
</ol>

<div class="row">
    <div class="col-xs-12 col-sm-6 col-md-8">
		{% for post in site.posts %}

			<div class="row">
        		<div class="col-md-3 one-edge-shadow3">
          			<img src="{{ post.description }}" class="pull-left img-circle img-responsive tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="{{ post.author }}">
        		</div>
        	
        		<div class="col-md-9">
				    <div class="row">
				        <div class="col-md-4">
				            <p>
				                <h5><small><strong>{{ post.date | date: "%B %e, %Y" }}</strong> . {{ post.category }}</small></h5>
				            </p>
				        </div>

				        <div class="col-md-3">
				            <p class="fb-like" data-href="http://developers.facebook.com/docs/reference/plugins/like" data-width="450" data-layout="button_count" data-show-faces="false" data-send="true"></p>
				        </div>

				        <div class="col-md-2">
				            <p class="g-plusone" data-size="medium"></p>
				        </div>

				        <div class="col-md-3">
				            <p>
				            	<a href="https://twitter.com/share" class="pull-left twitter-share-button">Tweet</a>
				            </p>
				        </div>
				    </div>
		    
				    <h3>
				    	<a href="{{ post.url }}" style="text-decoration: none;">{{ post.title }}</a>
				    	<a href=""><img src="{{ ASSET_PATH }}twitter/images/download_icon.png" class="pull-right tooltip-test" style="width:50px; height:50px;"  data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Download as PDF"></a>
				    </h3>

				    <p>
				    	<h5><em><small>by <a href="#" class="tooltip-test" data-toggle="tooltip" data-placement="right" title="" data-original-title="All Post by {{ post.author }}."><strong>{{ post.author }}</strong></a></small></em></h5>
				    </p>
				    
				    <hr class="hr" />

				    <p>
				    	<h5>{{ post.excerpt }}</h5>
				    </p>
				    
				    <br />
				    
				    <h5>
				    	<p><strong>Continue reading <a href="{{ post.url }}">{{ post.title }}</a></strong></p>
				    	<p><strong>Tags <span class="glyphicon glyphicon-tags"></span>  <small>{{ post.tags }}</small></strong></p>
				    </h5>
				    
				    <hr id="post_bottom_border" />
		    	</div>      			
			</div>
		{% endfor %}
	</div>
	
  <div class="col-xs-6 col-sm-6 col-md-4 one-edge-shadow2">

  	<h4>CATEGORIES</h4>
  	<div class="categories">
  		<p><h4>
	  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="left" title="" data-original-title="5 Posts">CSS</a></span>
	  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="top" title="" data-original-title="5 Posts">HTML</a></span>
	  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="top" title="" data-original-title="5 Posts">Design</a></span>
	  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="right" title="" data-original-title="5 Posts">Photoshop</a></span>
  		</h4></p>
  		
  		<p><h4><span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="left" title="" data-original-title="5 Posts">Tools</a></span>
  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="top" title="" data-original-title="5 Posts">Inspiration</a></span>
  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="5 Posts">Freelance</a></span>
  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="right" title="" data-original-title="5 Posts">Showcase</a></span></h4></p>

  		<p><h4><span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="5 Posts">Tutorials</a></span>
  		<span><a href="" class="label label-info tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="5 Posts">Javascript</a></span></h4></p>
  	</div>
  	<hr />
  	<h4>SEARCH</h4>
	<div class="input-group">
	    <input type="text" class="form-control" id="typeahead" />
		<span class="input-group-addon"><span class="glyphicon glyphicon-search"></span></span>
	</div>
	<hr />
	
	<h4>Follow Us<span style="color:gray"><small><strong> (we love stalkers)</strong></small></span></h4>

	<div class="widget_nav_menu">

				<ul class="socialIcons">
						<li class="vimeo tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Vimeo"><a href="#">vimeo </a></li>
						<li class="facebook tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Facebook"><a href="#">facebook </a></li>
						<li class="linkedin tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Linkedin"><a href="#">linkedin </a></li>
						<li class="twitter tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Twitter"><a href="#">twitter</a></li>
						<li class="pinterest tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Pinterest"><a href="#">pinterest</a></li>
						<li class="flickr tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Flickr"><a href="#">flickr </a></li>
						<li class="digg tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Digg"><a href="#">digg</a></li>
						<li class="yahoo1 tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Yahoo"><a href="#">yahoo1</a></li>
						<li class="reddit tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Reddit"><a href="#">reddit</a></li>
						<li class="googleplus tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Google Plus"><a href="#">googleplus</a></li>
						<li class="stumbleupon tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Stumbleupon"><a href="#">stumbleupon</a></li>
						<li class="skype tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Skype"><a href="#">skype</a></li>
						<li class="deviantart tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Devianart"><a href="#">deviantart</a></li>
						<li class="delicious tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Delicious"><a href="#">delicious </a></li>
						<li class="tumblr tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Tumblr"><a href="#">tumblr </a></li>
						<li class="lastfm tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Last FM"><a href="#">lastfm </a></li>
						<li class="youtube tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Youtube"><a href="#">youtube</a></li>
						<li class="friendfeed tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Friend Feed"><a href="#">friendfeed </a></li>
						<li class="myspace tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="MySpace"><a href="#">myspace </a></li>
						<li class="rss tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="RSS"><a href="#">rss </a></li>
						<li class="badoo tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Badoo"><a href="#">badoo </a></li>
						<li class="dribble tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Dribble"><a href="#">dribble </a></li>
						<li class="blogger tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Blogger"><a href="#">blogger </a></li>
						<li class="homeicon tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Home Page"><a href="index.html">homeicon</a></li>
						<li class="phone tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="xxx-xxx-xxx"><a href="#">phone </a></li>
						<li class="email tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="itdeveloper03@gmail.com"><a href="#">email </a></li>
						<li class="picassa tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Picasa"><a href="#">picassa </a></li>
						<li class="livejournal tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Live Journal"><a href="#">livejournal </a></li>
						<li class="bebo tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Bebo"><a href="#">bebo </a></li>
						<li class="technorati tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Technorati"><a href="#">technorati </a></li>
						<li class="newsvine tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="News Vine"><a href="#">newsvine</a></li>
						<li class="wordpress tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Wordpress"><a href="#">wordpress </a></li>
						<li class="yelp tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Yelp"><a href="#">yelp </a></li>
                   </ul>
                   <hr>
	</div>
      
    	<h4>RECENT POSTS<span style="color:gray"><small><strong> (more web goodness)</strong></small></span></h4>
    	<hr>
    	{% for post in site.posts limit:10 %}
    		<h5><a href="{{ post.url }}">{{ post.title }}</a></h5>
    	{% endfor %}

    <hr>
    <h4>QUICK TIPS</h4>	
  	<div>
  	  <div class="mb-wrap mb-style-6">
		<blockquote cite="http://www.gutenberg.org/ebooks/600">
			<p>For what is man without desires, without free will, and without the power of choice but a stop in an organ pipe?</p>
		</blockquote>
		<div class="mb-attribution">
			<p class="mb-author">Fyodor Dostoevsky</p>
			<cite><a href="http://www.gutenberg.org/ebooks/600">Notes from the Underground</a></cite>
		</div>
	  </div>
  	</div>

  	<hr>
  	<div class="one-edge-shadow">
  <h4><u>ARCHIVE</u></h4>
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
		      <li><h5><time>{{ post.date | date:"%d %b" }}</time><p><a href="{{ post.url }}">{{ post.title }}</a></p></h5></li>
		  {% endfor %}
		  </ul>
		</section>
  	</div>

  	
  </div>  
</div>  