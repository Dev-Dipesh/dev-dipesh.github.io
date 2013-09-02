---
layout: page
title: "About Us"
description: "Those old hacky days..."
group: navbar
weight: 5
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
  <li class="active">About Us</li>
</ol>
<div class="row">
<div class="col-xs-12 col-sm-6 col-md-8">
<div class="one-edge-shadow">
<p>
It is quite funny, no matter how many times I tell this story, I never get tired of it. Even now, as I am writting it down, I can still feel that shimering pride that one feels even long after achieving something that is worth telling, worth keeping. Our story is quite short, but as with all good things, it is a story of hard work, dedication, and cataclysms (how can we forget them?), for all good stories always need to have one right?
<br />
We started in early 2013 as the <a href="http://www.codecademy.com/groups/html-projects">Web Development Tutorials</a> group at <a href="http://www.codecademy.com/">CodeCademy.com</a> with a passion for making websites and sharing resources. Originally created by <a href="http://www.codecademy.com/wafflegnome">Waffle</a> (original leader) the objective of the group was to be a place where people could practice their skills by making a series of web challenges.
<br />
This however, changed quickly when <a href="http://www.codecademy.com/fl4m3ph03n1x">Pedro Martins</a> arrived. Being an hyperative man, with a hell of a fire in his hard and perhaps too much free time, he immediatly saw a chance to make that group something else, something bigger. He believed that CodeCademy, although a nice place for begginners, had loads of problems. To be perfectly honest, CodeCademy still has loads of problems, but that is another matter for another story. Instead of joining the pain train, he decided to become part of a solution. The group was then the perfect medium for that. People often say the first step into solving a problem is admiting it. They know not how right they are.
<br />
At that time, CodeCademy was still quite new, and our group was competing with thousands of other groups for attention. However, there was one thing that none of them had: quaility tutorials and information. It was this revelation by Pedro that led the group to new heights. With that in mind Pedro started making a serie of guides and tutorials, aided by Waffle charged with making the challenges. The success that resulted from the partnership astonished both of them. A group with just a few weeks was now competing with others for thousands of users. Such a success only demanded more attention from them however ... and Waffle had to leave, thus giviving the leadership of the group to Pedro Martins, a co-leader at the time.
<br />
As time went by the group kept growing, entering in direct competition with other well established groups Web Development groups. Things seemed to be going well right? Wrong... You see, life is not without irony. As we were sky-rocking our way to the top, the administrators at CodeCademy launched quite a bomb - there were just to many groups to maintain, they had to trim it down to just a dozen of lucky ones. CodeCademy's groups, as we knew them, were going to end.
<br />
It is easy for one to simply pack-up and go home after hearing such a thing. Some may say, it is the right thing to do - after all, there will be nothing left. What chance would we have? Turns out, a damn good one. After so much effort and work making guides and tutorials, it would be a shame to just burn it all. Believe it or not, some of the people working in CodeCademy's staff (specially <a href="http://www.codecademy.com/lindaliukas">Linda Liukas</a>) had keep an eye on him, and on the group. After some talking, and a promotion to moderator, Pedro received a wonder new - his group was going to be one of those with enough luck to survive the D-day cut. His work had payed off.
<br />
There were more then 1000 groups in CodeCademy at the time. After D-day, only 25 made it. We were one of them.
<br />
So now what? With the drastic decrease in groups, there were more people then ever looking for a place to stay, a group to enter. This eventually meant a new influx of users and an increased responsability. To cope with such an event, Pedro then started a set of new programs and voting polls, to decide the best course of action - but the feedback was just too big for one man to handle. Even with a group containing thousands of people, Pedro felt all alone in his tasks, his duty.
<br />
It was then that a young man, <a href="http://www.codecademy.com/dev-dipesh">Dipesh Bhardwaj</a> came in his help. Sharing too a big will to learn they both started making more guides and tutorials. By this time, new people had arrived. Some of the incomers were heavily interested, such as [Ksenia Dylova](http://www.codecademy.com/ksenja). Being a student with an enourmous thirst for knowledge and a will to help, she fited immediatly, taking lessons and giving support to the people in the forums. Later on, she also made a few guides sharing her experience.
<br />
And in this long text you have met most of the co-leaders of our group. Except for two: <a href="http://www.codecademy.com/thelulzboat">LulzSec</a>, a Brazillian pirate recently promoted due to his contributions in resources, and ... good old Waffle. Who would have known that our original creator would return one day later. Being busy as all people are, Pedro is still the leader of the group, but if you think you have what it takes, then go on and make a guide or share a resource. You may one day later become a co-leader as well of one of the largets groups in CodeCademy.</p>
</div>
</div>
<div class="col-xs-6 col-sm-6 col-md-4">
  <h1>AUTHORS</h1>
  <h4 id="sub">Nimbel Team</h4>
  <hr />
  <div class="row">
   <div class="col-xs-4 col-sm-4 col-md-5">   
	<img src="{{ ASSET_PATH }}twitter/images/dipesh1.jpg" class="img-circle img-responsive tooltip-test" data-toggle="tooltip" data-placement="top" title="" data-original-title="Dipesh Bhardwaj">
   </div>
   <div class="col-xs-4 col-sm-4 col-md-5">	
	<img src="{{ ASSET_PATH }}twitter/images/pedro.jpg" alt="neo" class="img-circle img-responsive tooltip-test" data-toggle="tooltip" data-placement="top" title="" data-original-title="Pedro Martins">
   </div>	
  </div>
  <br />
  <div class="row">
   <div class="col-xs-4 col-sm-4 col-md-5">	
	<img src="{{ ASSET_PATH }}twitter/images/revimg.png" alt="mark" class="img-circle img-responsive tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Ksenia Dylova">
   </div>
   <div class="col-xs-4 col-sm-4 col-md-5">	
	<img src="{{ ASSET_PATH }}twitter/images/revimg.png" alt="neo" class="img-circle img-responsive tooltip-test" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="Waffle Gnome">
   </div> 	
  </div>	
</div>
</div>
</div>
<hr />
</div>