# Run Buddy — website

A single-page site for **Run Buddy**, an iPhone app with an AI running coach that
talks to you while you run. Coming soon to iPhone.

- `index.html` — the whole site. No build step, no dependencies.
- `icon.png` — the app icon, used as favicon and in the header.

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). For GitHub Pages,
serve from the repository root on the branch you publish.

## To do

- Replace the placeholder contact email (`hello@tekanbuddy.com`) in the footer and feedback button.
- Wire the "Tell me when it's out" form to a mailing-list provider (see the comment in `index.html`).
- Add the App Store link once the app is released.
