## _goodbye

**Description:**

A very sad component

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| text | string | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/goodbye/_goodbye.html.twig" with {
    text: ""
} %}
```

**Location:**

 `src/templates/components/goodbye/_goodbye.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set componentClass = 'c-goodbye' %}

{% block content %}
    <div {{ attributes.addClass(componentClass) }}>
        {% if text %}
            <p>{{ text }}</p>
        {% endif %}
    </div>
{% endblock %}
```

</details>


