# MultiRoofs CityJSON Extension — Agent Guide

## Sources of truth

- **Extension definition**: `multiroofs.ext.json` — single source of truth for all attributes.
- **Attribute docs**: `attributes/geometric.md` (3D-derived) and `attributes/extra.md` (non-geometric) — must stay in sync with `multiroofs.ext.json`.
- **Version**: update both `"version"` in `multiroofs.ext.json` and `CHANGELOG.md`.

## Known gaps (sync needed between extension and tables)

_(none currently — `+colours` is intentionally not documented in markdown tables)_

## CityJSON 2.0 conventions

- Extra attribute keys in the extension JSON (`multiroofs.ext.json`) use a `+` prefix (e.g. `+building-height`). The markdown attribute tables omit this prefix.
- Types follow the `["type", "null"]` pattern (nullable array).
- Enums use `"type": ["string", "null"]` with an `"enum"` array.
- `roof-gradient` and `roof-azimuth` are per-surface attributes (defined on semantic surfaces), not per-building. They belong in `geometric.md` but not in `multiroofs.ext.json`, which only lists per-building extra attributes.

## Roofer integration

- `roofer-config/config_mr.toml` maps roofer output → extension attribute names.
- Run: `roofer -c roofer-config/config_mr.toml`.
- Usage: edit polygon-source, output-directory, and LAS source paths in the TOML before running.

## Validation

Validate a CityJSONSequence file with [cjval](https://github.com/cityjson/cjval):

```
cat examples/output_roofer_mr.city.jsonl | cjval
```

## No build/test/lint tooling

This is a spec-only repo — there are no tests, linters, or build steps.
