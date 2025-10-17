# Hello World + Captcha OCR

## Overview
This is a minimal, client‑side web app that:
- Displays “hello world.”
- Shows a captcha image from a URL passed via the `?url=` query parameter.
- Displays the passed captcha URL on the page.
- Attempts to extract and display the captcha text within approximately 15 seconds using on-device OCR (Tesseract.js). A quick filename-based guess is shown immediately while OCR is running.

The project is self-contained: just open `index.html` in a browser.

License: MIT

## Setup
No build steps are required.
1. Download or clone this repository.
2. Open `index.html` in any modern browser with JavaScript enabled and network access (for the Tesseract.js CDN).

## Usage
- Basic: open `index.html` to see “hello world.”
- Captcha OCR:
  - Provide an image URL via the `url` query parameter:
    - Example: `index.html?url=https%3A%2F%2Fdummyimage.com%2F220x80%2Fffffff%2F000000.png%26text%3DAB12CD`
  - The page will:
    - Show the captcha URL you passed.
    - Fetch and display the image.
    - Immediately display a quick filename-based guess (when possible).
    - Run OCR and update the solved text result, aiming to complete within ~15 seconds.
  - Tip: Use clear, high-contrast images (e.g., dummyimage.com text images) for best OCR results.

Notes:
- If the source image lacks permissive CORS headers, the app automatically retries via a public CORS proxy for fetching.
- OCR happens locally in the browser via Tesseract.js (loaded from a CDN).

## License
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.