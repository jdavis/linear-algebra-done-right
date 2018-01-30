---
layout: default
title: Home
description:
    Solutions and notes from the book Linear Algebra Done Right.
---

# Linear Algebra Done Right

<div class="figure right">
    <img src="{{site.baseurl}}/img/book.png" width="200" alt="Linear Algebra Done Right cover">
    <span>Cover of Axler's book</span>
</div>

This is the site that I'll use to store my notes and exercise solutions as I
work through the second edition of [Sheldon Axler][axler]'s book called [Linear
Algebra Done Right][linear-site] ([Amazon link][amzn-link]).

{% for collection in site.collections.chapters %}
## {{collection.name}} - {{collection.title}}

{{  collection.description }}

### Exercises
<ul class="pretty">
    {% for exercise in collection.docs %}
    <li>
        <a href="{{site.baseurl}}{{ exercise.url }}">
            Exercise {{exercise.number}}
        </a>
    </li>
    {% endfor %}
</ul>
{% endfor %}

[amzn-link]: http://amzn.com/3319110799
[axler]: http://www.axler.net/
[linear-site]: http://linear.axler.net/
