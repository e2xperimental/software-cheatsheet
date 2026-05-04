---
layout: post
title: Save text as mp3
date: 2026-05-03
category: Macbook
---

## Option 1: Use macOS built-in TTS (cleanest MP3)
1. Copy the page text (use Reader mode in Chrome or Edge to simplify it).
2. Open TextEdit (or any text editor).
3. In TextEdit, paste copied text using Edit > Paste and Match style
4. Remove advertisements.
5. Use macOS’s built-in speech:
  - Go to Edit → Speech → Start Speaking

### To save as MP3

#### 1. Open the **Automator** app.

#### 2. Create a Quick Action*
1. File menu > New > Select **Quick Action**.
2. Click **Choose**.
At the top, set:
3. “Workflow receives current” → **text**
4. “in” → **any application**

#### 3. Add “Text to Audio File”
1. With **Library** selected, search for **Text to Audio File**
2. Drag Drag “Text to Audio File” into the big empty area on the right or Double click on **Text to Audio File**

#### 4. Configure it
Inside the action
1. System Voice: Pick one. Try Alex, Daniel or Samantha (default).
  - Save As: MP3
  - Where: Downloads
- Run it on your copied text
  
* Quick Actions are workflows that may be added to Finder, Touch Bar, and the Services menu. You can manage Quick Actions in System Settings.

This uses macOS voices but gives you a direct MP3 export.
