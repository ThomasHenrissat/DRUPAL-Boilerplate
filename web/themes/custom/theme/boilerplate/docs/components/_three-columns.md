## _three-columns

**Description:**

Todo

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| title | text | :x: | :x: |
| content | content | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/three-columns/_three-columns.html.twig" with {
    title: "",
    content: ""
} %}
```

**Location:**

 `src/templates/components/three-columns/_three-columns.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set componentClass = 'c-three-columns' %}

{% block content %}
    <div {{ attributes.addClass(componentClass) }}>
        {{ title_prefix }}
        {{ title_suffix }}
        {% if title %}
            <h2 class="{{ componentClass }}__title">{{ title }}</h2>
        {% endif %}
        {% if content %}
            <div class="{{ componentClass }}__content">
                {{ content }}
            </div>
        {% endif %}
    </div>
{% endblock %}
```

</details>


