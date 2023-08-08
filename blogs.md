# Blogs
---

<ul>
  {% for post in site.posts reversed %}
    <li>
      <small>
        {{ post.date | date: "%-d %B %Y" }}
        -
        {{ post.categories | first }}
      </small>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
    <hr>
  {% endfor %}
</ul>