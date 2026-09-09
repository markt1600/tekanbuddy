# Tekan Buddy — placeholder website

A single-page "coming soon" site for **Tekan Buddy**, an iPhone running app.

- `index.html` — the whole site. No build step, no dependencies.

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). For GitHub Pages,
serve from the repository root on the branch you publish.

## To do before launch

- Wire the "Notify me" form to a mailing-list provider (see the comment in `index.html`).
- Replace the placeholder contact email in the footer.
- Add the real App Store link once the app is approved.
