---
layout: post
title:  "기본 레이아웃을 만들어보자!"
date:   2017-01-02
categories: jekyll update
---

일단 _layouts 폴더의 default.html을 만들어야겠다.

좋은 참고 페이지는 [이것](https://www.digitalocean.com/community/tutorials/exploring-jekyll-s-default-content) 과 [이것](https://jeremenichelli.github.io/2015/07/building-blog-jekyll-creating-layouts/) 인 것 같다.


>> Root / _includes / head.html
{% highlight text %}

<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <title>
    {% if page.title %} {{ page.title }}
    {% else %} {{ site.title }}
    {% endif %}
  </title>
  <meta name="description" content="{{ site.description }}">
  <meta name="viewport" content="width=device-width">
</head>

{% endhighlight %}


>> Root / _layouts / default.html

{% highlight text%}

<!DOCTYPE html>
<html lang="en">

  {% include head.html %}

  {% include header.html %}

  <body>
   <!--  <section class="post-wrapper">
      <p class="post-date">{{ page.date }}</p>
    </section>
    <h1 class="post-title">{{ page.title }}</h1> -->
    <article class="post-content">
      {{content}}
    </article>
  </body>

  {% include footer.html %}
</html>

{% endhighlight %}
