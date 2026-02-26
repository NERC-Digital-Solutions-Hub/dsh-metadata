# Dataset documentation

## Overview
- Land Cover Change 1990-2015 (LCC1990_2015) is a 5-band, 25m raster dataset designed to map land cover change between 1990 and 2015 across the UK.
- Derived from simplified versions of Land Cover Map 1990 (LCM1990) and Land Cover Map 2015 (LCM2015) to enable robust change detection and support Greenhouse Gas Inventory (LULUCF) reporting.
- Data are provided in two modes to support different analyses: full spatial coverage (bands 1-2) and change-only coverage (bands 3-5).

## Data structure and content
- Band 1: Simplified 1990 classes cast into 6 classes (as per Table 2).
- Band 2: Simplified 2015 classes cast into 6 classes (as per Table 2).
- Band 3: Binary change layer (0 = no change, 1 = change).
- Band 4: Change from class (0-6; only for areas that changed; 0 = no change).
- Band 5: Change to class (0-6; only for areas that changed; 0 = no change).
- The six classes are:
  - Woodland
  - Arable
  - Grassland
  - Water (Freshwater)
  - Built-up areas
  - Other
- Two primary usage modes:
  - Bands 1-2: Full UK coverage; inputs to models to reflect 1990–2015 change.
  - Bands 3-5: Partial coverage showing where change occurred and the specific change types.

## Derivation and class aggregation
- LCM1990 and LCM2015 originally had 21 classes; aggregated to 6 simplified classes to improve mapping accuracy and suitability for LULUCF tracking.
- Corrections applied during derivation (and mirrored in bands 1-5):
  - Inter-tidal areas: exclude changes between water/inter-tidal classes to avoid false positives.
  - Rock/non-rock confusion above 600m: excluded changes using NextMAP DEM due to data quality issues in mountainous areas.
  - River fragments and water bodies: identified and masked to remove false change to water.
- Corrections applied to bands 3-5 (and to band 1 to maintain consistency with bands 3-5).

## Quality assurance and validation
- Defined scripts and methods with QA checks for projections, spatial completeness, band structure, pixel size, and overall product specifications.
- Validation performed against other datasets (e.g., UK CEH Countryside Survey, National Forest Inventory); full validation results to be published separately.

## Data provenance and citation
- The dataset has DOIs for citation to support repeatability and traceability.
- DOIs available for GB and Northern Ireland products; include authors and date in text with full DOI in references.

## Access, metadata, and technical details
- Access: CEH Environmental Information Platform (eip.ceh.ac.uk).
- Separate datasets for Great Britain and Northern Ireland to accommodate different projections:
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish Grid (TM75) (EPSG 29903)
- Pixel size: 25 m for both GB and NI.
- Data dimensions (approximate):
  - Great Britain: 28,000 columns × 52,000 rows
  - Northern Ireland: 7,600 columns × 6,400 rows
- Data format: Uncompressed 8-bit GeoTIFFs.
- Lower-left coordinates and metadata provided; guidance on coordinate references notes that pixel value refers to the southwest corner of the lower-left pixel.
- Queries: spatialdata@ceh.ac.uk
- Acknowledgement: NERC award NE/R016429/1 (UK-SCAPE programme).

## Practical implications for analysts
- Use bands 1-2 for modelling across the UK to estimate 1990–2015 change; use bands 3-5 to quantify and locate actual changes and their nature.
- Be mindful of scale and projection differences between GB and NI datasets when combining or comparing regions.
- When publishing results, cite the corresponding DOIs and include method details for reproducibility.
- Consider data limitations in mountainous areas and coastal/intertidal zones where corrections were applied.

## References and further information
- Core methodology and related datasets:
  - Jackson, D.L. 2000. Guidance on Biodiversity Broad Habitat Classification.
  - Rowland et al. 2017a/b; Rowland et al. 2020a/b for LCM1990/LCM2015 and LCC1990_2015 datasets.
- Data access and citation information:
  - CEH Data DOI references and citation guidance (http://eidc.ceh.ac.uk/citing-data).
- Acknowledgement: UK Natural Environment Research Council (NERC NE/R016429/1).