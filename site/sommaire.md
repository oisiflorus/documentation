<section id="ghTree" class="ghTree" data-title="tree">
    {% assign sorted-pages = site.html_pages | sort: 'title' %}
    {% for page in sorted-pages %}
        {% if page.page-type != "info" and page.url != "/" and page.url != "/404.html" %}
        <article class="ghTreeItem ghTypeFile" data-title="dir">
            <h2 class="ghTreeTitle">
                <a class="folderLink" data-title="folderLink" href="{{ page.url | relative_url }}">
                    {{ page.path | replace:'.md', '' | default: page.title }}
                </a>
            </h2>
            <p class="ghTreeExcerpt" data-title="fileExcerpt">{{ page.description }}</p>
            <a class="ghTreeReadmore" title="Lire la suite de la fiche : Animer des ateliers collaboratifs" data-title="fileReadmoreLink"
                href="{{ page.url | relative_url }}">Lire la suite de la fiche</a>
        </article>
        {% endif %}
    {% endfor %}
</section>