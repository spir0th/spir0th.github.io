# Projects
---

<ul>
  {% for project in site.data.projects %}
    <li>
	  {% if project.icon %}
        <img src="{{ project.icon | relative_url }}" />
      {% endif %}
	  <h2>{{ project.name }}</h2>
	  <p>{{ project.description | default: "No description provided." }}</p>
      <p>
		{% if project.url %}
			<a href="{{ project.url }}" target="_blank">View full project</a>
		{% endif %}
		{% if project.url and project.download_url %}
			&mdash;
		{% endif %}
		{% if project.download_url %}
        <a href="{{ project.download_url }}" target="_blank">Download</a>
        {% endif %}
	  </p>
    </li>
    <hr>
  {% endfor %}
</ul> 