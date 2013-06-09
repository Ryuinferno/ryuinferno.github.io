---
layout: page
title: Tags
header: Posts By Tag
group: navigation
---
{% include JB/setup %}

<!-- Navbar-->
<div class="navbar navbar-inverse navbar-fixed-top">
  <div class="navbar-inner">
     <div class="container">
        <button type="button" class="btn btn-navbar" data-toggle="collapse" data-target=".nav-collapse">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
           <span class="icon-bar"></span>
        </button>
        <a class="brand" href="/index.html">Blazing Hot Android Development</a>
          <div class="nav-collapse collapse">
            <ul class="nav">
              <li class="">
                <a href="/categories.html">Categories</a>
              </li>
              <li class="active">
                <a href="/tags.html">Tags</a>
              </li>
              <li class="">
                <a href="/about.html">About</a>
              </li>
            </ul>
          </div>
     </div>
  </div>
</div>

<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>


{% for tag in site.tags %} 
  <h2 id="{{ tag[0] }}-ref">{{ tag[0] }}</h2>
  <ul>
    {% assign pages_list = tag[1] %}  
    {% include JB/pages_list %}
  </ul>
{% endfor %}
