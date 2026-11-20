# GlucoTrack PWA

A mobile-first blood glucose diary that can be installed on iPhone from Safari.

## Features
- Manual glucose entries with date/time, reading category and notes
- History with delete
- 7/30/90-day trend chart and average/minimum/maximum
- CSV export and JSON backup/restore
- Local browser storage (IndexedDB)
- Offline app shell via service worker

## Run locally
For a quick preview, use a local web server (not opening index.html as a file):
`python3 -m http.server 8000`
Then open `http://localhost:8000`.

## Install on iPhone
1. Host the contents of this folder on an HTTPS website (GitHub Pages, Netlify, or your own HTTPS host).
2. Open the HTTPS URL in Safari on your iPhone.
3. Tap Share -> Add to Home Screen -> Add.
4. Launch GlucoTrack from the Home Screen.

## Data and sync limitations
This version stores entries in IndexedDB on the device/browser. It does not include automatic iCloud or cross-device synchronisation. Use Download backup and Restore backup to move records manually. A hosted PWA needs a separately configured secure sync backend for automatic multi-device sync. iCloud Drive can be used to store the exported JSON backup manually.

## Medical note
This is a record-keeping tool, not a medical device. It does not provide diagnosis, treatment recommendations, or validated glucose alerts. Do not change medication based on the app.

## Category trend charts update

The dashboard now includes independent glucose trend charts for all six reading types: Fasting, Before meal, 1 hour after meal, 2 hours after meal, Bedtime, and Random. Each chart displays only its own category, with average, lowest, highest, and count statistics. The shared date filter supports 7 days, 30 days, 90 days, and All time. Existing records, history, CSV export, backup/restore, and local IndexedDB storage are retained.
