# Land Cover Change 1990 - 2015

## Overview
- A 5-band, 25m raster dataset (LCC1990_2015) documenting land cover change between 1990 and 2015 for the UK.
- Derived from simplified versions of Land Cover Maps 1990 (LCM1990) and 2015 (LCM2015) with a focus on robust change mapping.

## Data product and structure
- Five bands:
  - Band 1: Simplified 1990 classes (6 classes) derived from LCM1990.
  - Band 2: Simplified 2015 classes (6 classes) derived from LCM2015.
  - Band 3: Binary change layer (0 = no change, 1 = change).
  - Band 4: 'Change from' class (0-6) indicating 1990 class before change.
  - Band 5: 'Change to' class (0-6) indicating 2015 class after change.
- Two principal usage modes:
  - Bands 1-2 provide full UK coverage (for modeling inputs and analyzing overall change).
  - Bands 3-5 provide partial coverage focused on areas where change occurred (quantifying locations, areas, and types of change).
- Six simplified classes (Band 1/2 mapping; see Table 2):
  - 1: Woodland
  - 2: Arable
  - 3: Grassland
  - 4: Water (Freshwater)
  - 5: Built-up areas
  - 6: Other
- Bands 4-5 map changes using the same six-class scheme (0-6 values corresponding to the six classes).

## Class mapping and aggregation
- Aggregated from the original 21 LCM classes to 6 simplified classes to improve change accuracy (Table 3 mappings).
- Six classes align with LULUCF needs for Greenhouse Gas Inventory reporting.
- Cited LCM1990 and LCM2015 as parcel-based maps created with consistent methods to enable reliable change detection.

## Corrections and data quality adjustments
- Corrections applied to bands 3-5 (and reflected in bands 1-2 for modeling consistency):
  - Inter-tidal areas: Excluded changes between water/inter-tidal classes to avoid false positives.
  - Rock/non-rock changes above 600m: Excluded using NextMAP DEM due to higher spectral variability and snow cover affecting accuracy.
  - River fragments and water bodies: False positives in water change removal by cross-referencing known river networks and masking erroneous changes.
- These corrections help ensure change signals reflect real land cover changes rather than classification artifacts.

## Derivation and purpose
- LCM1990 and LCM2015 were originally classified into 21 classes; these were re-cast into 6 aggregated classes to improve accuracy and reliability of detected changes.
- The dataset supports Land-Use and Land Cover Change and Forestry (LULUCF) tracking for greenhouse gas inventories.

## Citation and DOIs
- Each Land Cover Change product has a DOI for repeatable citation (GB and NI versions).
- GB 25m raster DOI and NI 25m raster DOI provided; include authors and year in-text with full DOI in references.
- Guidance available on data citation at the CEH data portal.

## Quality assurance
- Generated using defined scripts and experienced staff.
- QA checks include projection validation, spatial completeness, band verification, pixel size checks, and conformity to Table 3.
- Full validation performed against other datasets (e.g., UK Countryside Survey, National Forest Inventory); results to be published separately.

## Access and metadata
- Available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Separate data sets for Great Britain and Northern Ireland due to different projections.
- Technical details:
  - Pixel size: 25 m (both GB and NI).
  - GB: 28,000 columns × 52,000 rows; NI: 7,600 columns × 6,400 rows.
  - Lower-left origins and coordinate systems:
    - GB: British National Grid, EPSG 27700.
    - NI: Irish Grid (TM75), EPSG 29903.
  - Data type: unsigned 8-bit GeoTIFF, uncompressed.
- Queries: spatialdata@ceh.ac.uk
- Note: A journal paper is in preparation; a separate publication will report validation results.

## Availability and acknowledgements
- Acknowledged support from NERC NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability.
- References and DOIs for related LCM products and background materials are provided in the documentation.

## Practical notes for GIS specialists
- Use bands 1-2 for full-coverage modeling of 1990 and 2015 states; derive change by comparing these bands.
- Use bands 3-5 to focus analyses on where and how changes occurred (locations, extents, and transition types).
- Leverage the six-class schema and the 21→6 mapping to integrate with other UK land cover datasets and LULUCF workflows.
- Consider the corrections applied when interpreting change results, especially in inter-tidal zones, high-elevation rock areas, and river networks.