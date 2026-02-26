# Land Cover Change 1990-2015

## Overview
- Provides a 5-band, 25m raster dataset (LCC1990_2015) for monitoring land cover change between 1990 and 2015 in the UK.
- Designed to support environmental health monitoring, policy scrutiny, and informing future decisions; suitable for input to models and change analysis.
- Two principal use modes: full-coverage inputs for 1990 and 2015 classifications to map overall change; or bands 3-5 for targeted analysis of areas where change occurred.

## Data Structure and Content
- Band 1: Simplified 1990 land cover cast into 6 classes (based on LCM1990).
- Band 2: Simplified 2015 land cover cast into the same 6 classes (based on LCM2015).
- Band 3: Binary change layer (0 = no change, 1 = change between 1990 and 2015).
- Band 4: 'Change from' class (0–6) showing what the area was in 1990 before change.
- Band 5: 'Change to' class (0–6) showing what the area became in 2015 after change.
- The six simplified classes map to: Woodland, Arable, Grassland, Water, Built-up areas, Other.
- The data are available separately for Great Britain and Northern Ireland, both 25m resolution.

## Derivation and Corrections
- Aggregated from original 21 LCM classes to 6 simplified classes to improve change-detection accuracy.
- Corrected known issues before producing change bands, including:
  - Inter-tidal/water classifications to avoid spurious changes.
  - Rock/non-rock confusion over ~600m using altitude data to exclude unreliable changes.
  - River fragments and water body misclassifications; false positives in change-to water were identified and masked.
- Corrections applied consistently across bands 1–5 to maintain model-compatibility.

## Quality Assurance and Validation
- QA checks verify projections, spatial completeness, band integrity, pixel size, and overall conformity to table specifications.
- Validation conducted against independent datasets (e.g., UK CEH Countryside Survey, National Forest Inventory); results planned for publication.
- Dataset creation is script-based and performed by trained staff; full validation supports reliability for monitoring purposes.

## Data Access and Metadata
- Available via the CEH Environmental Information Platform.
- GB and NI datasets provided separately with distinct projections:
  - Great Britain: 25m pixel, 28000 columns × 52000 rows, British National Grid (EPSG 27700).
  - Northern Ireland: 25m pixel, 7600 columns × 6400 rows, Irish Grid (TM75).
- Data distributed as uncompressed 8-bit GeoTIFFs; guidance notes on coordinate references and pixel corner definitions included.
- Metadata includes pixel size, extents, coordinate systems, and data types; contact for queries: spatialdata@ceh.ac.uk.
- Digital Object Identifiers (DOIs) are provided for citation (GB and NI products) to support reproducibility.

## Citation and Use in Policy Monitoring
- DOIs enable precise citation and reproducibility in scientific and policy documents.
- Encourages clear methods description and understanding of data usage scope and applications.
- Data are suitable for Greenhouse Gas Inventory tracking (LULUCF) and related policy monitoring through standardized class mappings and change analysis.

## Technical Specifications
- Data structure designed for two usage modes:
  - Bands 1-2 provide full UK spatial coverage for modeling and change assessment.
  - Bands 3-5 provide targeted information on areas that changed, useful for location- and area-specific analyses.
- Class mappings align with broader LCM lineage and UK biodiversity/habitat definitions, facilitating integration with other environmental datasets.

## Limitations and Considerations
- While extensive corrections address major error sources, users should be aware of residual uncertainties in complex landscapes (e.g., highly cloudy or topographically variable areas).
- Public sharing of underlying origination data is a consideration addressed through standardized metadata and governance; users should follow citation and data-use guidance.
- Separate datasets for GB and NI require attention to projection differences when integrating across the UK.