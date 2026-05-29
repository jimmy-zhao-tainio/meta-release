# meta release

Public distribution repository for signed-off `meta` and `meta-bi` release artifacts.

## Current release

Version: `2026.05.29.1`

Packages are published on the GitHub release page as framework-dependent Windows x64 zip files.
They use shared DLLs and require the .NET 8 runtime to be installed on the target machine.

## Verify a package

1. Download the zip and `checksums.sha256` from the same release.
2. Run:

```powershell
Get-FileHash -Algorithm SHA256 .\package-name.zip
```

3. Compare the hash with `checksums.sha256`.

## Runtime check

After extracting a package, run any CLI with `--version`:

```powershell
.\payload\meta\bin\meta.exe --version
.\payload\meta-bi\bin\meta-transform-script.exe --version
```
