---
layout: post
title: Save YouTube videos
date: 2026-07-17
category: Macbook
---

yt-dlp makes it easy to download a full YouTube video and convert it to MP4 so it plays seamlessly on both Windows and MacBook.

⸻

✅ Basic Command to Download a YouTube Video

yt-dlp "https://www.youtube.com/watch?v=VIDEO_ID"

This will download the best combined audio + video format by default. The result might be a .webm or .mkv file — both playable on modern systems like VLC or QuickTime (with recent macOS updates).

But since you asked specifically for MP4, let’s make that happen.

⸻

🛠️ Command to Download YouTube Video as MP4

yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 --merge-output-format mp4 "https://www.youtube.com/watch?v=VIDEO_ID"

Replace the link with your actual video link, like this:

yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 --merge-output-format mp4 "https://www.youtube.com/watch?v=76dmpJ0FNjs"

🔍 What This Does:

* -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4: tells it to pick the best quality MP4 video + M4A audio.
* --merge-output-format mp4: merges them into a single .mp4 file.
* Compatible with Windows, Mac, iPhone, iPad, etc.

⸻

📂 Optional: Download to a Specific Folder

-o "~/Downloads/%(title)s.%(ext)s"

This puts it in your Downloads folder with the video title as the filename:

yt-dlp -f bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4 --merge-output-format mp4 -o "~/Downloads/%(title)s.%(ext)s" "https://www.youtube.com/watch?v=76dmpJ0FNjs"

⸻

💡 Bonus: If the video doesn’t have MP4 streams

If YouTube doesn’t serve an MP4 stream at your requested quality, yt-dlp will fall back to .webm + .m4a, and still convert it into .mp4 using ffmpeg (which you’ve now installed).

⸻
