
# Attributes computed from the 3D geometries

|                                | **who?** |  **units**       | **name**          | **extra info**                    |
|:------------------------------ |:---------|:-----------------|:------------------|:----------------------------------|
| **Ground elevation**           | tudelft  | m                | ground-elevation  | surely useful to know the height of the building (coordinates are wrt CRS, not the ground) |
| **Building height**            | tudelft  | m                | building-height   | (roof-elevation - ground-elevation) |
| **Roof elevation**             | tudelft  | m                | roof-elevation    | which point do we use? median or 70-percentile|
| **Roof total area**            | tudelft  | m^2              | roof-total-area   | total of all RoofSurfaces |
| **Roof compactness**           | tudelft  | (no units)       | roof-compactness  | (rooftop-total-area / rooftop-perimeter) |
| **Roof gradient**              | tudelft  | degree           | roof-gradient     | for each roof segment  |
| **Roof azimuth**               | tudelft  | degree           | roof-azimuth      | for each roof segment, from North CW  |
| **Building mass** (volume)     | tudelft  | m^3              | building-volume   |  |
| **Roof sun hours**             | tudelft  | hours            | roof-sun-hours    | Full day, 21st March |
| **Roof solar irradiance**      | tudelft  | kWh/m2           | roof-irradiance   | Calculated for entire year |
| **Roof view quality**          | tudelft  | degree           | roof-view-quality | Measures number of unobstructed views from center of roof (SVF thus) |
