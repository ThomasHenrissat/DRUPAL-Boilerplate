## Hello

**Description:**

A very polite component

**Usage:**

```twig
{% include "@templates/components/hello/hello.html.twig" %}
```

**Location:**

 `src/templates/components/hello/hello.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{% set baseClass = 'c-hello' %}

{% embed "@templates/objects/base/base.html.twig" with { path: _self } %}
    {% block component %}
        <div class="{{ baseClass }}">
            <p>Hello world!</p>
        </div>
    {% endblock %}
{% endembed  %}
```

</details>


