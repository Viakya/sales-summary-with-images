# CSV Viewer + Images (Single-File Web App)

## Project Overview
This is a minimal, single-page web application that:
- Loads `data.csv` from the same folder.
- Displays its contents as a table.
- Shows two images: `photo1.png` and `photo2.png`.

Everything runs in your browser with no build step and no external dependencies. The main runnable file is `index.html`.

## Setup
Place these files in the same directory:
- `index.html` (this app)
- `data.csv` (provided)
- `photo1.png` (provided)
- `photo2.png` (provided)

Because browsers often restrict `fetch()` when opening files directly from disk, it’s best to run a simple local web server.

Common options:
- Python 3: `python -m http.server 8000`
- Node.js (http-server): `npx http-server -p 8000`
- VS Code: Install “Live Server” extension and click “Go Live”

Then open:
- http://localhost:8000/index.html

If you do open `index.html` directly (file://), the page will still attempt to load, but CSV loading may be blocked by your browser. The page shows a tip if it detects file://.

## Usage
- Start your local server and open `index.html`.
- The app will:
  - Fetch `data.csv`
  - Parse it (including quoted cells and commas within quotes)
  - Render a clean HTML table
  - Display `photo1.png` and `photo2.png`
- To update the data, edit `data.csv` and refresh the page.

CSV format notes:
- The first row is treated as the header.
- Basic CSV conventions are supported, including quoted fields and escaped quotes with `""`.

## License
MIT License

Copyright (c) 2025 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.