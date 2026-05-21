
# Attributes computed from the 3D geometries

| |                                | **who?** | **mandatory?**  |  **units**       | **name**          | **extra info**                    |
|-|:------------------------------ |:--------:|:---------------:|:----------------:|:------------------|:----------------------------------|
| | **Roof total area**            | tudelft  | yes             | m^2              | roof-total-area   | total of all RoofSurfaces |
| | **Roof elevation**             | tudelft  | yes             | m                | roof-elevation    | which point do we use? median or 70-percentile|
| | **Roof compactness**           | tudelft  | yes             | (no units)       | roof-compactness  | (rooftop-total-area / rooftop-perimeter) |
| | **Roof gradient**              | tudelft  | yes             | degree           | roof-gradient     | for each roof segment  |
| | **Roof azimuth**               | tudelft  | yes             | degree           | roof-azimuth      | for each roof segment, from North CW  |
| | **Building mass** (volume)     | tudelft  | yes             | m^3              | building-volume   |  |
| | **Roof sun hours**             | mvrdv    | yes             | hours            | roof-sun-hours    | Full day, 21st March |
| | **Roof solar irradiance**      | mvrdv    | yes             | kWh/m2           | roof-irradiance   | Calculated for entire year |
| | **Roof view quality**          | mvrdv    | yes             | degree           | roof-view-quality | internally generated from 3d model. measures number of unobstructed views from center of roof (SVF) |
| | **Ground elevation**           | tudelft  | yes             | m                | ground-elevation  | surely useful to know the height of the building (coordinates are wrt CRS, not the ground) |
| | **Building height**            | tudelft  | yes             | m                | building-height   | (roof-elevation - ground-elevation) |
