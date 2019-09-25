# Product
```
{% for image in product.images %}
    <img src="{{ image.src | product_img_url: 'large' }}">
{% endfor %}
```

```
<data>{{ product.price | money_with_currency }}</data>
```
