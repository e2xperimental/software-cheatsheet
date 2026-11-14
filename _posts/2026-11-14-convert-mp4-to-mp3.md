---
layout: post
title: How do I convert a .mp4 to .mp3 using yt-dlp?
date: 2026-11-14 10:00:00 -0000
category: "Macbook"
---

If you already have `yt-dlp` and `ffmpeg` installed, you can extract the audio from an existing `.mp4` with `yt-dlp`.

### Easiest command

First, go to the folder containing the MP4. If it's in Downloads:

```bash
cd ~/Downloads
```

Then:

```bash
yt-dlp -x --audio-format mp3 "your-video.mp4"
```

For example:

```bash
yt-dlp -x --audio-format mp3 "Bogleheads Conference 2024.mp4"
```

This will create:

```text
Bogleheads Conference 2024.mp3
```

in the same folder.

### Better quality

You can specify the MP3 quality:

```bash
yt-dlp -x --audio-format mp3 --audio-quality 0 "your-video.mp4"
```

`--audio-quality 0` means the best VBR quality available for the MP3 conversion.

### One important distinction

If you're converting a **local MP4**, you don't actually need `yt-dlp`; `ffmpeg` can do it directly:

```bash
ffmpeg -i "your-video.mp4" -vn -c:a libmp3lame -q:a 2 "your-video.mp3"
```

For what you're doing, I'd actually recommend **ffmpeg** for local files. `yt-dlp` is primarily useful when the source is YouTube.

If your MP4 is a **3-hour video**, I can also give you a command that produces a much smaller MP3 optimized for **spoken lectures/interviews**, which could dramatically reduce the file size.
