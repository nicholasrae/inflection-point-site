# Planned Apple AI: daily debrief and system avatars — September 30, 2026

This branch prepares disclosures for an unreleased native update. It does not announce an App Store release or replace historical policy archives. The maintained avatar path is being changed from Rork requests to Apple’s system Image Playground. The daily debrief remains separate and on device. Final native implementation validation and review are required before this website change is published.

## Intended app boundary

- Daily debrief: `SystemLanguageModel.default` through Foundation Models processes reflection and relevant identity context on the iPhone. There is no Rork, Private Cloud Compute or other cloud debrief fallback. Manual Quick Log remains available when eligibility, settings, language/region, model readiness or generation errors prevent AI use.
- Avatar: after feature-specific agreement, pass only selected active traits, optional character name and up to two vision descriptions to `imagePlaygroundSheet`. Do not supply a source image. The system sheet may let the user explicitly choose a personal photo; that is separate from an automatic app-provided photo. Copy the selected generated result into app-owned storage through the existing draft/save boundary.
- Restrict the app’s sheet to Apple’s Illustration, Animation and Sketch styles. Do not offer `.externalProvider` or Genmoji. Check system availability before presentation and retain photo/camera alternatives. Apple controls image processing, network requirements and usage limits; no offline, unlimited-generation or all-device promise is made.

## Primary Apple evidence, checked September 30, 2026

- [Create high-quality images using Image Playground, WWDC26](https://developer.apple.com/videos/play/wwdc2026/375/) explicitly places the new image model on Private Cloud Compute and explains system usage limits. It also describes restricting the style picker: the external-provider style is opt-in and exposes the provider configured by the user, such as ChatGPT. Excluding it does not make Apple’s iOS 27 generation local. The session’s concepts, options, completion callback and photo personalization describe a system-controlled sheet rather than an app-managed provider endpoint.
- [Apple Intelligence & Privacy](https://www.apple.com/legal/privacy/data/en/intelligence-engine/) gives Image Playground as an example of a description sent to Private Cloud Compute. Apple describes processing there to fulfill the request without retaining the content afterward, and separately describes limited request metadata, optional aggregate Device Analytics and the Apple Intelligence & PCC Report. These are Apple’s stated system practices, not a blanket promise about every Apple service, historical provider or AI feature.
- [Create original images with Image Playground, current iOS 27 guide](https://support.apple.com/en-gb/guide/iphone/iph0063238b5/ios) describes eligible Apple Intelligence devices, language/region constraints and server-feature usage limits. It also supports adding descriptions or personal photos in the system interface. iOS compatibility alone does not establish Image Playground availability.
- [ChatGPT Extension & Privacy](https://www.apple.com/legal/privacy/data/en/third-party-ai/) distinguishes extension use without an account from signed-in use, where account settings and OpenAI’s policies apply. This is relevant to Apple’s optional external-provider experience generally; the app’s planned allowed-style list does not offer it. Do not import its retention or training statements into historical Rork requests.
- [Generating content with Foundation Models](https://developer.apple.com/documentation/foundationmodels/generating-content-and-performing-tasks-with-foundation-models), [model availability](https://developer.apple.com/documentation/foundationmodels/systemlanguagemodel/availability-swift.property) and [locale support](https://developer.apple.com/documentation/foundationmodels/systemlanguagemodel/supportslocale(_:)) support the separate on-device daily debrief and its fallback. [Apple’s requirements](https://support.apple.com/en-us/121115) cover hardware, language, region and settings constraints.

## App-source checks required before publication

Review the final avatar integration, `native/App/AnalysisClient.swift`, `native/App/Views.swift`, resources and tests in the Inflection Point app checkout. Record the final source and validation evidence externally. Confirm:

1. The daily debrief remains only `SystemLanguageModel.default`, with runtime availability/locale checks, validated output and draft-preserving Quick Log fallback.
2. The maintained app has no Rork avatar request, provider endpoint, embedded key or silent image-generation fallback. Apple’s sheet receives only the agreed selected text and no app-supplied source image.
3. The sheet offers only Illustration, Animation and Sketch styles, checks availability again at presentation, and keeps photo/camera routes available.
4. Cancel or failed generation/save preserves the previous avatar and unsaved draft. Successful output is durably copied before the journal references it; an error never implies saved success.
5. Apple-controlled cloud processing and limits are explained separately from local debrief processing and Inflection Point’s pay-once access. Actual system availability, sheet cancellation and selected output still require appropriate runtime/device validation.
6. Existing screenshot bytes and their original failed whole-journey evidence stay unchanged. They are fictional development captures, not proof of the new avatar sheet or a production AI request.

Earlier Expo versions and native betas submitted avatar/debrief context to Rork. Their toolkit-specific retention, training, human review, deletion and downstream processing remain unverified. Moving the maintained path does not erase that history. Pay-once access, planned US$14.99 pricing, all four tabs and release-in-preparation status are unchanged.

## Current capture scope

The four website PNGs are unchanged normal-size captures from native development version 2026.9.30 (2), source `dd733c906029f6b620ef575e88a15e8e9153940b`, with fictional data. Synthesis shows manual Quick Log; these images do not prove Apple Intelligence generation. Independent preview validation includes all four passed normal strict audits, the functional checkpoint, all eight passed composer audits and final draft comparisons. The whole native journey remains **failed** with two unignored largest-text clipping assertions, so the app release gate stays open. This is scoped preview evidence, not a physical-device, VoiceOver, whole-UI or release pass.

Exact source/build/attachment provenance, the retained failed result, original PNG hashes and post-copy source checks are preserved outside Git in `/Users/nick/Documents/InflectionPoint-Releases/WebsiteNativeScreens-20260930`. This new disclosure branch still requires review of its final local results and fresh public verification after deployment.
