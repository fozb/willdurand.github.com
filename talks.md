---
layout: page
title: Talks
tagline: Talks I gave.
---

Most of my slides are available on [Speaker
Deck](https://speakerdeck.com/willdurand), and the sources can be found at:
[slides.williamdurand.fr](http://slides.williamdurand.fr/).

---

<ul class="talks">
  {% for data in site.data.talks %}
  <h2 class="title">{{ data.year }}</h2>

  <ul class="talks-by-year {{ data.year }}">
    {% for talk in data.talks %}
    <li>
      {{ talk.title }}
      - <em class="at">{{ talk.at }}</em>
      - [<a href="{{ talk.slides_url }}">slides</a>]{% if talk.video_url %} [<a href="{{ talk.video_url }}">video</a>]{% endif %}{% if talk.post_url %} [<a href="{{ talk.post_url }}">post</a>]{% endif %}
    </li>
    {% endfor %}
  </ul>
  {% endfor %}
</ul>
