# Blogs
---

<ul class="no-bullets">
  {% for post in site.posts %}
    <li>
      <small>
        {{ post.date | date: "%-d %B %Y" }} &mdash; {{ post.categories | first }}
      </small>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
    <hr>
  {% endfor %}
</ul>