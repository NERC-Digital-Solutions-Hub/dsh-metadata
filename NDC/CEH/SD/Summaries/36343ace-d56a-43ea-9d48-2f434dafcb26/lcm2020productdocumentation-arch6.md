# The UKCEH Land Cover Map for 2020

- Purpose: User guide for UKCEH Land Cover Map 2020 (LCM2020), detailing six datasets for GB and Northern Ireland, including 10m classified pixels, 25m rasterised land parcels, and land parcel datasets. Describes data production, validation, and data accuracy to help users make informed decisions and enable end-users to explore data.

## Overview of LCM2020

- LCM2020 is the eighth UK land cover map by UKCEH, mapping 21 UKCEH Land Cover Classes tied to Biodiversity Action Plan (BAP) Broad Habitats.
- Creation: Automated classification of Classification Scenes built from Sentinel-2 Seasonal Composite Images plus 10 Context Layers; uses Bootstrap Training and Random Forest.
- Temporal aim: Annual production to distinguish errors from real change; random errors expected to flicker over time, while persistent changes indicate real land-cover change.
- Validation: Appendix 4 reports overall accuracy just over 79% (79.2%).
- Relationship to BAP: 21 classes align with BAP Broad Habitats but are not identical; BAP terms are italicised when used; tables clarify relationships.

## Data Products and Structure

- Three main GB/Northern Ireland geospatial datasets plus related products (six datasets in total):
  - 10m Classified Pixel datasets (GB and NI): classification results with two bands:
    - Band 1: Most likely UKCEH Land Cover Class (integer)
    - Band 2: Probability/confidence for that class
    - Note: No generalisation with the Land Parcel Spatial Framework to preserve detailed features; intended for specialist users.
  - Land Parcel datasets: created by intersecting 10m Classified Pixels with the UKCEH Land Parcel Spatial Framework; provide parcel-level attributes and metadata.
  - 25m Rasterised Land Parcel datasets: per-parcel raster products with three bands:
    - Band 1: Dominant land-cover class (_mode)
    - Band 2: Mean confidence (_conf)
    - Band 3: Parcel purity (_purity)
  - 20m Classified Raster Product (Northern Ireland): NI-specific 20m classified pixels.
  - Additional dataset naming and configuration details are provided in Appendix 5.
- Seasonal Composite Images and Context Rasters:
  - Seasonal Composite Images derived from Sentinel-2 (winter, spring, summer, autumn bands) resampled to 10 m; used to form Classification Scenes.
  - Context Rasters (GB: 10 layers; NI: 7 layers) to reduce spectral confusion (terrain, distance to features, and coastal/flood masks).
- Classification Scenes and Processing:
  - GB uses overlapping 100x100 km tiles to assemble 36-band Classification Scenes; 74 overlapping GB scenes classified independently with manual precedence for final cut.
  - NI uses a single 100x100 km tile per year for a 43-band Classification Scene.
- UKCEH Land Parcel Spatial Framework:
  - Fixed framework with ~0.5 ha MMU; parcels generalised from national maps to reduce detail; gid identifiers have changed since LCM2015, affecting cross-year parcel-based comparisons.
- Bootstrap Training:
  - Fully automated training approach that uses historic LCM observations (2017–2019 for training) to generate training parcels with >99% purity across years.
  - Training set: GB ~941,027 objects; NI ~214,833 objects.
- Random Forest Classification:
  - Balanced training: 10,000 samples per class (with replacement) drawn to train the RF classifier.
  - Implementation combines bespoke UKCEH software with WEKA, PostGIS, and GDAL.

## Production Methodology

- Bootstrap Training: Uses wall-to-wall historic maps to sample current satellite imagery for training; reduces need for field data and supports continuous updates.
- Random Forest: Supervised learning to assign land cover classes; sampling balance prevents dominance by common classes and improves rare-class learning.
- Data Integration: Outputs are generated per Classification Scene and then integrated; emphasis on maintaining detailed 10m information (for specialist use) rather than deterministic parcel-level generalisation.

## Validation, Accuracy and Limitations

- Validation: Compared LCM2020 outputs with countryside survey data (2019–2020), open data (National Forest Inventory, IACS), and bespoke validation points (34715 field-interpreted points).
- Overall accuracy: 79.2% (approx. 79.2%) at full thematic detail (Appendix 4).
- Per-class performance: Varies by class; e.g., some classes show high user/producer accuracies, while others (e.g., Heather grassland, some grassland subclasses) show lower accuracies and notable confusion with related habitats.
- Notes on errors: Most classification errors are random in space/time; annual maps help distinguish true change from random error; no manual region-wide corrections are performed to enable annual production and change detection.

## Practical Guidance for Data Use

- Data suitability: The 10m Classified Pixels are rich in detail and suitable for specialist analysis; the Land Parcel datasets provide stable units for change detection, while 25m rasters offer simplified parcel-level attributes.
- Spatial framework considerations: The Land Parcel Spatial Framework MMU and parcel identifiers differ from previous LCM versions; cross-year parcel ID-based comparisons to LCM2015 may require spatial overlap-based alignment rather than gid-based matching.
- Interpretation and communication: UKCEH Land Cover Classes are distinct from BAP Broad Habitats; when referencing BAP terms, italicise and note differences to avoid confusion.
- Change detection and time series: Annual LCMs support monitoring UK countryside state and change; random errors unlikely to persist year after year, aiding differentiation of real change.

## Appendix Highlights and Dataset Access

- Appendix 4: Detailed validation matrices (confusion matrices) and per-class accuracies; overall accuracy 79.2% with producer’s and user’s accuracy varying by class.
- Appendix 1–2: Notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats, including nuances in class definitions and training considerations.
- Appendix 5: Full list of LCM2020 datasets and names, including:
  - Great Britain: 10m Classified Raster Product; Land Parcel Product; 25m Rasterised Land Parcel Product.
  - Northern Ireland: 20m Classified Raster Product; Land Parcel Product; 25m Rasterised Land Parcel Product.