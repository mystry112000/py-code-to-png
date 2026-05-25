# Py Code to PNG

Convert your Python code into a beautiful, syntax-highlighted PNG image with an optional background image.

## Features

- Syntax highlighting with multiple themes (Atom One Dark, GitHub Dark, Monokai, VS Code, Dracula, Nord)
- Upload any image as background for your code screenshot
- Adjustable font size and background opacity
- Live preview
- Downloads a ZIP containing the PNG image + the original `.py` file
- Works entirely in your browser — no server needed

## Live Demo

👉 **[Open the tool](https://mystry112000.github.io/py-code-to-png)**

## Usage

1. Paste your Python code in the editor
2. (Optional) Upload a background image
3. Choose your style, font size, and opacity
4. Click **Generate & Download ZIP**

## Local Development

Just open `index.html` in any modern browser.

## Tech

- [highlight.js](https://highlightjs.org/) — syntax highlighting
- [JSZip](https://stuk.github.io/jszip/) — ZIP creation
- [FileSaver.js](https://github.com/eligrey/FileSaver.js) — file download
