## _hello

**Description:**

A very polite component

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| image | image | :x: | :x: |
| media | media | :x: | :x: |
| paragraph | paragraph | :x: | :x: |
| text | text | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/hello/_hello.html.twig" with {
    image: "",
    media: "",
    paragraph: "",
    text: ""
} %}
```

**Location:**

 `src/templates/components/hello/_hello.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set componentClass = 'c-hello' %}

{% block content %}
    <div {{ attributes.addClass(componentClass) }}>
        {{ title_prefix }}
        {{ title_suffix }}
        {% if text %}
            <p>{{ text }}</p>
        {% endif %}
        {% if image %}
            {{ image|with(["0", "#item_attributes"], { "class": componentClass ~ "__image" }) }}
        {% endif %}
        {% if media %}
            {{ media }}
        {% endif %}
        {% if paragraph %}
            {{ paragraph }}
        {% endif %}
    </div>
{% endblock %}
```

</details>


