# Blog.

```liquid
{% for article in blog.articles %}
  <h4>{{ article.title }}</h4>
  {{ article.url }}
{% endfor %}
```
