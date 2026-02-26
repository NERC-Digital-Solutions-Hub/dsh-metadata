# The UKCEH Land Cover Map for 2023

- LCM2023 is the eleventh UK land cover map produced by UKCEH, built from 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
- It comprises seven datasets split between Great Britain (GB) and Northern Ireland (NI): three products per region (10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster product covering both GB and NI.
- The guide describes data production, validation, accuracy, and guidance for informed use, with ongoing aims to improve temporal consistency, change detection, and data accessibility.

## Data products ( LCMap 2023 product suite )

- 10 m Classified Pixel datasets
  - Generated from classification Scenes; each pixel has a most-likely UKCEH Land Cover Class and an associated confidence/probability.
  - GB: two-band product (class, confidence). NI: similar structure (two to three bands depending on product).
  - Preserves fine landscape detail (no generalisation by Land Parcel Spatial Framework) to capture narrow features.
- Land Parcel datasets
  - Derived by intersecting the 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
  - Parcels have a minimum area (~0.5 ha) and are designed to represent discrete real-world units (fields, parks, urban blocks, etc.).
- 25 m Rasterised Land Parcel datasets
  - Rasterised version of land parcels (GB and NI) at 25 m resolution with three bands: dominant land cover (mode), classification confidence (conf), and parcel purity (purity).
- 1 km raster products
  - Summary products summarising the 25 m raster to 1 km resolution:
    - Dominant cover at 1 km (for both classes and aggregates)
    - Percentage cover at 1 km (21 class bands; 10 aggregate bands)
  - Integer-valued percentages; coastal areas may sum to less than 100 due to coastal extents.

## How the data are produced

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 surface reflectance, resampled to 10 m.
  - Four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10 Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 8A, 11, 12).
  - Occasional gaps due to cloud are handled; classification tolerates partially complete spectral information.
- Context Rasters
  - 10 m context layers to reduce spectral confusion (GB: height, aspect, slope; distances to buildings/roads/tidal water/freshwater; foreshore, woodland, saltmarsh masks).
  - NI: height, aspect, slope; urban mask; distances to coast/roads/freshwater; foreshore and tidal water masks.
- Classification Scenes and Grid
  - GB is divided into 32 Classification Scenes (~100 x 100 km tiles); NI uses a single Scene defined by its bounding rectangle.
  - Each Scene is trained and classified independently; occasional overlap at tile boundaries is normal.
- Bootstrap Training
  - An automatic training approach that uses historic LCM data (LCMs of 2020–2022) to train the classifier, reducing reliance on field data.
  - Pixels with >80% probability and consistent class across three years are used as training data for Bootstrap Training.
  - Crop rotations (e.g., arable to improved grassland) may limit Bootstrap Training effectiveness for some classes.
- Random Forest Classification
  - Balanced training by drawing 10,000 samples per class with replacement.
  - Custom UKCEH software integrates WEKA, PostGIS, and GDAL.
- Validation
  - 33,107 reference points across all 21 classes; overall accuracy reported at 83%.
  - Validation combines GB countryside survey data, open data inventories, and bespoke validation points.

## UKCEH Land Cover Classes and BAP relationships

- 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not identical; some differences exist due to intended field-based vs. remote-sensing mapping.
- Appendices provide explicit mappings and nuanced notes (e.g., how Broad Habitat names relate to UKCEH classes like Deciduous woodland, Coniferous woodland, Arable, Various Grassland types, Urban/Suburban, Saltwater/Freshwater, and coastal/marine habitats).
- The guide clarifies how certain classes align (or differ) with BAP categories, including where multiple BAP Broad Habitats map to a single UKCEH Land Cover Class (e.g., Freshwater) or where splits occur (e.g., Heather vs. Heather grassland).

## Data quality, validation, and known issues

- Validation
  - Overall accuracy: 83% across 21 classes (as of LCM2023 formal validation).
- Known issues
  - A small number of polygons missing from vector land parcel products, causing nodata gaps in the 25 m rasterised parcels; negligible impact on 1 km summary rasters; 10 m classified pixels datasets are unaffected.
- Note on method changes
  - Annual LCMs use evolving methods; changes between maps may reflect method updates as well as real change.

## Using and citing LCM2023 data

- DOIs and citations are provided for all products (10 m classified pixels GB and NI; 25 m rasterised land parcels GB and NI; land parcels GB/NI; 1 km rasters GB/NI).
- Data are hosted in NERC EDS Environmental Information Data Centre; metadata includes coordinate systems and extents:
  - GB: British National Grid (OSGB 27700)
  - NI: TM75 Irish Grid (29903)
- Acknowledgement of ongoing development: methodology differences between years may introduce nominal changes beyond actual land cover change.

## Appendices and practical details for analysts

- Appendix 1 and 2 provide detailed notes on UKCEH Land Cover Classes and UK BAP Broad Habitats, with guidance on interpretation and potential spectral confusion.
- Appendix 3 lists the full dataset suite and DOIs.
- Appendix 4 presents correspondence matrices (confusion matrices) for classification accuracy across class pairs.
- Appendix 5 and 6 provide colour recipes (including color-blind friendly options) for displaying Land Cover Classes in GIS outputs and visualisation files (e.g., QGIS symbology files: lcm_raster.qml and lcm_raster_cb_friendly.qml).