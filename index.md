<!-- must not put anything here?? -->
# Hi!
---

<zero-md src="https://raw.githubusercontent.com/spir0th/spir0th/main/README.md">
    <template>
        <link rel="stylesheet" href="{{ "/assets/css/style.css" | relative_url }}">
        {%if site.color-scheme %}
            <link rel="stylesheet" href="{{ "/assets/css/colors-ColorScheme.css?v=" | replace: "ColorScheme", site.color-scheme | append: site.github.build_revision | relative_url }}">
        {% else %}
            <link rel="stylesheet" href="{{ "/assets/css/colors-auto.css?v=" | append: site.github.build_revision | relative_url }}">
        {% endif %}
    </template>
</zero-md>