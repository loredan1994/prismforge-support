# Prism Forge web pages

Two static pages required by App Store Connect and TestFlight external testing:

- `index.html` — support page (App Store "Support URL", TestFlight feedback pointer)
- `privacy.html` — privacy policy (App Store "Privacy Policy URL", required even for
  apps that collect nothing)

No JavaScript, no analytics, no external resources — the pages keep the same
privacy promise as the app.

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

- Confirm the contact email in both pages (currently `loredan6@live.com`).
- If the App Store name ends up different from "Prism Forge", update the titles.
