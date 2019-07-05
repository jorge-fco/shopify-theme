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
Folder /**sections**
```
list-collections-template.liquid
```

Item collection list.

Folder **include**
```
collection-grid-item.liquid
```

