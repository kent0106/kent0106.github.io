---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">
        <h1>your name</h1>
       <span>联系电话</span>
       <span>联系电话</span>
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


</body>
