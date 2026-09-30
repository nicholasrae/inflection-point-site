# Inflection Point Site

Static GitHub Pages website for [inflectionpoint.me](https://inflectionpoint.me/). HTML, CSS, images and bundled fonts are served directly; no application framework, dependency installation or mailing-list backend is required.

## Deployment

- Repo: `nicholasrae/inflection-point-site`
- Branch: `main`
- Host: GitHub Pages
- Custom domain: `inflectionpoint.me`
- App Store ID: `6759310530` — not a current download CTA

Pushes to `main` deploy automatically through GitHub Pages.

## Launch and product copy

The App Store release is in preparation. On September 30, 2026, the public US listing returned 404 and Apple's lookup returned no result. Release readiness includes app validation and provider/privacy review; do not imply Apple approval is the only remaining step. The pending native version is not advertised as publicly released.

Launch CTAs open an email request to the developer. The visitor must send it to request a launch update; no automatic subscription or notification is created by clicking. Change CTAs to download links only after a fresh check proves the actual listing is live and the intended app release is available:

```text
https://apps.apple.com/app/id6759310530
```

Access is explicitly **planned for launch**: a 72-hour full-access preview without automatic billing; afterward, one synthesis per day, seven days of visible history and one active project remain free. Lifetime access is a one-time purchase at the planned US price of **US$14.99**, with Apple's localized price shown before purchase. Keep history-retention and complete-export claims scoped to the planned release, not older installed versions.

The hero and three-screen preview use authentic earlier development captures, clearly labelled as such. Optional AI generation sends text and identity context online; do not add anonymous, zero-retention, no-training, clinical-outcome or already-public native/iOS27 claims.

## Files and local preview

- `index.html`, `styles.css`: landing page, six-step protocol, access and FAQ.
- `privacy.html`, `terms.html`, `legal.css`: existing legal content with presentation/accessibility improvements.
- `404.html`: branded missing-page navigation.
- `images/`: existing app captures/icon and the 1200×630 social card.
- `fonts/`: self-hosted Manrope and Barlow Condensed, with their SIL Open Font License files. Retain those notices.
- `robots.txt`, `sitemap.xml`, `CNAME`: indexing and GitHub Pages configuration.

From this directory:

```sh
python3 -m http.server 8766 --bind 127.0.0.1
```

Open `http://127.0.0.1:8766/`. No dependency installation is needed.

## Audit and legal boundaries

See [the September 30 audit](WEBSITE-AUDIT-20260930.md) for measured baseline/local results and unresolved findings. Evidence is preserved outside Git in `/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930`. Final public verification was pending when these local results were documented; record subsequent deployment checks there.

Legal paragraphs, lists, headings, dates and existing link targets remain unchanged: 65 substantive items were compared exactly. This redesign does not reconcile the existing policy's AI/local-storage contradiction or settle provider processing terms. [Draft policy PR #1](https://github.com/nicholasrae/inflection-point-site/pull/1) remains separate and unmerged; its native disclosures must match the actual app rollout before publication.

## Verification checklist

Before and after deployment:

1. Review product/availability copy, relative assets, fragment links, font notices, keyboard focus, mobile layout and reduced motion. Keep legal-content changes separate.
2. Review the diff before committing/pushing the intended work to `main`; this publishes through GitHub Pages.
3. Wait for the Pages deployment, then fetch fresh public content and confirm the expected source/assets are served.
4. Verify the root, legal pages, robots, sitemap, social card/fonts and a genuinely missing route. Recheck mobile layout/accessibility and performance against the deployed site; local scores do not establish live results.

Public URLs:

- `https://inflectionpoint.me/`
- `https://inflectionpoint.me/privacy.html`
- `https://inflectionpoint.me/terms.html`
- `https://inflectionpoint.me/robots.txt`
- `https://inflectionpoint.me/sitemap.xml`
