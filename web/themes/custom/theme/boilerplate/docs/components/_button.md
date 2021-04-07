## _button

**Description:**

Todo

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| icon | text | :x: | :x: |
| label | text | :x: | :x: |
| url | text | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/button/_button.html.twig" with {
    icon: "",
    label: "",
    url: ""
} %}
```

**Location:**

 `src/templates/components/button/_button.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set componentClass = 'c-button' %}

{% block content %}
    <a class="{{ componentClass }}" href="{{ url }}">
        <span class="{{ componentClass }}__label">{{ label }}</span><class="{{ componentClass }}__icon"span>{{ icon }}</span>
    </a>
{% endblock %}
```

</details>


