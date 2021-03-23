## Hello

**Description:**

A very polite component

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| image | image | :x: | :x: |
| name | string | :x: | :x: |


**Usage:**

```twig
{% include "@templates/components/hello/hello.html.twig" with {
    image: "",
    name: ""
} %}
```

**Location:**

 `src/templates/components/hello/hello.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{#
    This variable sets the base class of our component that we'll use in our markup.
    That way we can easily rename our component.
#}
{% set componentClass = 'c-hello' %}

{#
    We put our markup in a seperate variable because it's meant to be used as a block.
    If we were to put it directly in another block, the blocks it can contain would not work.

    The following variables are necessary to put in our markup for quick edit to work:
    - attributes (must be placed on the main container)
    - title_prefix (must be placed inside the main container, before the title if there is one)
    - title_suffix (must be placed inside the main container, after the title if there is one)
    These variables are received automatically from the parent template, in this case "node--hello.html.twig".
#}
{% set component %}
    <div {{ attributes.addClass(componentClass) }}>
        {{ title_prefix }}
        {{ title_suffix }}
        {% if name %}
            <p>Hello {{ name }}!</p>
        {% else %}
            <p>Hello!</p>
        {% endif %}
        {{ image|merge({ "#item_attributes": { "class": [componentClass ~ "__image"] } }) }}
    </div>
{% endset %}

{# We pass our markup as a block to the "base" object which will add Twig debugging around it #}
{% embed "@templates/objects/base/base.html.twig" with { path: _self } %}
    {% block component %}
        {{ component }}
    {% endblock %}
{% endembed  %}
```

</details>


