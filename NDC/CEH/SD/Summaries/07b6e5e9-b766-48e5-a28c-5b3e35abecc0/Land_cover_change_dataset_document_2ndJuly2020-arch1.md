# Land Cover Change 1990-2015

- A 5-band, 25 m raster dataset documenting land cover change in the UK between 1990 and 2015 (GB and NI provided separately with different projections).
- Designed for modelling inputs and change quantification, supporting greenhouse gas inventories and land-use planning analyses.

## Data Product and Structure

- Bands and meanings:
  - Band 1: Simplified 1990 classes (6 classes)
  - Band 2: Simplified 2015 classes (6 classes)
  - Band 3: Binary change layer (0 = no change, 1 = change)
  - Band 4: 'Change from' class (0–6; what the area was in 1990)
  - Band 5: 'Change to' class (0–6; what the area became in 2015)
- Coverage and use:
  - Bands 1–2 provide complete UK coverage and can be used as inputs to models; the difference between 1990 and 2015 reflects overall change.
  - Bands 3–5 cover only areas where change occurred, enabling analyses of location, extent, and type of changes.
- Class system:
  - Six simplified classes derived from the original 21 LCM classes:
    1) Woodland
    2) Arable
    3) Grassland
    4) Water (Freshwater)
    5) Built-up areas
    6) Other
  - Band 4/5 values (0–6) map to the corresponding LCM classes in the six-class framework (Table 3 mappings).

## Derivation and Methodology

- Based on Land Cover Map (LCM) datasets from 1990 and 2015:
  - LCM1990 and LCM2015 were originally 21-class maps; both were recast into six simplified classes to improve change-detection accuracy.
  - The change product (LCC1990_2015) was created to enable tracking of land-cover transitions for Greenhouse Gas Inventory (LULUCF) purposes.
- Original LCM datasets:
  - Parcel-based UK-wide maps created from satellite data, aligned to consistent methods for reliable change mapping.

## Corrections and Quality Assurance

- Corrections applied to bands 3–5 to reduce common error sources:
  - Inter-tidal and water class confusions: changes between inter-tidal water and freshwater were excluded to avoid false change detection.
  - Rock/non-rock classification above 600 m: adjustments using the NextMAP DEM to reduce errors in high-topography, cloud-prone areas (mainly Scotland).
  - River fragments and false water changes: river networks and other water bodies were used to identify and mask out false changes.
- Consistency: corrections applied to band 1 to maintain alignment with bands 3–5 for model inputs.
- QA and validation:
  - Scripts and structured QA checks ensure projections, completeness, band integrity, pixel sizes, and overall conformity to the product specification.
  - Full validation against other datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately.

## Data Access and Metadata

- Access: CEH Environmental Information Platform (eip.ceh.ac.uk). Separate datasets for Great Britain and Northern Ireland.
- Pixel size: 25 m (GB and NI).
- Dimensions:
  - Great Britain: 28,000 columns × 52,000 rows; lower-left origin easting/northing = 1; coordinates in British National Grid (EPSG 27700).
  - Northern Ireland: 7,600 columns × 6,400 rows; lower-left origin easting/northing = 1; coordinates in Irish Grid (TM75) (EPSG 29903).
- Data type: Unsigned 8-bit GeoTIFF, uncompressed.
- Projections:
  - GB: EPSG 27700 (British National Grid)
  - NI: EPSG 29903 (TM75 Irish Grid)
- Documentation and citing:
  - DOIs provided for both GB and NI Land Cover Change products; guidance on citation included in the dataset documentation.
  - Data queries: spatialdata@ceh.ac.uk
  - A journal paper is in preparation to present additional information.

## Citing and References

- DOIs for Land Cover Change products (GB and NI) and related Land Cover Map datasets are provided for proper citation in publications.
- Key references include:
  - Rowland et al. (2017a, 2017b) for Land Cover Map 2015 (GB and NI)
  - Rowland et al. (2020a, 2020b) for Land Cover Map 1990 (GB and NI)
  - Jackson (2000) – Biodiversity Broad Habitat classifications
- Data use notes emphasize including author/date and DOI in citations.

## Practical Use and Applications

- Modelling and analysis:
  - Use bands 1 and 2 as inputs to change-detection or land-use models; band 3 indicates where changes occurred; bands 4 and 5 identify the nature of those changes.
- Reporting and inventories:
  - Data support Greenhouse Gas Inventory (LULUCF) tracking and related land-use reporting.
- Accessibility and interoperability:
  - Data are designed to be machine-readable with metadata and will be discoverable via data portals; intended to be linked with other datasets through standardized classifications.

## Acknowledgements

- Funded by the Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE programme delivering National Capability.