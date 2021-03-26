## _media

**Description:**

To render all medias

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| image | image | :x: | :x: |


**Usage:**

```twig
{% include "@templates/objects/media/_media.html.twig" with {
    image: ""
} %}
```

**Location:**

 `src/templates/objects/media/_media.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% extends "@templates/objects/base/_base.html.twig" %} {% set path = _self %}

{% set objectClass = 'o-media' %}

{% block content %}
    <div {{ attributes.addClass(objectClass) }}>
        {{ title_suffix.contextual_links }}
        {{ image|with(["0", "#item_attributes"], { "class": objectClass ~ "__image" }) }}
    </div>
{% endblock %}
```

</details>


