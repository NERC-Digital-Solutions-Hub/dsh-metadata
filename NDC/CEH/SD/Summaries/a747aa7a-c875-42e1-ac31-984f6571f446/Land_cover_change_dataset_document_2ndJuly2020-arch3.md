# Land Cover Change 1990-2015

## Overview
- Provides a 5-band, 25m raster dataset capturing land cover change in the UK from 1990 to 2015.
- Built to support environmental monitoring, policy evaluation, and greenhouse gas inventory (LULUCF) tracking.
- Based on simplified classifications derived from the Land Cover Map (LCM) 1990 and 2015 to improve change detection accuracy.

## Data product at a glance
- Two inputs (Bands 1 and 2) map full spatial coverage for 1990 and 2015 using 6 simplified land cover classes.
- A binary change layer (Band 3) indicates whether change occurred (0 = no change, 1 = change).
- Change detail bands (Bands 4 and 5) show the 'change from' and 'change to' classes for areas that changed, with values 0-6.
- Coverage: separate datasets for Great Britain and Northern Ireland, aligned to their respective projections.

## Data structure and classes
- Band 1: Simplified 1990 classes (6 classes)
- Band 2: Simplified 2015 classes (6 classes)
- Band 3: Binary change layer (0 = no change, 1 = change)
- Band 4: 'Change from' class (0-6; only for changing areas)
- Band 5: 'Change to' class (0-6; only for changing areas)
- Table 2 maps simplified classes to underlying LCM equivalents
- Table 3 defines the six aggregate classes used for the change product:
  - Woodland, Arable, Grassland, Water, Built-up areas, Other

## Change detection and corrections
- Corrections applied to mitigate systematic mapping issues:
  - Intertidal and water area changes excluded to avoid erroneous change signals.
  - Rock/non-rock classifications above 600m adjusted using altitude data to reduce false positives in high-relief areas.
  - River fragments and water bodies flagged and false changes removed; consistency ensured across bands 1-5.
- Corrections applied to bands 3-5 and propagated to band 1 to maintain model input consistency.

## Derivation and rationale
- Initial 21 LCM classes were aggregated into 6 simplified classes to improve change-mapping accuracy.
- Aggregation aligns with LULUCF tracking needs and enhances greenhouse gas inventory reporting.
- LCM1990 and LCM2015 were created with consistent methods to enable reliable change mapping.

## Quality assurance and validation
- QA checks cover:
  - Correct projections, spatial completeness, band integrity (5 bands), pixel size, and overall product specification (Table 3).
- Full validation against other datasets (e.g., UK Countryside Survey, National Forest Inventory) conducted; results to be published separately.
- Data are produced by trained staff using defined scripts and methods.

## Data access, formats, and metadata
- Access via CEH Environmental Information Platform (eip.ceh.ac.uk).
- GB and NI provided as separate datasets due to different projections:
  - Pixel size: 25 m for both GB and NI
  - GB grid: 28,000 columns x 52,000 rows; lower-left easting/northing 1; EPSG 27700
  - NI grid: 7,600 columns x 6,400 rows; lower-left easting/northing 1; EPSG 29903
- Data format: uncompressed GeoTIFF, 8-bit unsigned integers
- Notes: describes two usage modes—full-coverage inputs (Bands 1-2) and change-focused analyses (Bands 3-5)
- Data queries: spatialdata@ceh.ac.uk

## Citation, DOIs, and reproducibility
- Each Land Cover Change product has a DOI to enable precise citation and reproducibility (Table 4 in the document).
- Include authors and date in text when citing; provide full DOI in references.
- Example DOIs cover GB and NI 25m rasters (GB: 10.5285/..., NI: 10.5285/...)

## Practical considerations for monitoring frameworks
- Enables monitoring of 1990–2015 land cover transitions and helps quantify changes in key classes (woodland, arable, grassland, water, built-up, other).
- Useful as input to models and as a basis for change-based indicators in policy evaluation.
- Provides transparency through documented corrections, metadata, DOIs, and QA procedures, aiding governance and data provenance.

## Acknowledgement and references
- Supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
- Methodological references include LCM1990/LCM2015 development papers and the Broad Habitat classification framework.