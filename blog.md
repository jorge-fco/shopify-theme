# Blog.

**Items**
```liquid
{% for article in blog.articles %}
  <h4>{{ article.title }}</h4>
  {{ article.url }}
{% endfor %}
```

**Odd and pairs**
```liquid
{% for item in site.posts %}
  {% capture thecycle %}{% cycle 'odd', 'even' %}{% endcapture %}
  {% if thecycle == 'odd' %}
    <div>Odd</div>
  {% else %}
    <div>Pairs</div>
  {% endif %}
{% endfor %}
```

# Article.
```
{{ article.content }}
