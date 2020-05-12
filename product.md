# Product

**Images.**
```
{% for image in product.images %}
    <img src="{{ image.src | product_img_url: 'large' }}">
{% endfor %}
```

**Description.**
```
<p>{{product.content}}</p>
```

**Price.**
```
<data>{{ product.price | money_with_currency }}</data>
```

**Collection.**
```
{% for collection in product.collections limit : 1%}
    {{ colection.title }}
{% endfor %}
```
