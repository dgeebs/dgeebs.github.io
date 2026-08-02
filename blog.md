---
layout: page
title: Blog Posts
permalink: blog
---
<div class="flex flex-col items-center min-h-screen px-6">
  <div class="w-full max-w-6xl section-light shadow-md rounded-sm p-8">
    <header class="mb-6">
      <h1 class="text-4xl font-bold mb-4">{{ page.title }}</h1>
    </header>
    <div>
      {% for post in site.posts %}
        <div class="py-1">
          <h3><a href="{{site.baseurl}}{{ post.url }}">{{ post.title}}</a></h3>
          <div class="text-sm text-gray-400">{{post.date | date: "%B %-d, %Y"}}</div>
        </div>
      {% endfor %}
    </div>
</div>


