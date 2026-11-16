---
layout: post
title: Combine MP3 files
date: 2026-05-02 10:00:00 -0000
category: FFMPEG
---
## Can I use ffmpeg to combine .mp3 files into one file?

Yes! FFmpeg can combine multiple `.mp3` files into a single MP3 file without re-encoding them (which preserves the original audio quality).

Since you're using a MacBook Air, you can do this directly from Terminal.

### Method 1: Combine MP3 files without re-encoding (recommended)

This is the fastest method and preserves the original audio quality.

Step 1. Put all the MP3 files you want to combine into one folder.

Step 2. Open Terminal and navigate to that folder. For example:

```bash
cd ~/Downloads/MP3Files
```

Step 3. Create a text file listing the MP3 files in the order you want them combined:

```bash
printf "file '%s'\n" *.mp3 > filelist.txt
```

This creates a list using alphabetical filename order.

Step 4. Run FFmpeg:

```bash
ffmpeg -f concat -safe 0 -i filelist.txt -c copy combined.mp3
```

That's it! You'll have one file named `combined.mp3`.

### Method 2: Combine MP3 files with re-encoding

If the MP3 files have different audio characteristics (sample rates, channel configurations, etc.), you can re-encode them to ensure consistency:

```bash
ffmpeg -f concat -safe 0 -i filelist.txt -acodec libmp3lame -b:a 192k combined.mp3
```

This creates a 192 kbps MP3.

### A few useful tips

* Order matters: FFmpeg combines files in the order listed in `filelist.txt`.

* No quality loss: Method 1 copies the compressed audio directly without re-encoding.

* Original files remain untouched: FFmpeg creates a new file.

* Metadata: The resulting file won't necessarily preserve individual track titles or metadata.

My recommendation: Start with Method 1. It's faster and avoids unnecessary quality loss.

I can also give you a single Terminal command that combines every MP3 in a folder alphabetically without requiring you to create a separate text file.