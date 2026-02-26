# Dataset documentation

## Overview
- Land Cover Change 1990 - 2015 is provided as a 5-band, 25m raster dataset. This document introduces key aspects for users and potential users and covers only the Land Cover Change data set (not the Land Cover Maps).

## Product and purpose
- Land Cover Change 1990-2015 (LCC1990_2015) is derived from simplified versions of LCM1990 and LCM2015, created with consistent methods to enable change mapping over 25 years.
- A revised LCM1990 was produced to enable this change dataset.
- The dataset supports greenhouse gas inventory tracking (LULUCF) by providing six simplified land cover classes derived from the original 21 LCM classes.

## Data structure and bands
- 5-band raster (GB and NI provided separately):
  - Band 1: Simplified 1990 classes (6 classes) derived from LCM1990.
  - Band 2: Simplified 2015 classes (6 classes) derived from LCM2015.
  - Band 3: Binary change layer (0 = no change, 1 = change).
  - Band 4: Change from class (0–6) for areas that changed.
  - Band 5: Change to class (0–6) for areas that changed.
- Bands 1-2 provide complete UK coverage for modeling inputs; bands 3-5 map only areas where change occurred.

## Class mapping
- 6 simplified classes (based on aggregation of 21 LCM classes):
  - 1 Woodland
  - 2 Arable
  - 3 Grassland
  - 4 Water (Wetlands)
  - 5 Built-up areas
  - 6 Other
- Table mappings detail how the six classes correspond to the original 21 LCM classes.

## Corrections and quality adjustments
- Corrections applied to avoid false detections in bands 3-5:
  - Inter-tidal areas: water and inter-tidal zones classified differently; changes between these classes excluded from change bands.
  - Rock/non-rock confusion above 600 m: changes between rock and non-rock excluded using NextMAP DEM; reduces errors due to cloud, topography, and snow.
  - River fragments and water bodies: false “change to water” detections masked using known river networks and other water features.
- Corrections applied to bands 3-5 and also applied to band 1 to maintain consistency with the change mapped in bands 3-5.

## Derivation and data lineage
- LCM1990 and LCM2015 were originally 21 classes each and were cast into 6 simplified classes to improve mapping accuracy and support change detection.
- The product is designed to provide robust inputs for modeling and methodological consistency with the LULUCF framework.

## Citation and DOIs
- The Land Cover Change datasets have DOIs to enable clear, repeatable methods and traceable use.
- GB 25m raster DOI: Rowland et al. 2020 (GB) – https://doi.org/10.5285/07b6e5e9-b766-48e5-a28c-5b3e35abecc0
- NI 25m raster DOI: Rowland et al. 2020 (NI) – https://doi.org/10.5285/a747aa7a-c875-42e1-ac31-984f6571f446
- Full citation guidance: include authors and date in text and full DOI in references.

## Quality assurance and validation
- Data are produced using defined scripts and trained staff; series of QA checks ensure:
  - Correct projections and spatial completeness.
  - Correct five bands and pixel sizes.
  - Consistency with the defined data specification.
- A full validation against reference datasets (e.g., Countryside Survey, National Forest Inventory) has been conducted; results will be reported in a separate publication.

## Access, metadata, and contact
- Data access: CEH Environmental Information Platform (eip.ceh.ac.uk).
- Separate data sets for Great Britain and Northern Ireland due to different projections.
  - GB: 25m pixel, 28,000 x 52,000 grid, lower-left easting/northing 1, British National Grid (EPSG 27700).
  - NI: 25m pixel, 7,600 x 6,400 grid, lower-left easting 180,000, lower-left northing 300,000, Irish TM grid (EPSG 29903).
- File format: uncompressed GeoTIFF, 8-bit unsigned.
- Data notes: Pixel value conventions reference Tables 1–5 in the documentation; minor notes about coordinate conventions apply (south-west corner of lower-left pixel).
- Data type note: 8-bit unsigned; compression can substantially reduce file sizes if saved in a compressed format.
- Queries: spatialdata@ceh.ac.uk
- Acknowledgement: NERC award NE/R016429/1 (UK-SCAPE programme, National Capability).

## Data usage and governance notes for Data Stewards
- Clear provenance: derived from LCM1990/LCM2015 with documented corrections; supports traceable data lineage.
- Versioning and updates: changes to corrections and validation workflows are described; datasets are published with DOIs for citation.
- Metadata completeness: includes pixel size, extent, projection, data type, and QA procedures; separate GB/NI datasets with projection-specific details.
- Access controls and usage: guidelines emphasize appropriate use, and data users should cite DOIs and authors as required.
- Practical use: designed for model inputs (full coverage) or targeted change analyses (change-only coverage), suitable for monitoring land cover transitions over 1990–2015.