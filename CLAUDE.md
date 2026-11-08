# SG Atom Uhr — notes for Claude

- **Bump the app version on every change to `index.html`.** Set `<meta name="app-ver" content="YYYYMMDDHHMMSS">` (line ~5) to the current **UTC** time before committing (the app converts it to the phone's local time for display; Berlin time would show an hour late). Open copies of the app check this stamp when opened or brought to the front and reload onto the new version; if it isn't bumped, phones keep showing the old version (GitHub Pages also caches pages for up to 10 minutes).
- Changes are pushed straight to `main` (GitHub Pages serves from it).
