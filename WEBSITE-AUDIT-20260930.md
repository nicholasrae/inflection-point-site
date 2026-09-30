# Inflection Point website audit — September 30, 2026

The redesign and local verification are complete; final public deployment verification was pending when this report was prepared. The website remains a static GitHub Pages site. This work improves presentation and launch information without publishing the unshipped native app or changing legal substance. Later public checks belong in the external evidence directory below.

## Scope and material changes

Reviewed the live homepage, privacy/terms, hosting responses, metadata, assets, keyboard/mobile behavior and product copy against retained legacy code and the pending native implementation. Baseline homepage source matched `main` commit `08e1588`. The public US App Store URL returned 404 and Apple lookup returned zero results; the pending native candidate has not been uploaded.

| Area | Finding and resulting change |
| --- | --- |
| Positioning and launch | Replaced vague outcome/Apple-only launch language with the concrete planning/reflection loop and “release in preparation.” Mailto CTAs explain that visitors must send an email. No broken App Store download CTA or claim that native/iOS27 is already public. |
| Product/access | Six steps: Anti-vision → Vision → 1-Year Goals → Projects → Daily Quests → Synthesis. Planned access explains the 72-hour preview, continued free limits and single lifetime purchase. US$14.99 is qualified by storefront-localized pricing. |
| Preview | Three authentic development screens plus the opening-question hero are labelled as earlier captures. The release interface may differ. |
| Layout and performance | Responsive preview layout, explicit image dimensions, prioritized hero/lazy lower images, external static CSS and self-hosted fonts retain the small static architecture. |
| Accessibility | Main includes primary content; focusable skip links, semantic headings, visible focus, larger targets, dark color-scheme and reduced-motion handling address baseline findings. Native details/summary elements provide the FAQ. |
| Discovery and recovery | Canonical/social metadata, a dedicated 1200×630 social image, robots/sitemap and branded 404 support sharing, indexing and recovery from missing links. No unsupported rating/user-count claims or structured offer implying current availability. |
| Legal presentation | Privacy/terms gain shared responsive styling, skip navigation and larger targets. Their substantive text, dates and existing links are preserved; no provider-policy approval is implied. |

## Measured verification

The retained Lighthouse 13.5.0 mobile runs used simulated throttling and a 412×823 viewport. Baseline was the public HTTPS site; the changed-page run was localhost, so hosting/network conditions differ. These are single lab measurements, not field Core Web Vitals or guaranteed visitor outcomes.

| Check | Public baseline | Local redesigned preview |
| --- | ---: | ---: |
| Lighthouse Performance / Accessibility / Best Practices / SEO | 79 / 95 / 100 / 100 | 100 / 100 / 100 / 100 |
| Cumulative Layout Shift | 0.501 | 0 |
| Homepage axe violations / incomplete checks | 3 / 2 | 0 / 1 |

Baseline axe findings were contrast, content outside landmarks and an unfocusable scrollable region. The one local incomplete check concerned the decorative, aria-hidden down arrow; manual contrast review measured 17.77:1 (`#f5f1e8` on `#080807`). That check is recorded separately rather than relabelled as an automated pass. Zero reported violations is not a conformance certification.

Final local Chromium interaction checks passed at widths 320, 390, 640, 768 and 1440: no horizontal overflow; primary header, CTA, footer and FAQ targets at least 44×44; one main/one h1; bundled fonts loaded; and no external runtime requests or JavaScript errors. Tab → skip link → Enter focused main, all five header anchors landed below the sticky header, the preview-subscription FAQ opened/closed with Enter, and reduced-motion scrolling became automatic. The mobile custom 404 had no horizontal overflow, axe zero violations/zero incomplete checks, a working return CTA and `noindex`. These are local test conditions, not device or assistive-technology certification.

Both legal pages were visually/layout checked at 320×900 and 1440×1000 in Chromium: no horizontal overflow, visible focus, skip navigation targeting main and each existing link target at least 44×44 passed. Each page's retained **mobile** axe scan reported zero violations and zero incomplete checks. These artifacts do not establish a separate desktop axe scan. Exact legal-text comparison passed for 34 privacy items and 31 terms items, including dates and existing link destinations.

## Open findings and release boundaries

1. **P1 — Legal substance needs separate reconciliation.** The existing privacy policy says journals leave only for export/backup while also describing online AI processing. Its optional-iCloud wording and generic export/deletion claims need to match the actual installed app. Presentation checks do not resolve these issues.
2. **P1 — Provider processing remains unverified.** Toolkit-specific retention, training/human review, deletion and downstream contractual settings remain open. Do not promise zero retention, anonymity or no training. [Policy PR #1](https://github.com/nicholasrae/inflection-point-site/pull/1) remains a separate draft; its native StoreKit/export/recovery disclosures must not be presented as current legacy behavior.
3. **P1 — Planned retention is not an older-app guarantee.** Legacy free history can be pruned, and its export omits several collections. The homepage scopes saved-history preservation and complete export to the planned release. Do not imply the redesign repairs existing app data or validates purchase/upgrade behavior.
4. **P2 — Verify deployment and availability freshly.** Confirm deployed HTML/assets, redirects, legal-text preservation, metadata, 404 behavior and rendered checks after Pages publication. Change launch CTAs only after the actual Apple listing becomes available, not merely after an internal beta or archive succeeds.
5. **P3 — Hosting and manual coverage remain bounded.** GitHub Pages security-header limitations and the retained large icon are lower-priority hardening/asset opportunities. No Safari, VoiceOver, physical-device, real-user performance or WCAG certification is claimed. Keep the static architecture; do not add a framework or ineffective host-specific header file to address these observations.

No explicit clinical efficacy or unsupported customer/view counts were found in the baseline homepage. The personal-development/medical disclaimer remains in Terms; AI output is for reflection and creative use, without guaranteed personal or health outcomes.

## Evidence

Preserved outside Git at `/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930`:

- [Technical HTTP/source baseline](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/technical/technical-findings.md), including response captures and deployment/source findings.
- [Baseline Lighthouse report](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/before/lighthouse-mobile.report.html) and `before/axe-mobile.json`.
- [Local Lighthouse report](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/after/lighthouse-local-mobile.report.html), `after/axe-local-mobile.json`, and desktop/mobile captures.
- [Final responsive/interaction QA](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/after/responsive-interaction-qa.json) and [mobile 404 axe result](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/after/axe-local-404.json).
- [Exact legal-text preservation proof](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/technical/legal-presentation/legal-text-preservation-proof.json) and [rendered legal QA](/Users/nick/Documents/InflectionPoint-Releases/WebsiteAudit-20260930/technical/legal-presentation/rendered-qa/rendered-qa.json).

This report records audit/local validation, not publication, policy sign-off or app release readiness.
