---
layout: post
title: Build a simple Jekyll site on GitHub Pages (web-only)
date: 2026-05-02 10:00:00 -0000
category: GitHub
---
# 1) Create the special repository

1. Sign in to GitHub → top-right + → New repository.
2. Name it exactly YOURUSERNAME.github.io (replace with your GitHub username). Turn on Add README → Create repository. 

# 2) Turn on GitHub Pages

1. In your repo, go to Settings → Pages (left sidebar under “Code and automation”).
2. Under Build and deployment → Source, choose Deploy from a branch.
3. Under Branch, choose main and /(root), then Save.
4. After a minute or two, visit https://YOURUSERNAME.github.io. (It can take up to ~10 minutes for first publish.)

# 3) Add minimal Jekyll files (still on the website)

1. Back on the Code tab, click Add file → Create new file.
2. Create a file named _config.yml with this content, then Commit changes:

theme: jekyll-theme-minimal
title: My Site
description: Hello from GitHub Pages + Jekyll

That theme: line tells Pages to build the site with Jekyll and apply one of GitHub’s built-in themes. You can swap jekyll-theme-minimal for any supported theme later.

3. Create another new file named index.md:

---
layout: default
title: Home
---

# Welcome
This page was built with **Jekyll** on **GitHub Pages** — no terminal!

Commit, then refresh your site URL. (Small publishes may also take a few minutes.)
