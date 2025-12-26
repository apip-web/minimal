---
layout: default
title: Tags
permalink: /tags/
---

<h1>Tags</h1>

<div id="posts">
  {% for post in site.posts %}
    <article class="post" data-tags="{{ post.tags | join: ',' }}">
      <h2>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </h2>

      <div class="post-tags">
        {% for tag in post.tags %}
          <button class="tag" data-tag="{{ tag }}">#{{ tag }}</button>
        {% endfor %}
      </div>
    </article>
  {% endfor %}
</div>

<script>
document.addEventListener('click', function (e) {
  const btn = e.target.closest('.tag');
  if (!btn) return;

  const tag = btn.dataset.tag;
  const posts = document.querySelectorAll('.post');

  posts.forEach(post => {
    const tags = post.dataset.tags.split(',');
    post.style.display = tags.includes(tag) ? '' : 'none';
  });
});
</script>

<button id="show-all">All</button>

<script>
document.getElementById('show-all')?.addEventListener('click', () => {
  document.querySelectorAll('.post').forEach(p => {
    p.style.display = '';
  });
});
</script>
