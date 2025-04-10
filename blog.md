# Blog.

#### Each > Items
```liquid
{% for article in blog.articles %}
  {% assign image = article.image | image_url %}
  
  <h4>{{ article.title }}</h4>
  <time>{{ article.author }}, {{ article.published_at | time_tag: format: 'date' }}</time>
  <p>{{ article.excerpt }}</p>

  <a href="{{ article.url }}">
    Leer post
  </a>
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

**Title.**
```
<h1>{{ article.title }}</h1>
```

**Author.**
```
{% if section.settings.blog_show_author %}
    <span class="article__author">{{ 'blogs.article.by_author' | t: author: article.author }}</span>
{% endif %}
```

**Date.**
```
{% if section.settings.blog_show_date %}
    <span class="article__date">
      {{ article.published_at | time_tag: format: 'date' }}
    </span>
{% endif %}
```

**Text.**
```
{{ article.content }}
```

**Comments.**
```
{% for comment in article.comments %}
  {% include 'comment' %}
{% endfor %}
```
