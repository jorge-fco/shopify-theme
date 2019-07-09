# Products
```liquid
{% for product in collections['all'].products %}
  <article>
    <h4>{{product.title}}</h4>
  </article>
{% endfor %}
```
