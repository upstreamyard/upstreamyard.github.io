# upstreamyard.github.io

The upstreamyard project website: the open-source container images and Helm charts, how they are built, signed and tested, and where to send questions and feedback.

Static pages with no build step, no cookies and no external requests:

- `index.html`: the homepage (inline CSS, a few lines of JavaScript for the copy buttons, light and dark theme)
- `imprint.html`, `privacy.html`, `terms.html`: imprint (aviso legal), privacy policy (including the cookie section) and terms of use, styled by `assets/legal.css`
- `assets/cookie-notice.js`: the cookie notice, shown once per browser; it stores one `localStorage` entry and no cookies (documented in `privacy.html#cookies`)
- `assets/logo.png`: the upstreamyard logo (same file as `logo.png` in `upstreamyard/helm-charts`)
- `.nojekyll`: serve the files as they are, without Jekyll

Links that leave the homepage (external sites and the legal pages) open in a new tab with `rel="noopener"`; in-page anchors and `mailto:` links don't.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Publishing

GitHub Pages deploys the `main` branch (`/` root) to https://upstreamyard.github.io/ on every push. The Helm repository at https://upstreamyard.github.io/helm-charts is unaffected, because project sites are served under their repository name.

## Keeping it current

The catalog is written by hand. When an image or chart is added to `upstreamyard/helm-charts`, add a card or chip in `index.html` and update the counts in the fact strip.
