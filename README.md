# Smit Social Site

Static QR redirect: one HTML page, no server. The redirect target is in the URL hash.

## Flow

1. **Scan / open link** — QR or link looks like `https://yoursite.com/#https://instagram.com/you`. When opened, the page immediately redirects to the URL in the hash (e.g. Instagram).
2. **Edit the link** — Open the site without a hash (e.g. `https://yoursite.com/`). Enter the new social URL and click “Get my link”. Use the generated URL for your QR or sharing.

There is no login; the “edit” is just building a new URL with a different hash. Anyone with the link can see the target (it’s in the URL). To change where the QR goes, generate a new link and point the QR to it.

## Setup

Host the files on any static host (GitHub Pages, Netlify, Vercel, or plain web server). No build step. Serve `index.html` and `index.css` at the root (or in a folder; the generated link will use the current origin and path).

## Files

- `index.html` — Redirect logic (hash → redirect) and form to build the share/QR link.
- `index.css` — Styles.
