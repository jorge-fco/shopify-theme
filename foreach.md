For.
```html
{% for product in collection.products %}
  <h4>{{product.title}}</h4>
{% endfor %}
```

Limit.
```html
{% for product in collection.products limit : 4%}
  <article>
    <h4>{{product.title}}</h4>
  </article>
{% endfor %}
```

Loop.
```html
{% for product in collection.products %}
{% endfor %}
```

Increment.
```html
{% for product in collection.products %}
{% endfor %}
```
