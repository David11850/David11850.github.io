---
layout: categories
title: Algorithm
description: 算法学习笔记与代码实现
keywords: 算法, algorithm, 数据结构, leetcode
comments: false
menu: 算法
permalink: /algorithm/
---

<section class="container posts-content">
{% assign algorithm_posts = site.posts | where_exp: "post", "post.categories contains 'algorithm'" %}
{% if algorithm_posts.size > 0 %}
<ol class="posts-list">
{% for post in algorithm_posts %}
<li class="posts-list-item">
<span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
<a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ol>
{% else %}
<div class="empty-state">
  <p>还没有算法相关的文章，开始写第一篇吧。</p>
  <p class="empty-hint">在文章的 categories 里加上 "algorithm" 标签即可出现在这里。</p>
</div>
{% endif %}
</section>
