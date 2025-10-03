---
layout: page
title: Current Members
subtitle: 
show_sidebar: false
permalink: /people/current/
---

{% for category in site.data.people.current %}
<div class="mb-6">
    <h3 class="title is-4">{{ category.category }}</h3>

    {% if category.members %}
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
                    </div>
                </div>
            </div>
            {% endfor %}
        </div>
    {% endif %}

    {% if category.subcategories %}
        {% for subcategory in category.subcategories %}
        <div class="columns is-multiline">
            {% for member in subcategory.members %}
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
                        <p class="title is-5">{% if member.link %}<a href="{{ member.link }}" target="_blank" rel="noopener noreferrer">{% endif %}{{ member.name }}{% if member.link %}</a>{% endif %}</p>
                        <p class="subtitle is-6">{{ member.role }}</p>
                    </div>
                </div>
            </div>
            {% endfor %}
        </div>
        {% endfor %}
    {% endif %}
</div>
{% endfor %}