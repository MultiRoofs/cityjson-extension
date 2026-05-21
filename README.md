# CityJSON Extension for the MultiRoofs project

Version **0.2.0** — [CHANGELOG](./CHANGELOG.md)

The [CityJSON Extension](https://www.cityjson.org/extensions/) is defined in [multiroofs.ext.json](./multiroofs.ext.json).

## Attributes

Attributes are split into two categories:

1. **Geometric** — attributes computed from the 3D geometries (roof elevation, area, gradient, azimuth, volume, solar, etc.)  
   → [`attributes/geometric.md`](./attributes/geometric.md)

2. **Extra** — non-geometric attributes per building and per neighbourhood (function, type, ownership, energy label, monument status, zoning, etc.)  
   → [`attributes/extra.md`](./attributes/extra.md)

## Examples

- [`output_roofer.city.jsonl`](./examples/output_roofer.city.jsonl) — raw roofer output
- [`output_roofer_mr.city.jsonl`](./examples/output_roofer_mr.city.jsonl) — multiroofed version

## Roofer configuration

Pre-configured [roofer](https://github.com/LeoStuckardt/roofer) settings are in [`roofer-config/`](./roofer-config).
