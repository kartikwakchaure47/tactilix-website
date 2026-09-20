# Tactilix Technologies — website page

Single-file static page (`index.html`) for Tactilix Technologies, built in the Aeline template layout.
Everything (styles, logos, team photos, artwork) is embedded in the file; only Google Fonts load from the internet.

## Deploy with GitHub Pages
1. Push this repository to GitHub.
2. Repository **Settings → Pages**.
3. Source: **Deploy from a branch**, branch **main**, folder **/ (root)**.
4. The site appears at `https://<username>.github.io/<repository>/`.

## Editing
- Text, phone numbers and email are in the `contact` and `team` sections of `index.html`.
- Team photos are embedded as base64 `<img class="photo">` elements inside each `.member` card.
