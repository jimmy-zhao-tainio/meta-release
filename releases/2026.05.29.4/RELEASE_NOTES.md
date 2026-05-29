# 2026.05.29.4

- Framework-dependent Windows x64 packages using shared DLLs.
- Requires the .NET 8 runtime.
- Supersedes `2026.05.29.3` with quieter DQ command output and a deployable empty-candidate DQ SQL package.
- `meta-data-quality from-transform-workspace`, `inspect`, and `promote` no longer print success-only `Ok` banners or command-guidance prose.
- `meta-convert data-quality-to-sql` now emits an empty `dq.v_DataQualityReview` plus the idempotent `[MetaDQ]` operational pack when no DQ candidates are promoted.
- Offline corpus probe defaults now ignore sparse platform columns `Audit_ID`, `UpdateAudit_ID`, `RowStartDate`, `RowIsCurrent`, and `IsInferred` during binding when present.
- Offline corpus probe Step 5 now supports `DataQualityWithoutBinding` / `DATA_QUALITY_WITHOUT_BINDING`, defaulting `DataWarehouse` to scan `TransformWS\DataWarehouse` directly without BindingWS filtering.
- Carries forward Step 6 DataQuality deployment, `_TargetView` target-binding convention, partial binding reports in `TestRuns`, `Mgmt` schema extraction, and DQ only for `Staging`/`DataWarehouse`.

Release metadata:

- `manifest.json`
- `checksums.sha256`
