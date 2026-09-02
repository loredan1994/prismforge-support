# Prism Forge web pages

Three static pages for App Store support and legal disclosure:

- `index.html` — support page (App Store "Support URL", TestFlight feedback pointer)
- `privacy.html` — privacy policy (App Store "Privacy Policy URL", required even for
  apps that collect nothing)
- `terms.html` — terms page linking to Apple's Standard EULA

Published copies:

- Support URL: `https://loredan1994.github.io/prismforge-support/`
- Privacy policy URL: `https://loredan1994.github.io/prismforge-support/privacy.html`

No JavaScript, no analytics, no external resources — the pages keep the same
privacy promise as the app.

The Prism Forge Help Scout alias and exact Cloudflare route are active. These
GitHub Pages URLs were published and verified on 2026-09-03 and remain the live
App Store values. A real inbound/reply test is still required. The optional
vanity URLs are `https://prismforge.calimanu.com/support`, `/privacy`, and
`/terms`; do not push them to App Store Connect before they return the same
checked-in pages over HTTPS.

## Publishing with GitHub Pages (one-time, ~2 minutes)

1. On GitHub: repo **Settings → Pages**.
2. Source: **Deploy from a branch**, branch `main`, folder `/site` is not offered
   directly — either:
   - easiest: keep this folder and add a GitHub Actions Pages workflow, or
   - simplest without Actions: copy `site/` contents to a new public repo named
     `<username>.github.io` (then the URLs are `https://<username>.github.io/` and
     `https://<username>.github.io/privacy.html`), or
   - select branch `main` + folder `/docs` and move these two HTML files into
     `docs/` (they can live alongside the markdown docs).
3. Paste the resulting URLs into App Store Connect:
   - App Information → **Privacy Policy URL** → the `privacy.html` URL
   - App Information → **Support URL** → the `index.html` URL
   - TestFlight → Test Information → **Privacy Policy URL** (external testing)

Any host works — these are plain static files; GitHub Pages is just the free,
zero-maintenance option.

## Before publishing

- Confirm the contact email in both pages (currently `prismforge-support@calimanu.com`).
- Page `<title>`s track the App Store listing name, currently "Prism Forge
  Block Puzzle". The `<h1>`s stay "Prism Forge" — that is the brand and the
  on-device display name. Update the titles if the listing name changes again.
