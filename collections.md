# Collections

### Object
Title
```html
<h4>{{ collection.title }}</h4>
<p>{{ collection.description }}</p>
```

Image.
```html
<img  itemprop="image" alt="{{shop.url}}" class="lazyload" data-src="{{ collection.image | img_url: '800x800' }}">
```
 
### Listado de colecciones.

**Products collection**
```html
{% for product in collection.products %}
<article>
  <h4>{{product.title}}</h4>
  <a href="{{product.url}}">Ver</a>
</article>
{% endfor %}
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

