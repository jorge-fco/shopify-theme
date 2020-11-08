
### Images
Markup img HTML.
```html
<img  itemprop="image" alt="{{ shop.name }} : {{ shop.url }}" class="lazyload" data-src="{{ }}">
```

Markup svg HTML.
```html
<img src="{{ 'amazon.svg' | asset_url }}" alt="{{ shop.name }}">
```

**Image type**
```html
{% for image in product.images %}
  {% if product.featured_media.media_type == 'image'%}
                          <!--ITEM-->
                          <div class="product__slider__thumb" role="item">
                              <div class="product__slider__thumb__image bg-img zoom">
                                  <img data-type="{{product.featured_media.media_type}}" itemprop="image" data-zoom-src="{{ image.src | product_img_url: '1024x' }}" data-src="{{ image.src | product_img_url: '1024x' }}" alt="{{shop.name}}" class="lazyload">
                              </div>
                          </div>
                          <!--ITEM-->
                  		{% else %}
  {% endif %}
{% endfor %}
```html
