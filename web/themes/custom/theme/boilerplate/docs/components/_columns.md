## _columns

**Description:**

Column layout

**Properties:**

| Name | Type | Values | Default | Description |
|------|------|--------|---------|-------------|
| columnCount | integer | `1` `2` `3` | `2` | Number of columns to display |
| title | text | :x: | :x: |  |
| content | any | :x: | :x: | Content to display in the columns |


**Usage:**

```twig
{% include "@templates/components/columns/_columns.html.twig" with {
    columnCount: "",
    title: "",
    content: ""
} %}
```

**Location:**

 `src/templates/components/columns/_columns.html.twig`



