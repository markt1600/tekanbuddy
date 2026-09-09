# Run Buddy — website

A single-page site for **Run Buddy**, an iPhone app with an AI running coach that
talks to you while you run. Currently in beta on TestFlight.

- `index.html` — the whole site. No build step, no dependencies.
- `icon.png` — the app icon, used as favicon and in the header.
- `og-image.jpg` — the 1200x630 link-preview card shown when the URL is shared on WhatsApp, iMessage, Telegram, Slack or X. Referenced by absolute URL (`https://tekanbuddy.com/og-image.jpg`) in the `og:image` tags.
- `media/run-buddy-promo-web.mp4` — the promo video, re-encoded for the web (H.264, 960x960, ~5 MB).
- `media/run-buddy-promo-poster.jpg` — poster frame shown before the video plays.

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). For GitHub Pages,
serve from the repository root on the branch you publish.

## Updating the promo video

Re-encode a new master with ffmpeg so the page stays light, then replace both files in `media/`:

```sh
ffmpeg -i promo-master.mp4 -c:v libx264 -preset slow -crf 23 -pix_fmt yuv420p -movflags +faststart -c:a aac -b:a 128k media/run-buddy-promo-web.mp4
ffmpeg -ss 1.5 -i promo-master.mp4 -frames:v 1 -q:v 3 media/run-buddy-promo-poster.jpg
```

## To do

- Replace the placeholder contact email (`hello@tekanbuddy.com`) in the footer and feedback button.
- Swap the TestFlight link for the App Store link once the app is released.
