# Dataset documentation

- This document introduces the Land Cover Change 1990-2015 (LCC1990_2015) 5-band, 25m raster data set, including its production, structure, corrections, quality assurance, and access.

## What the dataset is and its purpose
- 5-band raster dataset (25m) designed to map land cover change in the UK between 1990 and 2015.
- Derived from simplified versions of Land Cover Maps for 1990 (LCM1990) and 2015 (LCM2015) to enable robust change detection.
- Supports two main usage modes:
  - Bands 1 and 2 provide full spatial coverage (GB and NI) for modelling and inputs to analyses.
  - Bands 3–5 provide change-focused information (where change occurred) for dedicated analyses.
- Aids Land-Use, Land Cover Change and Forestry (LULUCF) tracking and greenhouse gas inventory reporting.
- Data are citable via DOIs to support reproducibility.

## Data product and structure
- Five bands:
  - Band 1: Simplified 1990 classes (6 classes)
  - Band 2: Simplified 2015 classes (6 classes)
  - Band 3: Binary change layer (0 = no change, 1 = change)
  - Band 4: Change-from class (0–6; only where change occurred)
  - Band 5: Change-to class (0–6; only where change occurred)
- Band 1 and Band 2 provide complete UK coverage; Bands 3–5 map only areas with detected change.
- Class scheme (bands 1–3) uses six simplified classes:
  - Woodland, Arable, Grassland, Water, Built-up areas, Other
- Band 4 and Band 5 show the specific “from” and “to” classes for changed areas.

## Derivation and class mapping
- LCM1990/LCM2015 were originally 21 classes; aggregated into 6 simplified classes to improve change-mapping accuracy.
- Aggregation aligned with LULUCF tracking needs and biodiversity/broad habitat definitions.
- Tables provide mappings between original LCM classes and the simplified classes (and notes on 21→6 aggregation).

## Corrections applied to the data
- Addressed systematic issues to improve change detection accuracy:
  - Inter-tidal areas: exclude changes between water and inter-tidal classes from bands 3–5.
  - Rock/non-rock confusion above 600 m: exclude potential errors using NextMAP DEM (notably in Scotland).
  - River fragments and water bodies: identified and masked false changes by referencing known river networks and other water bodies.
- Corrections applied to bands 3–5 and to band 1 to maintain consistency with change mapped in bands 3–5.

## Data quality and validation
- Data are produced with defined scripts/methods by trained staff.
- QA checks cover projections, spatial completeness, band integrity, pixel size, and overall compliance with the data specification.
- Full validation against other datasets (e.g., Countryside Survey, National Forest Inventory) performed; results to be published separately.

## Citing and DOIs
- Each Land Cover Change product has a DOI to support repeatability and clear methods.
- GB and NI 25m rasters have distinct DOIs and citations, enabling precise reference in publications.

## Access, metadata, and technical details
- Access via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Separate datasets for Great Britain and Northern Ireland due to different projections:
  - GB: British National Grid (EPSG 27700)
  - NI: TM75 Irish Grid (EPSG 29903)
- Pixel size: 25 m (GB and NI)
- Data formats: uncompressed GeoTIFF, 8-bit unsigned
- Dataset extents:
  - GB: 28,000 columns × 52,000 rows
  - NI: 7,600 columns × 6,400 rows
- Lower-left coordinates and origin conventions specified; notes on pixel-origin definitions for different software packages.
- Data are distributed with documentation, and queries can be directed to spatialdata@ceh.ac.uk.
- A journal article is in preparation to document additional methodological details.

## Practical considerations for Data Leaders
- Use Bands 1–2 for comprehensive, model-ready inputs spanning the UK; use Bands 3–5 for targeted analyses of where and how change occurred.
- Corrections improve change-detection reliability, particularly in inter-tidal zones, high-relief areas, and river/water body contexts.
- DOI-cited data enhances reproducibility in policy and academic work; ensure proper citation in reports.
- The dual-projection setup (GB vs NI) requires attention to coordinate reference systems when integrating with other data sources.
- The data support GHG inventory tracking and broader policy analyses, while QA and validation steps help quantify confidence in change detections.