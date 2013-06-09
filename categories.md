---
layout: page
title: Categories
header: Posts By Category
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
              <li class="active">
                <a href="/categories.html">Categories</a>
              </li>
              <li class="">
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
  {% assign categories_list = site.categories %}
  {% include JB/categories_list %}
</ul>


{% for category in site.categories %} 
  <h2 id="{{ category[0] }}-ref">{{ category[0] | join: "/" }}</h2>
  <ul>
    {% assign pages_list = category[1] %}  
    {% include JB/pages_list %}
  </ul>
{% endfor %}

