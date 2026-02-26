# The UKCEH Land Cover Map for 2021

## Overview
- LCM2021 is the ninth UK land cover map by UKCEH, delivering 21 UKCEH Land Cover Classes derived from a year-long, automatically classified product.
- Built from Sentinel-2 Seasonal Composite Images (4 seasons) plus 10 Context Raster layers to reduce spectral confusion.
- Classification uses Bootstrap Training with a Random Forest classifier, enabling annual updates and improved change detection.
- Formal validation shows an overall accuracy of 82.6% (95% CI 82.19%–82.99%), supporting use for state-and-change monitoring.

## What LCM2021 comprises
- Six geospatial datasets for GB and Northern Ireland (three per region):
  - 10 m Classified Pixel dataset
  - UKCEH Land Parcel Spatial Framework aligned dataset (Land Parcel dataset)
  - 25 m Rasterised Land Parcel dataset
- Additional 1 km summary rasters (GB and NI) providing dominant class and percentage cover across 1 km pixels.
- Datasets are provided in multiple resolutions and formats to support detailed analysis and change detection.

## Data production and structure
- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 data resampled to 10 m, with four seasons: Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec.
  - 50-band inputs (GB) or 49-band (NI) per Classification Scene; occasional data gaps are accommodated by the classifier.
- Context Rasters
  - GB: 10 m rasters for height, aspect, slope, distance to buildings, roads, sea, freshwater, foreshore mask, tidal water mask, woodland mask.
  - NI: 10 m rasters for height, aspect, slope, urban mask, distance to coast, freshwater, roads, foreshore mask, tidal water mask.
- Classification Scenes
  - GB: grid tiles (modified OS 100 x 100 km tiles) used to create 32 Classification Scenes covering GB land surface.
  - NI: a single 49-band Classification Scene for the Northern Ireland land mass.
- Bootstrap Training
  - Training data drawn automatically from historic LCM maps (LCM2018–LCM2020) with >80% purity and consistent class across three years.
  - Enables large, wall-to-wall training data without new field collection; supports balanced learning across classes.
- Random Forest
  - Pixel-level classification (10 m) producing two bands: class ID and associated confidence/probability.
  - Training and classification implemented with UKCEH-in-house software integrating Weka, PostGIS, and GDAL.

## UKCEH Land Parcel Spatial Framework
- Land Parcels are geometric units (~0.5 ha minimum, the MMU) derived from generalized national cartography to reduce noise and enable stable change detection.
- Parcel identifiers (gid) differ from LCM2015; spatial overlap comparisons across years may not align by gid.
- Parcels provide structured, repeatable units for reporting land cover composition within each parcel.

## Product details and formats
- 10 m Classified Pixel dataset (GB and NI)
  - Band 1: most likely UKCEH Land Cover Class id
  - Band 2: class membership probability/confidence
  - Not generalized by Land Parcel framework to preserve fine landscape detail
- 25 m Rasterised Land Parcel dataset (GB and NI)
  - 3-band raster: dominant land cover (mode), mean confidence (conf), and parcel purity (purity)
- Land Parcel Product (GB and NI)
  - Attribute table with parcel-level data, including histograms, mode, confidence, purity, and aggregation
- 1 km Summary Rasters
  - Dominant class (1-band) and percentage cover (21 bands for classes; 10 bands for aggregates)
  - Percentage values are integer-rounded; coastal areas may sum to less than 100 due to mapping resolution
- Coordinate systems
  - GB: British National Grid (EPSG 27700)
  - NI: Irish Grid TM75 (EPSG 29903)
- Dataset scale specifics
  - 10 m pixel resolution for classified rasters
  - 25 m rasterised parcel products
  - 1 km summary rasters across GB and NI
- Datasets listed in Appendix 3; official dataset naming and metadata provided with the product
- Visualisation
  - Appendix 5/6 provide recommended colour recipes (including color-blind friendly options) for displaying UKCEH Land Cover Classes

## Validation, accuracy, and interpretation
- Validation dataset: 35,182 points across all 21 classes, sourced from GB countryside survey, National Forest Inventory, Rural Payment Agency, and bespoke validation points.
- Overall accuracy: 82.6% (95% CI 82.19%–82.99%).
- Validation targeted against the 25 m rasterised land parcel dataset; the 10 m pixel classifications were not part of the validation baseline.
- Appendix 4 provides detailed confusion matrices and producer/user accuracy by class.

## Use considerations and guidance
- LCM2021 advances annual land cover mapping, enabling robust detection of real land cover change versus random error.
- The 10 m Classified Pixels retain high detail but come with higher classification noise risk; users should be aware of this when interpreting small or rare classes.
- Bootstrap Training relies on historic maps for training data; technique aims to maintain consistency across years while allowing updates.
- The relationship between UKCEH Land Cover Classes and UK BAP Broad Habitats is close but not identical; clarity is provided in Appendices 1–2 to reduce ambiguity.
- For cross-year comparisons, note that land parcel identifiers may not match exactly due to updates in the Land Parcel Spatial Framework.

## Appendices and additional resources
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitat mappings
- Appendix 3: Full list of LCM2021 datasets and dataset details
- Appendix 4: Correspondence matrices / confusion matrices (class-by-class accuracy metrics)
- Appendix 5–6: Recommended colour schemes for displaying UKCEH Land Cover Classes (including color-blind friendly options)
- Glossary and terminology clarifications (Bootstrap Training, Context Raster, Classification Scene, Seasonal Composite Image, etc.) present in the document for user clarity