---
layout: post
title: How to Install and Use yt-dlp on a MacBook
date: 2026-07-17
category: Macbook
---

Absolutely, Erik! Here’s a friendly, step-by-step guide to installing and using yt-dlp on your MacBook so you can download audio from long YouTube videos — safely, cleanly, and without restrictions.

⸻

✅ Step 1: Install Homebrew (if you haven’t already)

Homebrew is a package manager that makes installing tools like yt-dlp easy.

To check if you already have it:

Open Terminal and type:

brew --version

If it says something like Homebrew 4.x.x, you’re good to go.
If not, install it with:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Let it run until complete. You might be asked for your Mac password.

⸻

✅ Step 2: Install yt-dlp

In the same Terminal window, type:

brew install yt-dlp

Wait for it to install — it’ll also grab dependencies like Python if needed.

⸻

✅ Step 3: Download Audio from YouTube

In Terminal, paste this command, replacing the URL with your video link:

yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID

This tells yt-dlp to:

* -x: extract audio only
* --audio-format mp3: convert to MP3

🗂 The MP3 file will be saved in your current Terminal folder — usually your Home folder unless you navigated elsewhere.

⸻

💡 Optional Tips

🧭 Change Download Folder:

If you want to save to your Downloads folder:

cd ~/Downloads
yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID

📝 Rename File Automatically:

yt-dlp -x --audio-format mp3 -o "%(title)s.%(ext)s" https://www.youtube.com/watch?v=VIDEO_ID

🎵 Download Best Quality:

yt-dlp -x --audio-format mp3 --audio-quality 0 https://www.youtube.com/watch?v=VIDEO_ID

📂 Download a Playlist:

yt-dlp -x --audio-format mp3 https://www.youtube.com/playlist?list=YOUR_PLAYLIST_ID

⸻
