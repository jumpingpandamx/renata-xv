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

## Guest photos ("Comparte tus fotos")
Guests upload photos from their phones, with no account needed, and everyone sees them appear in a live
gallery and slideshow. Photos are stored in Cloudinary (free plan).

Setup (about 5 minutes):
1. Create a free account at https://cloudinary.com.
2. Copy the **Cloud name** shown on the dashboard.
3. Settings → Upload → Upload presets → **Add upload preset**:
   - Signing mode: **Unsigned**
   - Folder: `renata-xv` (optional, keeps things tidy)
   - Allowed formats: `jpg,jpeg,png,heic,heif,webp` (optional)
   - Save, and copy the preset **name**.
4. Settings → Security → **Restricted media types**: *uncheck* "Resource list" (the live gallery needs it).
5. In `index.html`, fill in `CLOUD_NAME` and `UPLOAD_PRESET`, then commit.

Until both are filled in, the section shows "Muy pronto" and nothing can be uploaded.

Links:
- `https://renata15.com/#fotos`: skips the envelope and opens the photo section. The QR code in
  `assets/qr-fotos.svg` points here (print it for the tables).
- `https://renata15.com/#proyeccion`: full-screen slideshow for a TV or projector at the venue, with the
  QR in the corner. New photos jump to the front as they arrive (checked every ~12 s). Click ⛶ for full screen.

Removing a photo: delete it in Cloudinary's Media Library. It disappears from the site within about a minute.
To download everything after the party: Media Library → select all → Download.

## Photo gallery (optional)
Add up to four photos named `assets/foto1.jpg` ... `assets/foto4.jpg`. The "Mis momentos" section appears automatically when at least one exists, and stays hidden otherwise.
