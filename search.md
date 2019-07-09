# Search.

**Form serarch**
```html
<section class="footer__search">
  <div class="container">
      <form action="/search" method="GET" role="search">
        <label for="search">¿QUÉ ESTÁS BUSCANDO?</label>
        <input type="search" name="q"  value="{{ search.terms | escape }}"  placeholder="Ingresa tu búsqueda aquí">
      </form>
  </div>
</section>
```

**Result**
```html
{% if search.performed %}
  <p>Resultados de la búsqueda para <span>"{{search.terms}}"</span> – Total (<span>{{search.results_count}}</span>)</p>
{% else %}
  <p>Comienza a realizar una búsqueda de un producto.</p>	
{% endif %}
```


