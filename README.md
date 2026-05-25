# StegoCode — PNG That Runs Code

Python code hidden inside a PNG image. Download a file that **appears as `code.png`** (Windows hides the `.py` extension by default). Double-click it → the image opens + your code runs silently in the background.

## 🔗 Live Demo

👉 **[Open the tool](https://mystry112000.github.io/py-code-to-png)**

## Why It Shows as `.png`

On Windows, "Hide extensions for known file types" is **enabled by default**. A file named `code.png.py` displays as `code.png` — so it looks like a normal image. When you double-click it, Python executes it instead.

## How It Works

1. **Paste** your Python code + **Upload** any PNG
2. Click **Generate** → downloads `code.png.py` (shows as `code.png`)
3. **Double-click the file** → the image opens in your default viewer
4. Your code runs **silently in a background thread** (doesn't block the image)

## Extract the Original .py

If you need the raw `.py` back, just rename `code.png` → `code.png.py` on Windows, or use `python code.png` on any OS.

## Tech

- Pure client-side JavaScript (no server)
- [FileSaver.js](https://github.com/eligrey/FileSaver.js) for download

## Local

Open `index.html` in any browser. No installation needed.
