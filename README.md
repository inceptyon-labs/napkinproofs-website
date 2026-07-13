<p align="center">
  <img src="assets/favicon.svg" alt="Napkin Proofs" width="72">
</p>

<p align="center">
  <strong>Proofs too big for the margin, small enough for a napkin.</strong><br>
  45 to 60 second animated math. Surprising results, exact geometry, checked against the source.
</p>

<p align="center">
  <a href="https://napkinproofs.inceptyon.io">Website</a> ·
  <a href="https://youtube.com/@NapkinProofs">YouTube</a> ·
  <a href="https://instagram.com/napkinproofs">Instagram</a> ·
  <a href="https://facebook.com/1230203483505455">Facebook</a>
</p>

---

# Napkin Proofs — website

Marketing site for the Napkin Proofs channel. Static HTML, no build step, deployed
on Cloudflare Pages at [napkinproofs.inceptyon.io](https://napkinproofs.inceptyon.io).

Also serves the Privacy Policy and Terms of Service pages required by the platform
publishing apps (TikTok in particular).

## Structure

```
index.html        landing page
privacy.html      privacy policy   (required by TikTok / Meta app review)
terms.html        terms of service (required by TikTok / Meta app review)
404.html          not-found page
css/              main.css (tokens, base, layout) + components.css
assets/           favicon.svg, og-image.png
_headers          Cloudflare security headers + CSP + caching
_redirects        Cloudflare redirect rules
robots.txt, sitemap.xml, manifest.json
```

## Design

Ink-on-navy, matching the channel's own aesthetic: amber (`#E1925A`) hand-drawn
geometry on dark navy (`#131A24`), STIX Two Text for display, Hanken Grotesk for
body. The imagery is generated SVG diagrams of each featured theorem, not stock
photography.

## Deploy

Cloudflare Pages, direct from this repo (or drag-drop the folder). No build command;
output directory is the repo root.

```
npx wrangler pages deploy . --project-name napkinproofs
```

Then point `napkinproofs.inceptyon.io` at the Pages project in the Cloudflare
dashboard.
