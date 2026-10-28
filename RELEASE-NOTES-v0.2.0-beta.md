# Nono ZIP Merge v0.2.0-beta

First public beta for Apple Silicon Macs. Extract and merge multiple ZIP archives into one new folder, keep their structure, and resolve duplicate names without overwriting original archives.

## Download

- `Nono-ZIP-Merge-v0.2.0-beta-macOS-arm64.zip`
- `SHA256SUMS.txt`

Requires Apple Silicon (arm64) and macOS 14 or later. Check the ZIP with `shasum -a 256` and compare the result with `SHA256SUMS.txt` before extracting.

## Signing status

**Locally ad-hoc signed only. No Apple Developer ID signature. Not notarized by Apple.** macOS may block this beta. Keep Gatekeeper and other system protections enabled; if blocked, wait for a properly signed and notarized release. This is not a notarized stable release.

## What's included

- ZIP folder merging, optional SHA-256 deduplication at matching paths, numbered filename conflicts, progress, cancellation, and JSON reports.
- Eight languages: English, Traditional Chinese, Simplified Chinese, Japanese, Korean, German, French, and Spanish.
- Settings, About, localized messages, and optional PayPal/USDT support with offline QR generation.
- App resources bundled with the executable; no developer tools needed for use.

## Validation scope

The final preparation results are recorded in `VALIDATION-SUMMARY.md`. Automated checks cover synthetic archives, language resources, QR payloads, bundle integrity, and local signature verification. They do not certify safe operation for every archive or validate recipient ownership or actual payments.

Manual acceptance remains open for complete GUI workflows, real large photo collections, legacy ZIP encodings, large physical ZIP64 files, external/network filesystems, the full macOS compatibility range, accessibility, and a quarantined download on another Mac. Keep backups and test with disposable data first.

## Support and privacy

Freeware: personal and commercial use are free; donations are optional. Copyright is retained, source code is private, and unauthorized redistribution, resale, or publication of modified versions is not permitted. See the [Freeware license](README.md#freeware-license) for the complete terms. USDT support uses **BNB Smart Chain (BEP20) only**. Confirm the recipient, asset, and network yourself; incorrect transfers may cause loss. Reports contain local paths and must be reviewed before sharing. The repository publishes documentation and compiled downloads; Swift source code is private.

## 繁體中文

首個公開測試版，支援 Apple Silicon 與 macOS 14 以上。可合併多個 ZIP、保留資料夾結構、去重與編號保留不同檔案，並支援八種語言與自願贊助。僅完成本機 ad-hoc 簽署，尚未 Developer ID 簽署或 Apple 公證；可能被 macOS 阻擋，請勿停用 Gatekeeper。完整人工驗收與實際收款驗證仍待完成，請先備份並使用可丟棄的資料測試。
