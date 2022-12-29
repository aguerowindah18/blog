---
layout: page
title: Bookmarks
description: Online tools dan resources yang berguna
---

Beberapa online tools, database, referensi, cheatsheets, dll. Yang berguna untuk bekerja setiap harinya.

Jika ada saran untuk ditambahkan atau saran lainnya, silahkan komen di bawah.

{% for category in site.data.bookmarks %}
{% assign items = category[1] | sort_natural: "name" %}

### {{ category[0] | capitalize }}:

{% for item in items %}

- [{{ item.name }}]({{ item.link }}){:target="\_blank"}
  - {{ item.description }}
    {% endfor %}
    {% endfor %}

---

{% if site.comments_repo %}
{% include comments.html %}
{% endif %}
