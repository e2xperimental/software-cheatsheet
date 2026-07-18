---
layout: post
title: How to install yt-dlp and ffmpeg using Homebrew on a MacBook
date: 2026-07-17
category: Macbook
---

[yt-dlp](https://github.com/yt-dlp/yt-dlp/) lets you download audio and/or video from long YouTube videos — safely, cleanly, and without restrictions.

⸻

## Step 1: Install Homebrew (if you haven’t already)

Homebrew is a package manager that makes installing tools like yt-dlp easy.

To check if you already have it:

Open Terminal and type:

`brew --version`

If it says something like Homebrew 4.x.x, you’re good to go.
If not, install it with:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Let it run until complete. You might be asked for your Mac password.

⸻

## Step 2: Install yt-dlp

In the same Terminal window, type:

`brew install yt-dlp`

Wait for it to install — it’ll also grab dependencies like Python if needed.

⸻

## Step 3: Install ffmpeg using Homebrew on Your Mac.

`yt-dlp needs ffmpeg (and its companion ffprobe) to convert the downloaded .webm audio into .mp3 files.`

In Terminal, type:

`brew install ffmpeg`

Let it install — it might take a few minutes. This adds both ffmpeg and ffprobe to your system path, so yt-dlp can find and use them automatically.

⸻

## Next steps

- [Save YouTube videos](https://e2xperimental.github.io/software-cheatsheet/macbook/2026/07/17/save-youtube-videos.html)
- [Save YouTube videos as audio mp3](https://e2xperimental.github.io/software-cheatsheet/macbook/2026/07/17/save-youtube-videos-as-mp3.html)
