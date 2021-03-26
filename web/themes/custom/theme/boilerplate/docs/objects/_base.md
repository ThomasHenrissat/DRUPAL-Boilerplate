## _base

**Description:**

This template is embeded in all our components to add a custom Twig Debugging.
Without it there would be no `BEGIN OUTPUT` and `END OUTPUT` in the inspector because the Twig Debugger cannot see the files in our custom namespaces.
The variable `twigDebugEnabled` is a variable we've added to the preprocess of our theme in `theme.theme`, we use it to know if the Twig debbuging is enabled.

**Properties:**

| Name | Type | Values | Default |
|------|------|--------|---------|
| path | string | `_self` | :x: |


**Blocks:**

- `content`

**Usage:**

```twig
{% embed "@templates/objects/base/_base.html.twig" with {
    path: ""
} %}
    {% block content %}{% endblock %}
{% endembed %}
```

**Location:**

 `src/templates/objects/base/_base.html.twig`

**Code:**

<details>
    <summary>Click to expand</summary>

```twig
{# This object allows us to add twig debbuging to our templates #}

{% if twigDebugEnabled %}
    <!-- BEGIN OUTPUT from '{{ directory ~ "/" ~ path[1:] }}' -->
{% endif %}
    {% block content %}{% endblock %}
{% if twigDebugEnabled %}
    <!-- END OUTPUT from '{{ directory ~ "/" ~ path[1:] }}' -->
{% endif %}
```

</details>


