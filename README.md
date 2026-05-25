# StegoCode — Polyglot PNG + Python

Embed Python code inside a PNG image. Download a **self-executing `.py` file** — double-click it and your code runs while the image opens automatically.

## 🔗 Live Demo

👉 **[Open the tool](https://mystry112000.github.io/py-code-to-png)**

## How It Works

1. **Paste** your Python code
2. **Upload** any PNG image
3. Click **Generate & Download .py**
4. A `runnable.py` file downloads — it contains the PNG image (base64-encoded) + your code
5. **Double-click `runnable.py`** → the image opens in your viewer AND your code executes

## What's Inside the .py

The generated file:
- Embeds the PNG image as a base64 string
- On execution: writes the PNG to a temp file and opens it
- Then runs your Python code via `exec()`

## Tech

- Pure client-side JavaScript (no server)
- [FileSaver.js](https://github.com/eligrey/FileSaver.js) for download

## Local

Open `index.html` in any browser. No installation needed.
