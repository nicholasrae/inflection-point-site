# Inflection Point Site

Static GitHub Pages website for [inflectionpoint.me](https://inflectionpoint.me/). HTML, CSS, images and bundled fonts are served directly; no application framework, dependency installation or mailing-list backend is required.

## Deployment

- Repo: `nicholasrae/inflection-point-site`
- Branch: `main`
- Host: GitHub Pages
- Custom domain: `inflectionpoint.me`
- App Store ID: `6759310530` — not a current download CTA

Pushes to `main` deploy automatically through GitHub Pages.

The initial redesign was published at `5963424` on September 30, 2026. Additional audit actions are delivered in [PR #3](https://github.com/nicholasrae/inflection-point-site/pull/3). That review and the external deployment record identify the deployed commit and fresh public verification; this source document does not substitute local results for live evidence.

## Launch and product copy

The App Store release is in preparation. On September 30, 2026, the public US listing returned 404 and Apple's lookup returned no result. Release readiness includes app validation and provider/privacy review; do not imply Apple approval is the only remaining step. The pending native version is not advertised as publicly released.

Launch CTAs open an email request to the developer. The visitor must send it to request a launch update; no automatic subscription or notification is created by clicking. Change CTAs to download links only after a fresh check proves the actual listing is live and the intended app release is available:

```text
https://apps.apple.com/app/id6759310530
```

Access is explicitly **planned for launch**: one non-consumable lifetime purchase unlocks the core protocol, with no free trial, ongoing free tier or recurring subscription. The planned US price is **US$14.99**, with Apple's localized price shown before purchase. Lifetime access includes daily quests, synthesis, unlimited projects, full saved history and complete journey export. Keep history-retention claims scoped to the planned release, not older Expo versions. Complete native **journey** export includes journal collections and an embedded avatar; it excludes separate purchase, historical preview/usage and reminder preferences. Export and recovery of existing data remain available without purchase as data-protection utilities, not a free protocol tier. Historical preview and usage records remain preserved. See [the current payment-model change](PAYMENT-MODEL-20260930.md); prior audit reports describe the earlier model.

The hero and three-screen preview use authentic earlier development captures, clearly labelled as such. Optional AI generation sends text and identity context online; do not add anonymous, zero-retention, no-training, clinical-outcome or already-public native/iOS27 claims.

## Files and local preview

- `index.html`, `styles.css`: landing page, six-step protocol, access and FAQ.
- `privacy.html`, `terms.html`, `legal.css`: current September 30 wording and shared presentation.
- `privacy-2026-04-26.html`, `terms-2026-04-26.html`: previous policies, marked archival and excluded from indexing.
- `404.html`: branded missing-page navigation with external CSS.
- `images/`: app captures, social card, 32×32 favicon, 64×64 brand and 180×180 touch icons. Preserve the original 800×800 icon; the smaller PNGs are derived assets.
- `fonts/`: self-hosted Manrope and Barlow Condensed, with their SIL Open Font License files. Retain those notices.
- `robots.txt`, `sitemap.xml`, `CNAME`: indexing and GitHub Pages configuration.

From this directory:

```sh
python3 -m http.server 8766 --bind 127.0.0.1
```

Open `http://127.0.0.1:8766/`. No dependency installation is needed.

## Audit and legal boundaries

The [September 30 audit](WEBSITE-AUDIT-20260930.md) is historical. [Audit follow-ups](AUDIT-FOLLOWUPS-20260930.md) record current changes and prerequisites. Evidence is outside Git in `/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930` and `WebsiteAuditFollowup-20260930`; record subsequent deployment checks there. Local scores do not establish new live scores.

Current legal copy corrects known behavior claims and distinguishes earlier Expo versions, native RevenueCat betas and the planned StoreKit release. It covers online AI context, conditional legacy analytics, platform backups, local photos, partial legacy export, native history/reset/recovery and historical grants. Toolkit-specific retention, training, human review, deletion and downstream processing remain unverified; copy corrections do not clear that provider gate. The two April 26 archives preserve 63 non-title substantive items, with two titles intentionally identifying them as previous policies. [Draft policy PR #1](https://github.com/nicholasrae/inflection-point-site/pull/1) remains separate; review its overlap before any merge.

## Security metadata maintenance

All six HTML pages place `no-referrer` and CSP metadata immediately after charset. CSP permits same-origin CSS/images/fonts and blocks connections, forms, frames, objects and base-URL changes. Five pages prohibit scripts; the homepage permits only its exact JSON-LD hash. No inline style exception or external runtime script is needed.

Changing JSON-LD bytes, including whitespace, requires replacing the homepage `script-src` digest. Calculate it from the exact body:

```sh
python3 - <<'PY'
import base64, hashlib, re
from pathlib import Path
html = Path('index.html').read_bytes()
blocks = re.findall(rb'<script\b[^>]*type=["\']application/ld\+json["\'][^>]*>(.*?)</script\s*>', html, re.S | re.I)
if len(blocks) != 1:
    raise SystemExit('Expected one JSON-LD block; review script inventory.')
print('sha256-' + base64.b64encode(hashlib.sha256(blocks[0]).digest()).decode())
PY
```

Review any new script/resource before weakening CSP. Meta CSP cannot replace response-header protection. HSTS, `frame-ancestors`/X-Frame-Options, `nosniff` and Permissions-Policy remain host-capability constraints; another host's `_headers` file will not configure GitHub Pages. No hosting/DNS migration is part of this work. Retain bundled font OFL notices.

## Verification checklist

Before and after deployment:

1. Review product/version scope, CSP hash/order, local assets/fragment links, archive notices, font licenses, keyboard focus, mobile layout, FAQ and reduced motion.
2. Review the diff before committing/pushing the intended work to `main`; this publishes through GitHub Pages.
3. Wait for the Pages deployment, then fetch fresh public content and confirm the expected source/assets are served.
4. Verify the root, both current policies, both archives, robots/sitemap, social card/fonts/icons and a genuinely missing route. Recheck intended-resource/CSP behavior, mobile layout/accessibility and performance against the deployed site. A direct local `404.html` response does not prove the production host's missing-route status.

Safari WebDriver authorization, genuine VoiceOver interaction and real iPhone testing remain separate coverage. Do not claim those checks, field performance or WCAG certification without evidence. Email links should be inspected without sending a message during QA.

Public URLs:

- `https://inflectionpoint.me/`
- `https://inflectionpoint.me/privacy.html`
- `https://inflectionpoint.me/terms.html`
- `https://inflectionpoint.me/robots.txt`
- `https://inflectionpoint.me/sitemap.xml`
