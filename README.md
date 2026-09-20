# Tactilix Technologies — Website Page

A single-file, responsive marketing page for **Tactilix Technologies**, an agri-tech startup building offline-first AI and IoT tools for agriculture, starting with **Agricure AI**.

The layout follows the Aeline Webflow template (blue hero with a strip of cards, rounded stat cards, lime accent), rebuilt as plain HTML and CSS with no build step.

Live site: https://tactilixtechnologies.com

---

## What's inside

| Section | Anchor | Notes |
|---|---|---|
| Hero | `#home` | Blue gradient hero, navigation, headline, call-to-action, strip of sample UI cards |
| About us | `#about` | Statement with inline icons, four stat cards, technology strip |
| Products | `#agriculture-ai` | Agricure AI: soil sensors, on-device AI, AgriDoctor, GSM and LoRa |
| Team | `#team` | Sunil Dongare, Sudarshan Dongare, Kartik Wakchaure |
| Contact | `#contact` | Call, email and website buttons, phone and email cards |

## Project structure

```
tactilix-website/
├── index.html   # the whole site: markup, CSS, logos and photos (embedded)
├── README.md
└── .gitignore
```

Everything is embedded in `index.html`: styles, SVG artwork, the Tactilix logo variants and the team portraits (as base64 images). Only the Google Fonts (**Inter Tight** and **JetBrains Mono**) load from the internet; if they are blocked, the page falls back to system fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

**GitHub Pages**
1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Your site appears at `https://<username>.github.io/<repository>/`.

**Netlify / Vercel / any static host**
Upload the folder (or connect the repository). There is no build command and the publish directory is the repository root.

**cPanel / shared hosting**
Upload `index.html` to the folder you want to serve, for example `public_html/` or `public_html/new/`.

## Editing guide

**Text and links**
Search `index.html` for the section comments (`HERO`, `ABOUT`, `PRODUCTS`, `TEAM`, `CONTACT`) and edit the text in place.

**Contact details**
Phone numbers and the email address appear in the `contact` section as `tel:` and `mailto:` links, in the "Call us" and "Email us" buttons and in the contact cards. Update every occurrence. Search for `tel:` and `mailto:`.

**Colours and theme**
Colours are CSS variables at the top of the `<style>` block (`--lime`, `--blue-deep`, `--blue-mid`, `--blue-soft`, `--ink`, `--card`, and so on). Dark mode follows the visitor's system setting (`prefers-color-scheme`) and can be forced with `data-theme="dark"` or `data-theme="light"` on the `<html>` element.

**Team members**
Each person is an `<article class="member …">` inside the `#team` section.
- Add a person by copying an existing card and changing the name and role.
- Photo cards use `<img class="photo">`. Replace the `src` with a file path such as `assets/name.jpg` to keep the HTML smaller.
- Cards without a photo show a large monogram (`.portrait`) on a colour or leaf background. Replace it with an `<img class="photo">` and a `<div class="shade">` to match the others.
- Use square images (about 800 × 800) for the best crop.

**Logo**
The navigation uses a white version of the logo (for the blue hero). The footer has two versions that switch automatically between light and dark mode (`.logo-light` and `.logo-dark`).

**Sample data**
The values shown in the hero cards (for example soil moisture and "Leaf spot: Low risk") are illustrative placeholders, marked "Sample" on the page. Replace them with real product data, or keep the "Sample" label.

## Responsive behaviour

Breakpoints are at 1000px (tablet), 900px (the hero card strip becomes a swipeable row) and 640px (single column). The team cards stack on phones.

## Accessibility

- Semantic landmarks and heading order
- Keyboard focus outlines on all links and buttons
- Decorative artwork is hidden from screen readers
- Respects reduced-motion settings

## Known placeholders

- Sunil Dongare's card still uses a placeholder (green background with "SUN") until a portrait is added.
- The contact section lists phone and email only; there is no contact form because this is a static page. To collect enquiries, connect a form service such as Formspree or Netlify Forms.

## Credits

Layout inspired by the Aeline template for Webflow. Fonts: Inter Tight and JetBrains Mono via Google Fonts.

© 2026 Tactilix Technologies. All rights reserved.
