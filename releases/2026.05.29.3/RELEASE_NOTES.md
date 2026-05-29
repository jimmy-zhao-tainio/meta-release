# 2026.05.29.3

- Framework-dependent Windows x64 packages using shared DLLs.
- Requires the .NET 8 runtime.
- Supersedes `2026.05.29.2` with an explicit offline corpus probe Step 6 for deployment.
- Adds `6-step-deploy-data-quality.ps1`, which deploys `DataQualityViews-Staging.sql` with `STAGING_SQL` and `DataQualityViews-DataWarehouse.sql` with `DATA_WAREHOUSE_SQL`.
- Step 6 uses `meta-sql execute --quiet` and the generated scripts create/update both source-side `dq` views and the idempotent `[MetaDQ]` operational database pack.
- Adds all-in-one probe deployment controls: `-RunDQDeploy`, `RUN_DQ_DEPLOY`, `DqDeployTimeoutSeconds`, and `DQ_DEPLOY_TIMEOUT_SECONDS`.
- Carries forward the compact DQ inspect output, `_TargetView` target-binding convention, sparse platform-column ignores, partial binding reports in `TestRuns`, `Mgmt` schema extraction, and DQ only for `Staging`/`DataWarehouse`.

Release metadata:

- `manifest.json`
- `checksums.sha256`
