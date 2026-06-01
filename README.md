# aidenchoi.com — site files

A multi-page portfolio. Plain HTML/CSS/JS on GitHub Pages, with a private
Studio (admin) backed by Firebase for uploading photos.

## Pages

- **index.html** — landing: hero, About, brief intros to Photography & Creations, contact.
- **photography.html** — full gallery (Seoul / Vancouver filters, lightbox). Live photos
  uploaded in the Studio appear here automatically.
- **creations.html** — ThinkTwin, AC Studios, Booze & Foods, and Prints.
- **admin.html** — the Studio. Open at **<https://aidenchoi.com/admin.html>**. Sign in,
  then upload one or many photos at once.
- **gallery.html** — redirect to photography.html (keeps old links working).

## Images (live in the repo root, shared across pages)

logo-white.png, hero.jpg, about-1.jpg, about-2.jpg, thinktwin.png, signature.png,
and the gallery seeds p1.jpg … p8.jpg. Filenames are referenced in the HTML, so
**keep the names exactly** when uploading.

## Updating the site (from your phone)

1. GitHub repo → **Add file → Upload files**.
1. Drag in the changed file(s). Keep filenames identical.
1. **Commit changes**. Live in ~1 minute at aidenchoi.com.

## The Studio (bulk upload + AI titles)

- Pick **one or many** photos. Each lands as a card with an AI-suggested title,
  location, year, and a “for sale as print” toggle. Edit anything, then **Upload all**.
- AI titles aim for simple, clean, gallery-style names (place/subject based) — not
  flowery “AI-sounding” ones. Re-name any card with the ✨ button, or just type your own.
- Uploaded photos go live on photography.html instantly; “for sale” ones also appear
  under Prints on creations.html.

## Config (already set)

- **firebase-config.js** holds the public Firebase web config.
- Studio model: gemini-3.5-flash · Firebase JS SDK 12.14.0.
- Firestore + Storage rules: public read, authenticated write.

## YouTube counts

**youtube.json** drives the Booze & Foods numbers on creations.html.
Edit it by hand, or automate with youtube-counter-workflow.yml.