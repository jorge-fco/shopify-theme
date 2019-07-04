Form serarch

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
