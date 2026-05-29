# 2026.05.29.1

- Framework-dependent Windows x64 packages using shared DLLs.
- Requires the .NET 8 runtime.
- Adds sparse binding target-column exclusion with `--ignore-target-columns-if-present`.
- Adds explicit partial binding with `--allow-partial` and TSV diagnostics through `--partial-report`.
- Adds DQ filtering with `--binding-workspace`, scanning only validation-backed transform scripts.
- Updates the offline corpus probe to ignore sparse `UpdateAudit_ID`, run binding in partial mode, write binding skip reports, and generate DQ SQL only from matching validated BindingWS inputs.
- Updates the offline corpus probe to extract `Mgmt`/`KUBMgmt` as a schema-only source, write binding partial reports into `TestRuns`, and run DQ only for `Staging` and `DataWarehouse`.

Release metadata:

- `manifest.json`
- `checksums.sha256`
