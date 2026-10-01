# Planned daily Apple AI debrief — September 30, 2026

This is a website disclosure change for an unreleased native build. It does not announce an App Store release, replace historical policy archives, or claim that the implementation has passed its final tests. Publication requires final source validation and source-verified, visually reviewed captures.

The intended native path is `SystemLanguageModel.default` through Apple’s Foundation Models framework for the daily debrief. Reflection and relevant identity context are processed on the iPhone; there is no Rork or other cloud debrief fallback. Manual Quick Log remains the alternative when eligibility, settings, language/region, model readiness or generation errors prevent AI use. AI avatar generation remains a separate Rork HTTPS request with explicit selected-context consent; the selected photo is not part of that request.

## Primary Apple evidence

- [Generating content with Foundation Models](https://developer.apple.com/documentation/foundationmodels/generating-content-and-performing-tasks-with-foundation-models) describes the on-device language model, checking availability before use, and providing a fallback. This supports a claim about the selected on-device debrief path, not every Apple Intelligence feature.
- [SystemLanguageModel availability](https://developer.apple.com/documentation/foundationmodels/systemlanguagemodel/availability-swift.property) and [locale support](https://developer.apple.com/documentation/foundationmodels/systemlanguagemodel/supportslocale(_:)) provide runtime checks. The installed iOS 27 SDK exposes `.default`, `.availability` and `.supportsLocale(_:)` from iOS 26. Unavailable reasons include an ineligible device, Apple Intelligence disabled and the model not ready.
- [Apple’s current requirements](https://support.apple.com/en-us/121115) identify hardware, language, region and settings constraints. Do not equate support for iOS 26 or 27 with support for Apple Intelligence, or promise AI on every iPhone.
- [Apple’s Image Playground session](https://developer.apple.com/videos/play/wwdc2026/375/) explains that its new image generation uses Private Cloud Compute and may expose an optional external provider. Image Playground is not the avatar implementation in this change; no Apple/offline image-generation claim belongs on this website.

## App-source checks required before publication

Review `native/App/AnalysisClient.swift`, `native/App/Views.swift` and their final tests in the Inflection Point app checkout. Record the validated source commit and exact captures in the external website evidence directory before publishing this branch. Confirm:

1. The daily debrief uses only `SystemLanguageModel.default`, checks runtime availability and locale, and preserves drafts with a Quick Log fallback.
2. No debrief prompt reaches `URLSession`, the Rork object endpoint, Private Cloud Compute or another fallback provider. The network path that remains is avatar generation.
3. Local debrief results pass domain validation before saving. The website does not call alignment an objective or clinical score.
4. The avatar flow still explains its selected name/traits/vision context, requires explicit agreement and keeps the photo out of its request.
5. Homepage screenshots are authentic captures of the final native interface. They are labelled development captures until the actual release is available, and do not imply a production Apple AI run if they show test fixtures or manual content.

Cloud-avatar and historical-request retention, training, human review, deletion and downstream processors remain unverified. Moving future debriefs on device does not delete previously submitted context or clear those provider, device-validation or release gates. Pay-once access, the planned US$14.99 price and release-in-preparation status are unchanged.

## Current capture scope

The four website PNGs are unchanged normal-size captures from native development version 2026.9.30 (2), source `dd733c906029f6b620ef575e88a15e8e9153940b`, with fictional data. Synthesis shows manual Quick Log; these images do not prove Apple Intelligence generation. Independent preview validation includes all four passed normal strict audits, the functional checkpoint, all eight passed composer audits and final draft comparisons. The whole native journey remains **failed** with two unignored largest-text clipping assertions, so the app release gate stays open. This is scoped preview evidence, not a physical-device, VoiceOver, whole-UI or release pass.

Exact source/build/attachment provenance, the retained failed result, original PNG hashes and post-copy source checks are preserved outside Git in `/Users/nick/Documents/InflectionPoint-Releases/WebsiteNativeScreens-20260930`. Publication still requires review of this website’s final local results and fresh public verification after deployment.
