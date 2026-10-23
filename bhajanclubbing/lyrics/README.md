# A4H Bhajan Clubbing: Sing-Along Lyrics Page

Live address: https://americans4hindus-mi.github.io/bhajanclubbing/lyrics/
(The QR code and the "Sing-Along Lyrics" button on the event page point here.)

## What it is
One self-contained file (index.html). No other files are needed.
- Songs are listed in singing order, as in the Oct 23, 2026 performance script.
- Tap a song to open it. Tap it again to close it. Tap "Next song" to move on.
- "Find a song" is a small search for anyone who needs it.
- Display settings: text size (A- / A+), Roman text under the Devanagari, singer names, light/dark theme.

## Reusing it for the next event
1. The song data sits inside index.html in a block that begins
   <script type="application/json" id="data">
   Each song has: title, group, alias (search words) and items (lyric lines).
2. To change the order, move songs around in that block. The numbers follow the order automatically.
3. Update the page title, the "Welcome from" card and the footer link as needed.
4. Keep the file at bhajanclubbing/lyrics/index.html so the QR code and links keep working.

## Notes
- Roman spellings are generated from the Devanagari and may vary slightly.
- Do not rename this folder. The printed QR code depends on the address.
