# Cart.
- Empty Cart
- Form
- Remove
- Image
- Title
- Collection
- Price
- Quantity
- Line price
- Subtotal
- CheckOut

#### Empty
```html
{% if cart.item_count > 0 %}
  //
{% else %}
  //
{% endif %}
```

#### Each
```html
{% for item in cart.items %}
{% endfor %}
```

**Cart items**

Cantidad.
```
{{ item.quantity }}
```

Precio.
```
{{ item.price | money }}
```

Total.
```
{{ item.line_price | money }}
```


