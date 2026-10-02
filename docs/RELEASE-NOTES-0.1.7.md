# LabelFlow v0.1.7 — Release Notes

**Published:** 2026-10-01 (v0.1.7, versionCode 8)
**Artifact:** `LabelFlow-0.1.7.apk` — SHA-256 `46baf25d956dfbf1195737bf2f1b8951f48f7e7d37ae04fbc21c5e198ea7f277`

This release is the **fifth-round review closure** of the LabelFlow audit
series. It is published here as a demonstration artifact for evaluation and
portfolio reference.

## Changes in v0.1.7 (vs v0.1.6)

- **R1 — Buyer upgrade note**: README documents the stricter activation
  storage format; users upgrading from v0.1.5 or earlier are told to re-enter
  their purchased code once.
- **R2 — Render ack gating + injection hardening**: PDF export waits for the
  label renderer's JS acknowledgement (with a timeout fallback) before opening
  the system print dialog; user-entered values are escaped via
  `JSONObject.quote` to prevent HTML/JS injection into the label document.
- **R3 — Lint baseline**: a `lint-baseline.xml` is committed so lint
  regressions are visible against a known-good state.
- **R4 — Privacy wording**: the privacy policy is rewritten in plain language
  (no data collected, no network permission, local-only activation flag).

## Earlier lineage (summary)

- v0.1.2 — HMAC short-signature activation introduced (5-char signature,
  ~60.5M space).
- v0.1.3 — activation strength: failure-count cooling (5 wrong → 10-min
  lockout), keygen interop tests, debuggable hygiene, honest docs.
- v0.1.5 — watermark sample preview, demo-code documentation, HMAC key
  de-hardcoding in the distribution flow.
- v0.1.6 — fourth-round review closure.

## Activation note for this public build

The public v0.1.7 APK ships **without** the evaluation demo codes (they are
excluded from this public repository on purpose). The activation dialog
expects a purchased code. The current commercial version (v0.2.0) is
distributed via Gumroad; this public artifact is for evaluation only.

## Disclaimer

LabelFlow renders labels in the FDA 2016 format as a design aid. It is not a
substitute for professional regulatory or legal review of food labeling.
