---
layout: post
title: Save YouTube videos as mp3
date: 2026-05-03
category: Macbook
---

Online converters often have limits (like a 30-minute cutoff I ran into) so switching to a reliable open-source tool like [yt-dlp](https://github.com/yt-dlp/yt-dlp) gives you full control, supports long videos, and avoids shady ads or broken downloads.

⸻

✅ What You’ll Use: yt-dlp

yt-dlp is a powerful command-line tool, forked from youtube-dl, and it’s actively maintained. It supports downloading just the audio from long YouTube videos, in MP3, M4A, or WebM formats.

⸻

🛠️ Step-by-Step: Install and Use yt-dlp on Windows

1. Download yt-dlp

Go to:
👉 ⁠https://github.com/yt-dlp/yt-dlp/releases

Scroll down to “Assets” and download:

yt-dlp.exe

Save it somewhere easy, like your Downloads or C:\yt-dlp

2. Open Command Prompt

* Press Win + R, type cmd, press Enter.
* Navigate to the folder where you saved yt-dlp.exe, e.g.:

cd C:\yt-dlp

3. Download Audio from YouTube

Replace [URL] with the link to the YouTube video.

To get high-quality audio in MP3, run:

yt-dlp.exe -x --audio-format mp3 [URL]

Example:

yt-dlp.exe -x --audio-format mp3 https://www.youtube.com/watch?v=dQw4w9WgXcQ

This will:

* Download only the audio track
* Convert it to MP3
* Save it in the current folder

You can also use:

--audio-quality 0

to get the best possible bitrate.

⸻

💡 Pro Tips

* To specify a download folder, add:

-o "C:\Users\YourName\Music\%(title)s.%(ext)s"

* To download a whole playlist:

yt-dlp.exe -x --audio-format mp3 https://www.youtube.com/playlist?list=...

* To avoid YouTube ads and skips:

--no-playlist --no-part

⸻

❤️ Bonus: Save the Command as a Script

If you’re doing this often:

1. Open Notepad.
2. Paste your yt-dlp command.
3. Save it as download_audio.bat on your desktop.
4. Double-click it anytime to start a download!
