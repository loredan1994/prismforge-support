# Prism Forge legacy URL compatibility

The canonical website is https://prismforge.calimanu.com/, hosted on Cloudflare Workers Static Assets.

This GitHub Pages repository stays enabled because released apps and App Store metadata contain these URLs. Its HTML pages use immediate browser redirects plus visible fallback links. Keep the repository, Pages deployment and existing paths. The old root opens support; privacy and terms open their corresponding documents.

Current website source is in the app project, `site/public`. Hosting config: `site/wrangler.jsonc`.

Migration date: 25 September 2026. Pre-migration commit for rollback: `e9e23815e815cb9c7f332782f6bc00ed6fe16e14`.
