## _goodbye

**Description:**

A very sad component

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| bold | boolean | :x: | `0` |
| text | text | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/goodbye/_goodbye.html.twig" with {
    bold: "",
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
{% set classes = [
    componentClass,
    bold == "On" ? componentClass ~ '--bold' : ''
] %}

{% block content %}
    <div {{ attributes.addClass(classes) }}>
        {% if text %}
            <p>{{ text }}</p>
        {% endif %}
    </div>
{% endblock %}
```

</details>


