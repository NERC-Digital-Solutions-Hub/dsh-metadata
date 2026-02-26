# Land Cover Change 1990 - 2015

- A 5-band, 25m raster data set (LCC1990_2015) produced from simplified versions of LCM1990 and LCM2015 to map land cover change over 1990–2015.
- Two primary use modes:
  - Bands 1 and 2 provide complete UK coverage for modeling inputs; the difference between 1990 and 2015 reflects change.
  - Bands 3–5 map areas where change occurred only, enabling analysis of change locations and types.

## Data structure and bands

- Band 1: Simplified 1990 classes (6 classes, based on LCM1990 cast into simplified categories).
- Band 2: Simplified 2015 classes (6 classes, based on LCM2015 cast into simplified categories).
- Band 3: Binary change layer (0 = no change, 1 = change).
- Band 4: 'Change from' class (0–6; what the area was in 1990 before change).
- Band 5: 'Change to' class (0–6; what the area was in 2015 after change).
- The 6 simplified classes are Woodland, Arable, Grassland, Water, Built-up areas, Other (mapped from 21 original LCM classes).

## Class mapping and purpose

- Table 3 maps the 6 simplified classes to equivalent LCM classes for cross-compatibility.
- Designed to support Greenhouse Gas Inventory tracking (LULUCF) and model inputs with higher confidence in detected changes.

## Corrections and quality adjustments

- Inter-tidal areas corrected to avoid false change detections; water and inter-tidal zones handled to reduce confusion between freshwater and saltwater.
- Rock/non-rock changes above 600m excluded using NextMAP DEM to mitigate spectral variability and snow cover effects (primarily Scotland).
- River fragments and false water-change detections identified and masked using known river networks and other water bodies.
- Corrections applied to bands 3–5 and also aligned with bands 1–2 for modeling consistency.

## Derivation and methodology

- LCM1990 and LCM2015 originally consisted of 21 classes; aggregated to 6 simplified classes to improve change-mapping accuracy.
- The aggregation supports the change product and aligns with UK biodiversity habitat definitions (Broad Habitat classifications).

## Data access, projections, and metadata

- Available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Great Britain and Northern Ireland provided as separate data sets with different projections:
  - Great Britain: 25m pixels; 28,000 columns × 52,000 rows; lower-left easting 1, northing 1; pixel size 25 m; data type unsigned 8-bit GeoTIFF; CRS EPSG 27700 (British National Grid).
  - Northern Ireland: 25m pixels; 7,600 columns × 6,400 rows; lower-left easting 1, northing 1; pixel size 25 m; data type unsigned 8-bit GeoTIFF; CRS EPSG 29903 (TM75 Irish Grid).
- File notes: uncompressed GeoTIFFs; values refer to the south-west corner of the lower-left pixel.
- DOI-cited references for citation and methods (GB and NI DOIs provided); include author/date in-text and full DOI in references.

## Quality assurance and validation

- QA checks on projections, spatial completeness, band integrity, pixel sizes, and overall specification adherence.
- Validation performed against external datasets (e.g., UK CEH Countryside Survey, National Forest Inventory); results to be reported in a separate publication.

## Usage considerations and guidance

- For modeling and change analysis, use Bands 1 and 2 to assess overall change between 1990 and 2015.
- For targeted change analysis, use Bands 3–5 to identify and categorize where and how changes occurred (change from and change to).
- Ensure consistency when combining GB and NI datasets due to different projections; reproject as needed.
- Reference the DOIs when publishing results to enable reproducibility.

## Documentation, citations, and contact

- DOIs provided for both GB and NI Land Cover Change products; include author and date in-text citations and full DOI in references.
- Data and support queries: spatialdata@ceh.ac.uk
- Acknowledgement: NERC ENvironmental Research Council support under grant NE/R016429/1 (UK-SCAPE).