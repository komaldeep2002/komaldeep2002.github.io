---
layout: page
title: Blog Archive
---

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
  <li> OpenAI, ChatGPT to Komaldeep Kaur, Output, 09 April 2023 </li>
    {% endfor %}
  </ul>
{% endfor %}
