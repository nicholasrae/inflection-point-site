# Inflection Point Site

Static GitHub Pages landing page for [inflectionpoint.me](https://inflectionpoint.me/).

## Deployment

- Repo: `nicholasrae/inflection-point-site`
- Branch: `main`
- Host: GitHub Pages
- Custom domain: `inflectionpoint.me`
- App Store ID: `6759310530`

Pushes to `main` deploy automatically through GitHub Pages.

## Current launch state

The public App Store URL is not live until Apple approval completes. While the URL returns 404, primary CTAs should point to a launch-notice email action instead of the App Store page.

When Apple flips the listing live, update CTAs back to:

```html
https://apps.apple.com/app/id6759310530
```

Recommended live CTA copy:

- Header: `Download Free`
- Hero: `Try Premium Free`
- Pricing: `Get Inflection Point`

## Offer copy

Keep public copy aligned with the real IAP:

- 3 days free
- $14.99 one-time lifetime unlock
- No subscription / no auto-renewal

## Verification checklist

After edits:

1. Validate local links/assets.
2. Commit and push to `main`.
3. Wait for GitHub Pages deployment to complete.
4. Verify live URLs:
   - `https://inflectionpoint.me/`
   - `https://inflectionpoint.me/privacy.html`
   - `https://inflectionpoint.me/terms.html`
   - `https://inflectionpoint.me/robots.txt`
   - `https://inflectionpoint.me/sitemap.xml`
