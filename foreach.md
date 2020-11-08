**Foreach.**
```html

{% for product in collection.products %}
  <article role="item">
    <h4>{{product.title}}</h4>
  </article>
{% endfor %}

```

**Limit.**
```html

{% for product in collection.products limit : 4%}
  <article>
    <h4>{{product.title}}</h4>
  </article>
{% endfor %}

```

**Loop.**
```html

{% for product in collection.products %}
  <article data-num="{{forloop.index}}">
     <h4>{{product.title}}</h4>
  </article>
{% endfor %}

```

**Loop and if**
```html

{% for product in collection.products %}

  {% if forloop.index==1 %}
      <article data-num="{{forloop.index}}">
          <h4>{{product.title}}</h4>
      </article>
  {% else %}
      <article data-num="{{forloop.index}}">
          <h4>{{product.title}}</h4>
      </article>
  {% endif %}
{% endfor %}

```

**Break.**
```html

{% for product in collection.products %}

  {% if forloop.index==1 %}
      <article data-num="{{forloop.index}}">
          <h4>{{product.title}}</h4>
      </article>
      {% break %}
  {% endif %}
{% endfor %}

```

**Increment.**
```html

{% for product in collection.products %}
  
{% endfor %}

```
