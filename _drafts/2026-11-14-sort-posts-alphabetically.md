---
layout: post
title: How can I change a Jekyll blog to sort pages alphabetically, in each category?
date: 2026-11-14 7:36:00 -0000
category: Jekyll
---

Yes—keep the `YYYY-MM-DD-` prefix for files in `_posts`, for example:

```text
2026-11-08-bonds.md
```

That’s Jekyll’s standard post filename format, and the date is used for post dating and often permalinks. Your posts also have a `date` in their front matter, but that doesn’t mean you should drop the filename date. Alphabetical sorting by title is handled separately in the Liquid template, so you don’t need to rename your files.