# Projects
---

<ul style="list-style: none; padding-left: 0;">
  {% for project in site.data.projects %}
    <li>
      {% if project.icon %}
        <img src="{{ project.icon }}" width="24px" height="24px" />
      {% endif %}
      <h2>{{ project.name }}</h2>
      {% if project.tags %}
          <small>{{ project.tags | join: " &mdash; " }}</small>
      {% endif %}
      <p>{{ project.description | default: "No description provided." }}</p>
      {% if project.url %}
        <a href="{{ project.url }}" target="_blank">View full project</a>
      {% endif %}
      {% if project.url and project.download_url %}
        <br>
      {% endif %}
      {% if project.download_url %}
        <a href="{{ project.download_url }}" target="_blank">Download</a>
      {% endif %}
    </li>
    <hr>
  {% endfor %}
</ul> 