# Validation summary — v0.3.0-beta

Validation evidence collected on 2026-11-25. These checks are not universal compatibility certification or Apple notarization.

## Automated evidence

The existing 84-case harness was rerun during preparation: 29 core, 18 support, and 37 v0.3 cases, with zero failures. The support suite includes version and intentionally limited core-change scope assertions updated for v0.3; it does not claim the entire original core is unchanged.

Coverage includes cross-parent rejection, common-root detection/fallback, ordered drop payload handling, numbered destination conflicts (including late collisions), source ZIP immutability, traversal/link rejection, cancellation and cleanup, resource limits, language resources, QR payloads, and an isolated native clipboard. Each of eight languages has 108 interface strings.

The unsupported-filesystem check injects ENOTSUP at the exclusive-rename boundary. Permission checks use local restricted directories. Neither demonstrates physical ExFAT, SMB, other network-volume, or TCC compatibility.

## User-reported real-Mac acceptance

The user explicitly reported these four scenarios as passed on 2026-11-25:

1. Single ZIP dragged from Finder appears in the list.
2. Multiple ZIPs dragged together all appear in the correct order.
3. Dragging a folder containing ZIPs finds the files.
4. Extraction next to sources uses the correct automatic name and location.

These are user-reported observations, not independently repeated by Codex or inferred from automated tests. No exact test machine version, filesystem, recording, or dataset fingerprint was supplied. Codex separately observed native file-picker addition, path preview, extraction, displayed final path, and restoration of manual controls.

## Packaging

The existing accepted v0.3 app is packaged without rebuilding or changing it. Bundle version, resources, archive round-trip, content hashes, executable permission, and deep strict local signature verification are checked during preparation. Only an ad-hoc signature is present; no Developer ID or Apple notarization is claimed. Documentation and unpacked bundle contents are checked against explicit allowlists and selected sensitive-data patterns; this is not an exhaustive secret guarantee.

## Still unverified

Mixed ZIP/folder Finder drops, Finder rejection/duplicate/special-name cases, the original failure's precise event/provider trigger, physical ExFAT/network volumes, TCC restrictions, all target macOS versions, large real archives/ZIP64 datasets, full eight-language GUI/accessibility checks, actual payment receipt, and quarantined-download Gatekeeper acceptance remain unverified. Keep backups and test with non-important data.

The three screenshots now show actual accepted v0.3.0-beta app windows: English manual-output mode, Traditional Chinese extraction next to sources, and English new-folder/path preview. Only synthetic text ZIPs and generic temporary demo paths were used. Screenshots do not certify every manual workflow. The current beta uses a separate preferences identity from v0.2.
