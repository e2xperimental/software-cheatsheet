---
layout: post
title: Save YouTube videos as mp3
date: 2026-07-17
category: Macbook
---


✅ Step 1: Download Audio from YouTube

In Terminal, paste this command, replacing the URL with your video link:

yt-dlp -x --audio-format mp3 "https://www.youtube.com/watch?v=VIDEO_ID"

This tells yt-dlp to:

* -x: extract audio only
* --audio-format mp3: convert to MP3

🗂 The MP3 file will be saved in your current Terminal folder — usually your Home folder unless you navigated elsewhere.

⸻

💡 Optional Tips

🧭 Change Download Folder:

If you want to save to your Downloads folder:

cd ~/Downloads
yt-dlp -x --audio-format mp3 "https://www.youtube.com/watch?v=VIDEO_ID"

📝 Rename File Automatically:

yt-dlp -x --audio-format mp3 -o "%(title)s.%(ext)s" "https://www.youtube.com/watch?v=VIDEO_ID"

🎵 Download Best Quality:

yt-dlp -x --audio-format mp3 --audio-quality 0 "https://www.youtube.com/watch?v=VIDEO_ID"

📂 Download a Playlist:

yt-dlp -x --audio-format mp3 "https://www.youtube.com/playlist?list=YOUR_PLAYLIST_ID"

⸻

💡 Clean Up the .webm After Conversion

If you’d like yt-dlp to delete the .webm file after it makes the .mp3, just add:

--audio-quality 0 --keep-video=false

Your full command becomes:

yt-dlp -x --audio-format mp3 --audio-quality 0 --keep-video=false "https://www.youtube.com/watch?v=76dmpJ0FNjs"

⸻
