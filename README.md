# StegoCode — Hide Python Code Inside PNG Images

A web tool that uses **steganography** to invisibly hide Python source code inside a PNG image file. The image looks completely normal, but the code is embedded after the PNG's `IEND` chunk — a classic polyglot technique.

## 🔗 Live Demo

👉 **[Open the tool](https://mystry112000.github.io/py-code-to-png)**

## How It Works

1. **Paste** your Python code
2. **Upload** any PNG image (the carrier)
3. Click **Embed Code & Download ZIP**
4. The code is appended after the PNG's IEND marker — invisible to image viewers
5. Download a ZIP containing:
   - `stego.png` — the carrier image with code hidden inside (looks identical)
   - `code.py` — the original source file
   - `extract.py` — a script to retrieve the hidden code

## Extract the Hidden Code

```bash
python extract.py stego.png
```

Or manually:
```bash
# Find ---PYCODE--- marker in the PNG and extract everything after it
python -c "import sys; d=open('stego.png','rb').read(); i=d.find(b'---PYCODE---'); exec(d[i+len(b'---PYCODE---')+4:])"
```

## Technical Details

This appends data after the PNG's `IEND` chunk. PNG specifications allow extra data after `IEND` — compliant decoders ignore it. The format is:

```
[original PNG bytes] ---PYCODE--- [4-byte code length] [Python source]
```

The image is **100% visually identical** to the original — zero pixel modification.

## Tech

- Pure client-side JavaScript (no server)
- [JSZip](https://stuk.github.io/jszip/) for ZIP creation
- [FileSaver.js](https://github.com/eligrey/FileSaver.js) for download

## Local

Open `index.html` in any modern browser. No installation needed.
