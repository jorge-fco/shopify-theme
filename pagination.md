# Pagination

```html
{% assign count = paginate.pages %}

<div class="shop__items__pagination">
    <ul>
        <!--PREV-->
        <li>
            <a href="{{ paginate.previous.url }}" title="Prev">
                {% include 'arrow.prev' %}
            </a>
        </li>
        <!--PREV-->

        <!--NUMBERS-->
        {% for part in (1..count) %}
          <li>
            <a {% if paginate.current_page == part %}class="active"{% endif %} href="{{ collection.url }}?page={{ forloop.index }}">
              {{ forloop.index }}
            </a>
          </li>
        {% endfor %}
        <!--NUMBERS-->

        <!--NEXT-->
        <li>
            <a href="{{ paginate.previous.url }}" title="Next">
                {% include 'arrow.next' %}
            </a>
        </li>
        <!--NEXT-->
    </ul>
</div>
```
