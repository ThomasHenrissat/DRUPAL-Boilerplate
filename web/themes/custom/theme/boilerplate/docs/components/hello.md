## Hello

**Description:**

A very polite component

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| attributes | array | `attributes` | :x: |
| name | string | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/hello/hello.html.twig" with {
    attributes: "",
    name: ""
} %}
```

**Location:**

 `src/templates/components/hello/hello.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% set componentClass = 'c-hello' %}

{% embed "@templates/objects/base/base.html.twig" with { path: _self } %}
    {% block component %}
        <div {{ attributes.addClass(componentClass) }}>
            {% if name %}
                <p>Hello {{ name }}!</p>
            {% else %}
                <p>Hello!</p>
            {% endif %}
        </div>
    {% endblock %}
{% endembed  %}
```

</details>


