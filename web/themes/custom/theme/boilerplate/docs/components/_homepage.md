## _homepage

**Description:**

Todo

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| paragraph | paragraph | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/homepage/_homepage.html.twig" with {
    paragraph: ""
} %}
```

**Location:**

 `src/templates/components/homepage/_homepage.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set componentClass = 'c-homepage' %}

{% block content %}
    <div {{ attributes.addClass(componentClass) }}>
        {% if paragraph %}
            {{ paragraph }}
        {% endif %}
    </div>
{% endblock %}
```

</details>


