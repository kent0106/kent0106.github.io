---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">
        <h1>BeiYuu</h1>
        <a href="http://weibo.com/beiyuu/" target="_blank"><img src="http://www.weibo.com/favicon.ico" alt="" width="25"/></a>
        <a href="http://www.douban.com/people/beiyuu/" target="_blank"><img src="http://www.douban.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://instagram.com/beiyuu/" target="_blank"><img src="http://d36xtkk24g8jdx.cloudfront.net/bluebar/00c6602/images/ico/favicon.ico" alt="" width="22"/></a>
      </div>
      <div id="particles-js"></div>
    </div>

    <div class="index-content">
      <ul class="artical-list">
        {% for post in site.categories.blog %}
        <li>
          <a href="{{ post.url }}" class="title">{{ post.title }}</a>
          <div class="title-desc">{{ post.description }}</div>
        </li>
        {% endfor %}
      </ul>
    </div>
  </div>

<div id="pagination"> 
<div class="pagenavi"> 
<span class="page_number">第{{paginator.page}}页/共{{paginator.total_pages}}页</span> 
<a href="/">第一页</a> 
{% if paginator.previous_page %} 
{% if paginator.previous_page == 1 %} 
<a href="/" class="current"><<前一页</a> 
{% else %} 
<a href="/page{{paginator.previous_page}}"><<前一页</a> 
{% endif %} 
{% else %} 
<span><<前一页</span> 
{% endif %} 
{% for count in (2..paginator.total_pages) limit:8 %} 
{% if count == paginator.page %} 
<span class="current-page">{{count}}</span> 
{% else %} 
<a href="/page{{count}}">{{count}}</a> 
{% endif %} 
{% endfor %} 

{% if paginator.next_page %} 
<a href="/page{{paginator.next_page}}">后一页>></a> 
{% else %} 
<span>后一页>></span> 
{% endif %} 
<a href="/page{{paginator.total_pages}}">最后一页</a> 
</div> 
</div>
  
</body>
