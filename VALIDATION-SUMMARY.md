# Local validation — v0.2.0-beta

Prepared on 2026-10-28 using an Apple Silicon Mac running macOS 26. This is local beta evidence, not a certification for all macOS versions or filesystems.

- Swift release app build: passed.
- Existing synthetic-archive regression harness: 29 cases, 0 failures.
- Support-feature harness: 18 cases, 0 failures, including eight-language resources, language preferences, QR payload decoding, and an isolated native test clipboard.
- Eight language resource sets: 84 keys each, compared with their build inputs.
- Eight-language native main/support windows: launched and captured; both QR payloads decoded from each support-window capture.
- Bundle completeness and arm64 architecture: checked.
- ZIP CRC, extraction, byte-for-byte file comparison, executable permissions, and extracted app signature: checked during final packaging.
- Local code signature: valid **ad-hoc** signature only; **no Developer ID signature or Apple notarization**.
- Public files are selected using an explicit allowlist. Documentation and uncompressed bundle contents are scanned for known local path, private account, and credential patterns. This scan is not an exhaustive guarantee against all secrets.

Restricted-environment attempts initially encountered moved compiler-cache paths and unavailable desktop services. The final build used fresh caches, and native-service tests were rerun successfully. Earlier failures were not counted as passes.

Full manual GUI acceptance, real large archives, legacy ZIP encodings, physical large ZIP64 files, ExFAT/network volumes, all target macOS versions, accessibility, actual PayPal receipt, wallet ownership/payment receipt, and fresh-download Gatekeeper acceptance remain **unverified**. No payment or chain transaction was made. Screenshots show idle app windows, not a complete user workflow.

The app's numeric bundle version remains `0.2.0`; its UI and public distribution label identify the build as `v0.2.0-beta`.

## Payment identity and privacy review

Before publication, the user confirmed that the public PayPal payment page displays “Nono ZIP Merge” and accepted the risk that payment may reveal recipient identity. This publication hold has been cleared by the user. HTTP reachability and QR payload checks do not verify account ownership or actual payment receipt; no payment or chain transaction was made during preparation.
