# Changelog

## v0.3.0-beta — 2026-11-25

- Improved drag payload handling, ordered batches, failure feedback, and duplicate handling.
- Added optional extraction next to ZIPs sharing the same actual parent folder.
- Added shared-root or first-ZIP naming, explicit fallback, destination preview, and safe numbered conflicts.
- Preserved manual output selection, archive structure, deduplication, reports, cancellation, and exclusive atomic publication.
- Excluded generated output folders from recursive source discovery.
- Updated all eight languages. Automated validation covers 84 cases. The user separately reported four real Finder/output acceptance scenarios as passed.
- Local ad-hoc signature only; no Developer ID or Apple notarization. External/network filesystems and remaining manual scenarios are unverified.


## v0.2.0-beta — 2026-10-28

- Added eight interface languages, system-language matching, and a saved manual language choice.
- Added an optional support window, PayPal and USDT QR codes, and copy controls.
- Added Settings and About windows and localized error presentation.
- Included language resources inside the app bundle for portable distribution.
- Rebuilt and revalidated after relocating the private development project; release resource loading avoids the development-path fallback.
- Retained ZIP merge, duplicate handling, cancellation, JSON reporting, and existing safety checks.

This beta uses only a local ad-hoc signature. Apple Developer ID signing and Apple notarization are not included. See the release notes for validation scope and pending manual checks.

## v0.1.0 — initial local prototype

Introduced native ZIP extraction and merging, preserved folder structure, optional deduplication, numbered conflicts, cancellation, reporting, and archive safety checks. This entry describes development history; it does not announce a separately available public download.
