# Disaster Science — Website

A complete, ready-to-publish website for Disaster Science. Five self-contained
pages, no build step, no dependencies to install. Open any file in a browser and
it just works.

---

## What's in this folder

| File | Page |
|------|------|
| `index.html` | Home — hero with a live 3D globe, key statistics, approach, the two service areas, the risk-management cycle, research, and contact call-to-action. Includes a language switcher (English · Русский · Español · 中文). |
| `disaster-risk-management.html` | Disaster Risk Management — the four service offerings. |
| `nature-based-solutions.html` | Nature-Based Solutions — approach and capabilities. |
| `research.html` | Research & Partnerships. |
| `contact.html` | Contact form (opens the visitor's email app addressed to contact@disastersci.com) plus direct contact details. |

Every page is **one self-contained HTML file** — the styling is built in, so
there is no separate CSS file to keep in sync and nothing can break from a
missing stylesheet. Just keep the five files together in the same folder.

---

## Preview it

Double-click `index.html` (or drag it into a browser). The navigation links move
between the pages. An internet connection is needed only for the 3D globe on the
home page (it loads a small graphics library from a public CDN); everything else
works fully offline.

---

## Edit it with Claude (recommended for changes)

You don't need to know how to code to change this site. In your own Claude:

1. Start a new project (or a new chat) and **upload these five files** (and this
   README).
2. Tell Claude what you'd like changed, in plain language. For example:
   - *"Update the four service descriptions on the Disaster Risk Management page to this new text…"*
   - *"Change the contact email everywhere to hello@disastersci.com."*
   - *"Add a fifth service card to the Nature page."*
   - *"Replace the blue visual panels on the home page with these photos I'm attaching."*
3. Claude edits the files and gives them back to you. Download and replace.

**Good things to know before editing:**

- **Text on the home page** lives in a translations block near the bottom of
  `index.html` (a section labelled `I18N` with `en`, `ru`, `es`, `zh`). Each
  language has the same set of labels — update all four so the switcher stays
  consistent, or ask Claude to translate a change into the other languages for you.
- **Text on the other four pages** is written directly in the visible HTML —
  easy to find and change.
- **The decorative visuals** in the home-page panels are hand-drawn SVG graphics
  (so they never break and need no image files). To use real photos instead,
  drop an image into the folder and ask Claude to place it in a given panel.
- **The contact form** has no server behind it — submitting simply opens the
  visitor's email app with the message pre-filled to contact@disastersci.com.
  That address is set in `contact.html`.
- **Colors and fonts** are defined once at the top of each file's `<style>`
  block (the dark navy background, the blue accent, the type). Change them there.

---

## Publish it

Because the pages are plain static HTML, they can go on almost any host:

- **Any static host** — Netlify, Vercel, Cloudflare Pages, GitHub Pages: drag the
  folder in, done.
- **An existing site builder** — the pages can be embedded or uploaded depending
  on the platform.
- **Your own web hosting** — upload the five files to the public folder; make sure
  `index.html` is the home page.

Keep all five files in the same directory so the links between pages keep working.

---

## Notes

- No analytics, trackers, cookies, or third-party accounts are wired in.
- The only external request is the 3D-globe graphics library on the home page,
  loaded from a public CDN (cdnjs). Remove that one `<script>` tag in
  `index.html` if you'd prefer a fully offline home page (the globe area will
  simply stay dark).
- Links to "Insights" and "About" currently point to disastersci.com — repoint
  or rebuild those as native pages whenever you're ready.
