# SG Atom Uhr — notes for Claude

- **Bump the app version on every change to `index.html`.** Set `<meta name="app-ver" content="YYYYMMDDHHMMSS">` (line ~5) to the current **UTC** time before committing (the app converts it to the phone's local time for display; Berlin time would show an hour late). Open copies of the app check this stamp when opened or brought to the front and reload onto the new version; if it isn't bumped, phones keep showing the old version (GitHub Pages also caches pages for up to 10 minutes).
- Changes are pushed straight to `main` (GitHub Pages serves from it).
- Text recognition (Tesseract.js 5.1.1: main script, worker, SIMD + non-SIMD LSTM cores, English 4.0.0_best_int data) is self-hosted in `ocr/`. The Content Security Policy only allows this site, the three time services and api.bigdatacloud.net — keep it that way; don't add CDN scripts.
