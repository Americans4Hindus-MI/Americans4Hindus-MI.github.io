# A4H Bhajan Clubbing 2026 — Event Presentations

This folder hosts the public event presentation viewer for A4H Bhajan Clubbing 2026.

## Website

https://americans4hindus-mi.github.io/bhajanclubbing/presentations/

## Files

- `index.html` — live entry point for the presentations page.
- `presentations-v1.html` — versioned copy of the original page for reference and rollback.
- `README.md` — documentation and maintenance instructions.

## How the presentation list works

The viewer loads presentation titles, descriptions, ordering, visibility, and video URLs from the **Event Presentations** tab of the **A4H Bhajan Clubbing 2026 – Attendee Feedback** Google Sheet through a separate, read-only Google Apps Script web app.

API endpoint:
https://script.google.com/macros/s/AKfycbzZDXNjZfe9HDlRMXofTcKOw0WnniDRO1fAFpIHglVOwM-zpi1FVdr7ZeTgPToac2ca/exec

The sheet columns are:

| Column | Purpose |
| --- | --- |
| A — Order | Playback/display sequence (0, 1, 2, …) |
| B — Presentation Title | Public title |
| C — Google Drive Video Link | Shareable link to the MP4 |
| D — Display | `YES` to show; `NO` to hide |
| E — Description | Short public description |

Only rows with `Display = YES` and a nonempty video link are included. Changes to the Sheet should appear on a newly loaded viewer page without modifying GitHub files.

## Adding or replacing a video

1. Upload the MP4 to the A4H Google Drive presentations folder.
2. Set its sharing permission to **Anyone with the link → Viewer** if the public should be able to watch it.
3. Copy the MP4's sharing link.
4. Enter or replace the link in column C of the **Event Presentations** tab.
5. Confirm the title, order, description, and `YES` status; refresh the website and test playback.

The source spreadsheet contains private attendee information on other tabs. **Do not publish the spreadsheet itself** or add private fields to the public API.

## Publishing and updates

In the `bhajanclubbing` GitHub repository, place these files in the `presentations/` folder. GitHub Pages serves `presentations/index.html` at the website URL above.

When updating the design, save a new versioned HTML copy (for example, `presentations-v2.html`) and update `index.html` with the approved version. Test the page before linking it from the survey Thank You screen.

## Related resources

- Event photos: https://photos.app.goo.gl/HSu7SEh6K1HoEKEdA
- Sing-along lyrics: https://americans4hindus-mi.github.io/bhajanclubbing/lyrics/
- Event survey: https://americans4hindus-mi.github.io/bhajanclubbing/survey/

Maintained for A4H Michigan.
