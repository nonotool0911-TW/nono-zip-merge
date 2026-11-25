# Nono ZIP Merge v0.3.0-beta

A beta update for Apple Silicon Macs, with improved drag handling and optional extraction next to source ZIPs.

## Downloads

- `Nono-ZIP-Merge-v0.3.0-beta-macOS-arm64.zip`
- `SHA256SUMS.txt`

Requires Apple Silicon (arm64) and macOS 14 or later. The minimum deployment target does not mean every macOS version has been tested. Compare the ZIP's `shasum -a 256` result with the published checksum before extracting.

## What's new

- Read file-drop URL representations in ordered batches and provide feedback for unreadable, unsupported, timed-out, duplicate, and rejected items.
- Add **Extract next to source ZIPs (create a new folder)**, off by default. Actual ZIPs must share one parent folder; otherwise use the retained manual output selection.
- Choose a unique shared top-level folder or the first ZIP name in the displayed list. A confirmed shared root is removed exactly once, avoiding double nesting. An explicit fallback keeps the complete internal archive structure.
- Preview the complete destination. Use safe numbered names when occupied and show the actual path after completion. Never overwrite existing destinations or modify the original ZIPs.
- Recheck source and destination identities, preserve existing resource limits, deduplication, reports and cleanup, and retain exclusive atomic publication without an unsafe fallback.
- Skip generated output folders during recursive source discovery. Update the interface in all eight supported languages.

This beta has separate preferences from v0.2.0-beta; language selection may need to be set again.

## Verification and remaining acceptance

- Automated regression and feature validation: **84 cases, 0 failures** (29 core, 18 support, 37 v0.3 cases).
- **User-reported real-Mac acceptance:** single ZIP drag, multiple ZIP drag with correct order, a folder containing ZIPs, and extraction next to sources with correct naming/location all passed. These are the user's observations, separate from automated tests and Codex's own file-picker/output GUI checks.
- Different actual source parents, destination collisions, source ZIP protection, cancellation, and failure cleanup have automated evidence. Unsupported-filesystem behavior is tested with an injected error; this is not real ExFAT or network-volume acceptance.

Mixed ZIP/folder Finder drags, invalid/duplicate/special-name Finder cases, TCC restrictions, physical ExFAT/network volumes, full macOS compatibility, large real datasets, accessibility, and fresh-download Gatekeeper behavior still need manual acceptance. The original drag failure's precise event/provider trigger was not independently proven; successful user acceptance does not establish that low-level root cause.

## Signing and safety

**Local ad-hoc signature only. No Apple Developer ID signature. Not notarized by Apple.** Gatekeeper may prevent the app from opening. Keep macOS protections enabled; if blocked, wait for a properly signed and notarized release. Download integrity and signature consistency are not Gatekeeper or Apple notarization approval.

This is beta software. Keep backups and test with non-important data first. Use is freeware for personal and commercial purposes, with optional donations; copyright is retained and unauthorized redistribution, resale, or publication of modified versions is not permitted. See the [Freeware license](README.md#freeware-license).

PayPal/USDT payment receipt is not verified by QR checks. USDT uses **BNB Smart Chain (BEP20) only**; confirm recipient, address, asset and network yourself. Reports contain paths: review and redact them before sharing.

## 繁體中文

v0.3.0-beta 改善拖曳批次接收與失敗回饋，新增預設關閉的原地輸出、共同頂層或第一個 ZIP 命名、完整路徑預覽與安全編號衝突處理，保留手動輸出、目錄結構、去重與 JSON 報告。

84 項自動測試通過。使用者另回報真實 Finder 單 ZIP、多 ZIP、包含 ZIP 的資料夾拖曳，以及原地輸出命名／位置四項通過；此為使用者實機回報，不能擴大為全部人工驗收完成。ExFAT／網路磁碟、其他拖曳邊界、權限與跨系統等項目仍待驗收。

僅 ad-hoc 簽署，未 Developer ID 簽署或 Apple 公證，可能被 Gatekeeper 阻擋。請保留系統保護、先備份並使用非重要資料測試。個人及商業使用免費，贊助自願。本版本以 Pre-release 提供。
