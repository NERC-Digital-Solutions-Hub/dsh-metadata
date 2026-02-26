# 25m raster

## Overview
- Describes a 25-meter resolution raster dataset created by converting land parcels into a 25m grid and recording the dominant land cover using LCM2000 Subclasses.
- Includes details of both 25m and 1km rasters for Great Britain and Northern Ireland, with information on how the rasters were produced and how to interpret the codes.

## 25m raster details
- Spatial setup: Great Britain grid 24400 columns × 48400 rows; Northern Ireland grid 7600 × 7200.
- Extents and origins: specified lower-left easting/northing values for each region; pixel size of 25 m.
- Coordinate systems and datums: Great Britain uses British National Grid (OSGB 1936) with Transverse Mercator projection and Airy spheroid; Northern Ireland uses Irish National Grid (Ireland 1965) with Transverse Mercator projection and Airy Modified 1849 spheroid.
- Pixel center reference: to obtain pixel centers, add 12.5 m to the lower-left corner values.
- Coding and storage: LCM2000 Subclass codes (originally floating point) are multiplied by 10 and stored as unsigned 8-bit bytes (0–255). Example: Water (inland) Subclass 22.1 is stored as 221.

## 1km raster
- Created by summarising the 25m raster within 1km grid cells.
- Spatial setup: Great Britain 700 columns × 1300 rows; Northern Ireland 500 × 500.
- Pixel size and extents: 1000 m pixel size; same coordinate systems and datums as the 25m rasters.
- Pixel center reference: add 500 m to the lower-left values to obtain pixel centers.

## Subclass to Aggregate mapping
- The 25m data can be summarized in two ways: by LCM2000 Subclass or by LCM2000 Aggregate class.
- Table 3 provides the correspondence between Subclasses and Aggregate classes and includes attribute codes for each land cover category.
- The document shows the mapping for both 25m and 1km codes, demonstrating how fine-scale classes translate to coarser classes used in summaries.

## Data encoding and storage efficiency
- To optimise storage in raster format, Subclass codes are scaled (multiplied by 10) to convert floating point values (with one decimal place) into integers (0–255).

## Practical implications for monitoring frameworks
- Enables detailed (25m) and broader (1km) land cover analyses across Great Britain and Northern Ireland, suitable for policy scrutiny, trend detection, and informing future decisions.
- The explicit crosswalk between Subclass, 1km codes, and Aggregate class codes supports multi-scale reporting and integration with other datasets.
- Requires careful handling of metadata and documentation to ensure correct interpretation of codes, extents, and coordinate systems.

## Metadata and governance considerations
- The document provides extensive metadata: grid dimensions, lower-left coordinates, pixel sizes, coordinate systems, projections, spheriods, datums, and notes on pixel center calculations.
- For monitoring teams, this underscores the importance of clear metadata, reproducibility, data lineage, and alignment across GB and NI datasets.
- Encoding choices (8-bit storage via scaling) highlight the need for documentation on data encoding practices and their implications for interoperability and data sharing.

## Challenges and considerations for authors of monitoring frameworks
- Cross-border consistency: ensuring harmonised coordinate systems, datums, and classification schemes between Great Britain and Northern Ireland.
- Metadata completeness: maintaining thorough, accessible metadata to enable quality assurance, verification, and reuse.
- Data transformation: handling the required transformation steps (e.g., 25m to 1km summaries, code scaling) with transparent methods.
- Data governance: establishing open access, versioning, and data management standards to support governance processes and stakeholder scrutiny.