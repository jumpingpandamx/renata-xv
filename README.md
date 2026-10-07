# Invitación XV · Renata Muñoz

Static site, no build step. Works on GitHub Pages.

## Files
- `index.html`: the whole invitation (HTML, CSS and JS in one file)
- `assets/cancion.mp3`: **add the song here** (the "Play me" button uses it)

## Publish on GitHub Pages
1. Upload the contents of this folder to the repo root.
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The link will be `https://<user>.github.io/<repo>/`.

## RSVP
GitHub Pages can't store form answers. To receive them:
1. Create a free form at https://formspree.io (or similar).
2. Paste its endpoint into `RSVP_ENDPOINT` near the bottom of `index.html`.

If it's left empty, guests only see the thank-you message.

## Edit
- Event date/time: `EVENT_DATE` in `index.html`.
- All text is plain HTML in `index.html`.
