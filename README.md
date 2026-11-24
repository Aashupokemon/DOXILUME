# DOXILUME — landing page

Static marketing page for **DOXILUME**, the offline PDF compressor and page resizer
for Android, plus the signed release APK it offers for download.

Live: <https://aashupokemon.github.io/DOXILUME/>

## What is in here

| Path | Purpose |
| --- | --- |
| `index.html`, `styles.css` | The page (plain HTML/CSS, no build step) |
| `privacy.html` | Privacy policy (linked from the footer, FAQ and the app) |
| `favicon.svg` | Doxilume mark used as the tab icon |
| `shots/` | App screenshots and the launcher icon shown on the page |
| `downloads/DOXILUME-0.1.0.apk` | Signed release build (Android 8.0+, ~15 MB) |
| `.nojekyll` | Serve the folder as-is on GitHub Pages |

The Android application source is not part of this repository; this repo only
publishes the page and the built APK.

## Preview locally

```bash
cd site
python -m http.server 8089 --bind 127.0.0.1
# open http://127.0.0.1:8089/index.html
```

## Updating the download

1. Build the release APK from the app project (signed with the same key as the
   previous release, or Android will refuse the update).
2. Replace `downloads/DOXILUME-0.1.0.apk`, renaming it if the version changed.
3. Update the three `downloads/…` links and the size line in `index.html`.
4. Push to `main` and `gh-pages`; GitHub Pages publishes within a minute.

The app makes no network requests: it declares no `INTERNET` permission.
