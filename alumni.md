---
layout: page
title: Alumni
subtitle: 
show_sidebar: false
permalink: /people/alumni/
---

{% for category in site.data.people.alumni %}
<div class="mb-6">
    <h3 class="title is-4">Former {{ category.category }}</h3>
    <div class="columns is-multiline">
        {% for member in category.members %}
        <div class="column is-one-quarter-desktop is-one-third-tablet">
            <div class="card">
                {% if member.image %}
                <div class="card-image">
                    <figure class="image is-4by3">
                        <img src="{{ member.image | relative_url }}" alt="Photo of {{ member.name }}" style="object-fit: contain;">
                    </figure>
                </div>
                {% endif %}
                <div class="card-content has-text-centered">
                    <p class="title is-5">
                        {% if member.link %}<a href="{{ member.link }}" target="_blank" rel="noopener noreferrer">{% endif %}
                            {{ member.name }}
                        {% if member.link %}</a>{% endif %}
                    </p>
                    <p class="subtitle is-6">{{ member.role }}</p>
                    {% if member.now %}<p><strong>Now at:</strong> {{ member.now }}</p>{% endif %}
                </div>
            </div>
        </div>
        {% endfor %}
    </div>
</div>
{% endfor %}