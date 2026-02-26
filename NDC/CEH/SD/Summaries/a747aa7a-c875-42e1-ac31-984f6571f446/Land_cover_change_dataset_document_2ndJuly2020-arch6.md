# Dataset documentation

## Overview
- Land Cover Change 1990-2015 is provided as a 5-band, 25m raster data set.
- Produced from simplified versions of Land Cover Maps for 1990 and 2015 to enable 25-year change mapping.
- Two main use modes: (1) bands 1 and 2 as inputs to models to reflect changes between 1990 and 2015, (2) bands 3–5 for areas where change occurred, useful for quantifying change locations and types.
- Supports Greenhouse Gas Inventory (LULUCF) tracking and broader data-support needs.

## Data product and bands
- Band 1: Simplified 1990 class data (6 classes) derived from LCM1990.
- Band 2: Simplified 2015 class data (6 classes) derived from LCM2015.
- Band 3: Binary change layer (0 = no change, 1 = change).
- Band 4: Change from class (0–6) for areas that changed (what the area was in 1990).
- Band 5: Change to class (0–6) for areas that changed (what the area became in 2015).
- Coverage: Bands 1 and 2 provide complete spatial coverage of the UK; bands 3–5 provide partial coverage for changed areas only.
- Classes (6 simplified): Woodland, Arable, Grassland, Water (Freshwater), Built-up areas, Other.

## Class mapping and derivation
- Original data converted from 21 LCM classes to 6 simplified classes to improve change accuracy.
- Aggregation designed to support LULUCF tracking and related reporting.
- LCM1990 and LCM2015 are parcel-based maps created from satellite data; 6-class scheme aligns with these products for change analysis.

## Data corrections
- Inter-tidal and water classification corrections to avoid false change detections.
- Rock/non-rock confusion above 600m corrected using NextMAP DEM data.
- River fragments and misclassified water bodies identified and masked to reduce false positives.
- Corrections applied to bands 3–5; band 1 adjusted for consistency with the change mapping.

## Applications and use-cases
- Use bands 1 and 2 as model inputs to analyze 1990–2015 change.
- Use bands 3–5 to quantify areas and types of change, including location and transition states.
- Suitable for policy support, environmental reporting, and broader data products (e.g., dashboards or self-serve analyses).

## Derivation and data lineage
- LCM1990 and LCM2015 originally comprised 21 classes; reclassified to 6 simplified classes to improve accuracy of detected changes.
- Change product designed to support UK-wide and regional (GB and NI) analyses; 25m pixel resolution enables cross-dataset compatibility and GHGI reporting.

## Data access, formats, and metadata
- Availability: CEH Environmental Information Platform (eip.ceh.ac.uk); GB and Northern Ireland provided as separate datasets with different projections.
- Pixel size: 25m (GB and NI); Dimensions: GB ~ 28,000 x 52,000; NI ~ 7,600 x 6,400.
- Georeferencing: GB – British National Grid (EPSG 27700); NI – TM75 Irish Grid (EPSG 29903).
- Data format: Uncompressed 8-bit GeoTIFF; unsigned integers.
- File positioning: Lower-left pixel corner referenced; some file size reductions possible with compression.
- Documentation includes tables for band structure, class mappings, and DOIs; see Table 4 for DOIs and Table 5 for metadata details.

## Citation, DOIs, and QA
- Each Land Cover Change product has a DOI for citation to enable reproducibility.
- Recommended citation includes authors and date with full DOI in references.
- Quality Assurance: scripted, expert-validated processes; checks for projection, completeness, band integrity, pixel size, and adherence to specifications.
- Validation performed against other datasets (e.g., Countryside Survey, National Forest Inventory); full validation results to be published separately.

## Access, contact, and acknowledgements
- Access: spatialdata@ceh.ac.uk for queries; a journal paper with additional information is in preparation.
- Acknowledgement: Supported by NERC award NE/R016429/1 (UK-SCAPE National Capability).

## References
- Includes foundational works on LCM1990/LCM2015 and related datasets; DOI-based references provided for data products and related mappings.