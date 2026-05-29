# 2026.05.29.2

- Framework-dependent Windows x64 packages using shared DLLs.
- Requires the .NET 8 runtime.
- Includes the compact `meta-data-quality inspect` output: no success banner, no command-guidance prose, summary-first default output, and sanitized scalar-expression displays.
- Updates `meta-transform-script` so `CREATE VIEW` imports may omit `--target`; bare SELECT workspace imports still require a target.
- Updates validated binding so targetless SELECT views are source-bound without target rowset validation.
- Updates the offline corpus probe so only split views ending in `_TargetView` receive a target; the target name is derived by dropping `_TargetView` and preserving the configured system prefix.
- Carries forward the `2026.05.29.1` offline corpus probe changes: sparse platform-column ignores, partial binding reports in `TestRuns`, `Mgmt` schema extraction, and DQ only for `Staging`/`DataWarehouse`.

Release metadata:

- `manifest.json`
- `checksums.sha256`
