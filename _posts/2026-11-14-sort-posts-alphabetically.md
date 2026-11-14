---
layout: post
title: How can I change a Jekyll blog to sort pages alphabetically, in each category?
date: 2026-11-14 7:36:00 -0000
category: Jekyll
---

In [`index.md`](https://github.com/e2xperimental/finance/blob/main/index.md), sort each category’s posts by title before looping over them. Replace the inner loop with:

```liquid
{% assign posts = category[1] | sort_natural: "title" %}
{% for post in posts %}
  <li>
    <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
```

`sort_natural` sorts titles alphabetically without treating uppercase and lowercase as different. This changes the order of posts **within each category**; it doesn’t change the order of the categories themselves. Your site uses Jekyll posts in `site.categories` here, rather than standalone pages.

The code-search results may be incomplete. [View more matching code in the GitHub UI](https://github.com/e2xperimental/finance/search?q=category&type=code).

## In the posts folder, do I still have to put the date at the beginning of each file name?


Yes—keep the `YYYY-MM-DD-` prefix for files in `_posts`, for example:

```text
2026-11-08-bonds.md
```

That’s Jekyll’s standard post filename format, and the date is used for post dating and often permalinks. Your posts also have a `date` in their front matter, but that doesn’t mean you should drop the filename date. Alphabetical sorting by title is handled separately in the Liquid template, so you don’t need to rename your files.
