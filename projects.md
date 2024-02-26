# Projects
---

<ul class="no-bullets">
  {% for project in site.data.projects %}
    <li>
	  {% if project.icon %}
        <img src="{{ project.icon | relative_url }}" />
      {% endif %}
	  <h2>{{ project.name }}</h2>
	  <p>{{ project.description | default: "No description provided." }}</p>
      <p>
		{% if project.download_url %}
			<button onclick="redirectInNewTab('{{ project.download_url }}');">Download</button>
        {% endif %}
		{% if project.url %}
			<button onclick="redirectInNewTab('{{ project.url }}');">Source code</button>
		{% endif %}
	  </p>
    </li>
    <hr>
  {% endfor %}
</ul> 