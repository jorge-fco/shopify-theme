# Product

#### Images
```
{% for image in product.images %}
    <img src="{{ image.src | img_url }}">
{% endfor %}
```

#### Description
```
<p>{{ product.content }}</p>
```

#### Price
```
<data>{{ product.price | money_with_currency }}</data>
```

#### Variants


**Collection.**
```
{% for collection in product.collections limit : 1 %}
    {{ colection.title }}
{% endfor %}

{% for collection in product.collections limit : 1 %}
    {% assign current = collection.title | handle %}
    {% if current != 'todos' %}
        {{ colection.title }}
    {% endif %}
{% endfor %}
```

**Related products**

#### Metafields
```
{% assign list_products = product.metafields.custom.list_products.value %}

{% for product in list_products %}
   {{ product.title }} 
{% endfor %}
```
