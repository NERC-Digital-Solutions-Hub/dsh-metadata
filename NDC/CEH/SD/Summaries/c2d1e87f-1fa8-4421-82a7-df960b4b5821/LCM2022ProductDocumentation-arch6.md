# The UKCEH Land Cover Map for 2022

- Purpose of the document: User guide for the UKCEH Land Cover Map for 2022 (LCM2022), detailing data production, validation, accuracy, and guidance for informed use.
- Product scope: LCM2022 comprises seven datasets (three per region for Great Britain and Northern Ireland) plus a 1 km summary raster product:
  - 10 m Classified Pixel datasets (GB and NI)
  - Land Parcel datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets (GB and NI)
  - 1 km summary raster data (GB and NI)
- Land Cover classes: 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; classifications derived from Sentinel-2 Seasonal Composite Images plus Context Rasters; classifications produced automatically using Bootstrap Training with Random Forest.
- Annual mapping rationale: Aims to improve temporal consistency, enable change detection, and differentiate random errors from real change; annual maps help monitor UK countryside state and change.

## Data products and structure

- 10 m Classified Pixel datasets
  - Derived from mosaicked Classification Scenes; each pixel has a most likely UKCEH Land Cover Class (band 1) and a probability/confidence score (band 2).
  - No generalisation to Land Parcel Spatial Framework to preserve fine landscape detail (narrow features and small patches may be below 0.5 ha MMU).
  - Validation performed against 25 m rasterised parcels; 10 m pixels carry no official validation against the parcel framework.
- Land Parcel datasets
  - Created by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to produce parcel attributes.
- 25 m Rasterised Land Parcel datasets
  - Rasterised representation of land parcels at 25 m resolution; three bands per parcel: dominant land cover class (mode), confidence (conf), and purity.
- 1 km raster products
  - Summary rasters derived from 25 m data:
    - Dominant cover at 1 km (21-class, 1 band)
    - Dominant cover at 1 km (Aggregate classes, 1 band)
    - Percentage cover at 1 km for 21 classes (21 bands)
    - Percentage cover at 1 km for 10 aggregate classes (10 bands)
  - Note: Percentage values are integers; totals may not sum exactly to 100 due to rounding; near-coast areas may sum to less than 100.
- Classification Scenes
  - GB: 32 tiles (approximately 100 x 100 km each) classified independently; some edge overlaps exist due to processing.
  - NI: Single classification scene covering the whole landmass.
  - In NI, the classification scene uses 40-band Sentinel-2 Seasonal Composite Image plus NI Context Rasters (total 49 bands).
- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 surface reflectance, resampled to 10 m; four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) across 10 bands; occasional cloud-related gaps tolerated by the classifier.
- Context Rasters
  - Used to reduce spectral confusion between land cover types.
  - GB: 10 context rasters including height, aspect, slope, distance to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, saltmarsh mask.
  - NI: 9 context rasters including height, aspect, slope, urban mask, distance to coast/freshwater/road, foreshore mask, tidal water mask.
- Coordinate systems and extents
  - GB: British National Grid, EPSG 27700
  - NI: Irish Grid (TM75), EPSG 29903
- Parcel framework
  - UK Land Parcel Spatial Framework with a ~0.5 ha minimum mapping unit (MMU); parcels represent discrete real-world units (fields, parks, urban areas, etc.) and are used to enhance change detection and provide a fixed analytical structure.

## Production methodology

- Bootstrap Training
  - Automated training data sampling from historic land-cover maps (LCM2019–LCM2021) to train the classifier, reducing the need for fresh field data.
  - Pixels with >80% probability and consistent class across three years are used to form Bootstrap Training data.
  - Balances training by drawing 10,000 samples per class; helps ensure rarer classes are learned.
- Random Forest classification
  - RF classifier uses Bootstrap Training pixels to assign class membership; the highest probability class is chosen for each pixel.
  - Software integrates Weka with PostGIS and GDAL; open-source stack.
- Validation and accuracy
  - 33,107 validation points across the UK, across all 21 classes.
  - Overall accuracy: 86.1% (full thematic detail).
- Known issues and caution
  - Some vector land parcel polygons are missing, causing nodata areas in corresponding 25 m rasterised parcels (negligible effect on 1 km products; 10 m datasets unaffected).
  - Methods evolve over time; comparisons between maps may reflect methodological changes as well as real land-cover change.

## Data specifics and access

- Datasets and DOIs
  - Each LCM2022 dataset has an assigned DOI; see Table 5 in the document for DOIs and citations (e.g., 10 m Classified Pixels GB and NI; 25 m Rasterised Land Parcels GB and NI; Land Parcels GB and NI; 1 km Summary Rasters GB and NI).
  - Recommended to cite Marston et al. (2023) for LCM2021 and Marston et al. (2024a–g) for LCM2022 data products.
- Data usage guidance
  - Output products should be cited with their DOIs; use the 21 UKCEH Land Cover Classes and 10 UKCEH Aggregate Classes consistently.
  - The document provides recommended colour schemes (Appendix 5) and color-blind friendly options (Appendix 6) with corresponding QGIS symbology files (lcm_raster.qml and lcm_raster_cb_friendly.qml).
- Appendix highlights (for users needing deeper detail)
  - Appendix 1: Notes on UKCEH Land Cover Classes (detailed class descriptions and BAP alignment considerations)
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and relationships to UKCEH classes
  - Appendix 3: Full dataset list and DOIs for LCM2022 products
  - Appendix 4: Correspondence matrices (validation results by class; producer and user accuracies)
  - Appendix 5 & 6: Display recommendations (color schemes; color-blind friendly options) and associated QGIS files

## Practical guidance for data use

- When using 10 m Classified Pixels
  - Expect a high level of detail and potential noise in patchy or small features; reference the 25 m rasterised parcels for a coarser, noise-reduced view.
  - Use contextual rasters and seasonal composites to understand spectral drivers behind classifications.
- For change detection and time-series analysis
  - Leverage Bootstrap Training methodology to understand how classifications may evolve year-to-year; annual maps aid in distinguishing real change from method-driven variation.
  - Use the Land Parcel Spatial Framework to align with consistent mapping units (MMU ~0.5 ha) for time-series comparisons.
- For visualization and dissemination
  - Utilize the provided color schemes and QGIS styles (Appendix 5/6) to ensure clear, consistent mapping of the 21 classes and 10 aggregates.
  - Acknowledge potential misclassifications in spectrally similar habitats highlighted in Appendix 1–2 (e.g., arable vs. improved grassland; neutral grassland vs. other grasslands) when interpreting outputs.

## End notes

- The document emphasizes that LCM2022 methods are part of an evolving process; slight methodological differences across years mean some interannual changes may reflect update-driven refinements as much as real land-cover change.
- Users are encouraged to consult the DOIs and cited literature for detailed methodological background and to reference the appropriate datasets when using LCM2022 data in analyses or reports.