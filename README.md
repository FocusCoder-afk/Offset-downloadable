# Offset-downloadable

Distribution payload for the OFFSET loader. Nothing here is built from source —
the loader pulls these files and verifies them against `version.json`.

```
OFFSET.exe        external build
version.json      version + sha256 manifest the loader reads
sounds/           runtime sounds the external loads from its own directory
```

To publish an update, replace `OFFSET.exe`, update `version.json` (bump
`version`, refresh `sha256`, `size` and `updated`), then commit. The loader
picks it up on the next attach.
