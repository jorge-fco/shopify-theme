# Collections
#### Title
```html
<h4>{{ collection.title }}</h4>
<p>{{ collection.description }}</p>
```

#### Collections
```html
{% for collection in collections %}
{% endfor %}
```

#### Products in collection
```html
{% for product in collection.products %}
  <article>
    <p>{{ product.type }}</p>
    <h4>{{ product.title }}</h4>
    
    <a href="{{ product.url }}" role="button">Comprar</a>
  </article>
{% endfor %}
```

#### Tags
```html
{% for tag in collection.all_tags %}
{% assign current = tag %}
{{ collection.url }}/{{ tag | handle }}
<span>{{ tag }}</span>
{% endfor %}
```

Image.
```html
<img  itemprop="image" alt="{{shop.url}}" class="lazyload" data-src="{{ collection.image | img_url: '800x800' }}">
```
 
### Listado de colecciones.
```
{%- for product in collection.all_products -%}
{%- endfor -%}
```

**Thumb image**
```html
{% for image in product.images limit: 1%}
  <div class="thumb">
    <img data-src="{{ image.src | img_url: '1024x' }}" alt="{{product.title}} : {{shop.name}}" class="lazyload">
  </div>
{% endfor %}
```

Folder /**sections**
```
list-collections-template.liquid
```

Item collection list.

Folder **include**
```
collection-grid-item.liquid
```

