## _article

**Description:**

Todo

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| icon | text | :x: | :x: |
| url | text | :x: | :x: |
| rte | rte | :x: | :x: |
| title | text | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/article/_article.html.twig" with {
    icon: "",
    url: "",
    rte: "",
    title: ""
} %}
```

**Location:**

 `src/templates/components/article/_article.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set componentClass = 'c-article' %}

{% block content %}
    <div {{ attributes.addClass(componentClass) }}>
        {{ title_prefix }}
        {{ title_suffix }}
        {% if icon %}
            {{ icon }}
        {% endif %}
        {% if title %}
            <h3>{{ title }}</h3>
        {% endif %}
        {% if rte %}
            {{ rte }}
        {% endif %}
        {% include "@templates/components/button/_button.html.twig" with {
            icon: "icon",
            label: "En savoir plus",
            url: url
        } %}
    </div>
{% endblock %}
```

</details>


