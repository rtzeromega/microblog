---
title: 首页
---

<section class="hero">
  <h1>写给未来自己的技术与生活笔记</h1>
  <p class="lead">这是一个用 GitHub Pages 搭建的个人博客，文章直接使用 Markdown 编写并发布。</p>
  <p><a class="button" href="{{ '/about/' | relative_url }}">了解我</a></p>
</section>

<section class="post-list-section" aria-labelledby="latest-posts">
  <h2 id="latest-posts">最新文章</h2>
  <ul class="post-list">
    {% for post in site.posts %}
      <li class="post-card">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="meta">{{ post.date | date: "%Y-%m-%d" }}</p>
        <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </li>
    {% endfor %}
  </ul>
</section>
