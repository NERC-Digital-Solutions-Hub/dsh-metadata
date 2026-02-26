# The UKCEH Land Cover Map for 2023

## Overview
- UKCEH LCM2023 is an annual land cover product for the UK, built from seven geospatial datasets (GB and NI): 10 m classified pixels, land parcels (10 m and 25 m), 25 m rasterised land parcels, vector land parcels, and a 1 km summary raster product for GB and NI.
- 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) are mapped; classifications rely on Classification Scenes created from Sentinel-2 Seasonal Composite Images plus Context Rasters.
- Classification uses Bootstrap Training with a Random Forest (RF) algorithm; annual production aims to improve temporal consistency and support change detection.
- Formal validation reports an overall thematic accuracy of 83%.

## Dataset suite and data holdings
- 10 m Classified Pixel datasets (GB and NI): per-pixel class with a second band giving classification confidence.
- 25 m Rasterised Land Parcel datasets (GB and NI): rasterised version of land parcels with three bands: mode (dominant class), conf (confidence), and purity.
- Land Parcel Spatial Framework: fixed 0.5 ha minimum parcel size; parcels generalise national cartography to discrete units (fields, parks, etc.) to reduce noise and enable change detection.
- 1 km Summary Raster products (GB and NI): dominant class per 1 km pixel and percentage cover for both class sets (with rounding).
- Vector Land Parcel product (GB and NI): vector representation of land parcels (gids, attributes).
- Dataset metadata and DOIs are provided for each product; citations available in the document.

## Data structure and attributes
- 10 m Classified Pixels (GB/NI)
  - Band 1: UKCEH Land Cover Class identifier (integer, 1–21)
  - Band 2: Class probability/confidence for the assigned class
- 25 m Rasterised Land Parcels (GB/NI)
  - Band 1: _mode (dominant land cover class for the parcel)
  - Band 2: _conf (mean parcel-level confidence)
  - Band 3: _purity (parcel-level purity)
- 1 km Summary Rasters
  - Dominant class (1 band)
  - Percentage cover per class (21 bands for classes, 10 for aggregates)
- Spatial reference
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish Grid (TM75, EPSG 29903)
- Extents and scale
  - GB NI products cover their respective land masses; GB extents ~0–700000 E, 0–1300000 N (GB); NI extents are defined in Irish Grid
  - Pixel resolutions: 10 m (GB/NI) and 25 m (GB/NI)

## Classification methodology and Bootstrap Training
- Bootstrap Training: uses historic land cover maps (LCM2020–2022) to automatically sample training observations, reducing the need for new field data.
- Training data selection: pixels with >80% probability and consistent class across three years are used to train RF.
- Random Forest: balanced sampling with 10,000 samples per class per bag to avoid dominance by common classes.
- Software stack: bespoke UKCEH tool integrating Weka, PostGIS, and GDAL (open source).

## Seasonal inputs and context rasters
- Seasonal Composite Images: derived from 10-band Sentinel-2 data (bands 2,3,4,5,6,7,8,8A,11,12) at 10 m resolution; four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with potential cloudy gaps.
- Context Rasters (GB and NI) provide terrain and proximity information to improve discrimination:
  - GB: height, aspect, slope; distances to buildings, roads, tidal water, freshwater; foreshore and water/vegetation masks.
  - NI: height, aspect, slope; urban mask; distances to coast, freshwater, roads; foreshore and tidal water masks.

## Classification Scenes and processing
- GB uses a grid of 32 Classification Scenes (~100 x 100 km tiles) to classify the entire GB land surface; scenes trained and classified independently to manage regional variation.
- NI uses a single Classification Scene based on the minimum bounding rectangle of NI landmass (49-band input: 40-band Sentinel-2 Seasonal Composite plus NI Context Rasters).
- Some tile overlaps may occur due to processing extents.

## The UKCEH Land Parcel Spatial Framework
- The Land Parcel Spatial Framework was developed for LCM2007 and updated; identifiers (gid) may differ from LCM2015 for cross-map comparisons.
- MMU and parcel logic: parcels ~0.5 ha minimum; designed to represent discrete land units; parcel-wide dominance of a single land cover type is common but not universal.
- Parcel-based organisation reduces classification noise and supports change detection over time.

## Validation and quality
- Validation: 33,107 reference points across all 21 classes, using GB countryside survey, National Forest Inventory, Rural Payments Agency data, and bespoke points.
- Overall accuracy: 83% for LCM2023 (full thematic detail).
- Appendix 4 provides detailed confusion matrices, user’s and producer’s accuracies per class (illustrating common misclassifications and strengths).

## Known issues and cautions
- A small number of polygons are missing from the vector land parcel products, causing nodata areas in derived 25 m raster parcels; effect on 1 km summaries is negligible.
- The 10 m classified pixel dataset is unaffected by the missing parcels.
- Changes between LCM maps can reflect real land cover change and/or methodological updates; users should account for potential methodology-induced differences when comparing years.

## Citations, DOIs, and usage
- Each dataset has a DOI and recommended citation; reference Marston et al. (2023/2024) for production methods and related products.
- See Table 5 in the document for DOIs and recommended references for each product (10 m classified pixels GB/NI, 25 m rasterised land parcels GB/NI, vector land parcels GB/NI, and 1 km summary rasters).
- Disclaimer: ongoing development may introduce method changes between annual maps, affecting direct year-to-year comparability.

## Appendices: key mappings and visualisation
- Appendix 1 and 2: notes on UKCEH Land Cover Classes and their relationship to Biodiversity Action Plan (BAP) Broad Habitats; guidance on naming conventions (capitalization) and potential spectral confusion.
- Appendix 3: full list of LCM2023 datasets with DOIs and citations.
- Appendix 4: correspondence matrices (confusion matrices) by class pair, including user’s and producer’s accuracies.
- Appendix 5 and 6: recommended colour schemes for displaying UKCEH Land Cover Classes (standard and colour-blind friendly), plus associated QGIS symbology files.