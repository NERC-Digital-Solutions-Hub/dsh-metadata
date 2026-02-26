# The UKCEH Land Cover Map for 2022

## Overview
- LCM2022 is the tenth UK land cover map produced by UKCEH, mapping 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
- Built from Classification Scenes combining Sentinel-2 Seasonal Composite Images with Context Rasters to produce automatic land cover classifications using Bootstrap Training and a Random Forest classifier.
- Annual production aims to improve temporal consistency, enable change detection, and differentiate real changes from classification error (random errors should flicker over time).
- Formal validation reports an overall accuracy of 86.1%.

## Datasets and product suite
- 10 m Classified Pixel datasets
  - Great Britain (GB) and Northern Ireland (NI) classifications; first band = most likely UKCEH Land Cover Class, second band = probability/confidence.
- Land Parcel datasets (10 m pixels)
  - GB and NI: land parcels created by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
- 25 m Rasterised Land Parcel datasets
  - GB and NI: rasterised parcels with three bands per parcel: dominant land cover (_mode), confidence (_conf), and purity (_purity); includes parcel-level attributes.
- 1 km Raster Summary products
  - GB and NI: dominant cover and percentage cover per 1 km pixel (two sets: 21 class bands and 10 aggregate bands); values are rounded and totals may deviate from 100 due to rounding and coastal extents.
- Classification Scenes and Seasonal Data
  - GB is classified in 32 tiles (100 x 100 km); NI uses a single 49-band Classification Scene (from a 40-band Sentinel-2 Seasonal Composite plus NI context rasters).
- Spatial framework
  - UK Land Parcel Spatial Framework with a minimum mapping unit of ~0.5 ha; parcels are designed to represent discrete real-world units and help reduce noise and support change detection.

## Data production and structure (key methods)
- Seasonal Composite Images
  - Derived from Google Earth Engine; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) using 10 Sentinel-2 bands; occasional gaps are tolerated and classifications handle partially complete spectral information.
- Context Rasters
  - Great Britain: height, aspect, slope; distance to buildings, roads, tidal water, freshwater; foreshore and binary masks for woodland and saltmarsh.
  - Northern Ireland: height, aspect, slope; urban mask; distance to coast, freshwater, roads; foreshore and binary masks.
- Classification Scenes
  - GB: 32 scenes; NI: single scene; combines 49-band inputs (Seasonal + Context) for classification.
- Bootstrap Training
  - Auto-generated training data from historic LCMs (LCM2019–LCM2021) with >80% probability and consistency across three years; reduces need for fresh field data.
- Random Forest classifier
  - Balanced learning with 10,000 samples per class bag; uses Weka, PostGIS, and GDAL in a bespoke pipeline.
- Data interpretation notes
  - The 10 m classified pixels preserve fine features (e.g., small patches) not present in the 25 m parcel products; validation for 10 m pixels is not the same as for 25 m parcels.

## Class mapping and guidance
- UKCEH Land Cover Classes (21 classes) are related to but not identical to UK BAP Broad Habitats; a detailed mapping is provided in Appendices.
- Color and display guidance are provided (Appendix 5 and 6) with both standard and color-blind friendly options; a QGIS symbology file is supplied.

## Validation, accuracy, and data quality
- Validation dataset: 33,107 reference points spanning all 21 classes.
- Overall accuracy: 86.1% (with class-level producer’s and user’s accuracies documented in Appendix 4).
- Known issues
  - A small number of polygons missing from vector land parcel products; negligible effect on 1 km raster outputs; 10 m classified pixels are unaffected.
  - Some spectral confusion between certain classes (e.g., coastal/peat, Saltwater vs Freshwater) varying by class.
  - 1 km percentage totals may sum to slightly above or below 100 due to rounding; coastal areas may show under-representation.
  - The Land Parcel Spatial Framework uses a fixed MMU (~0.5 ha); some narrow features may be present only in 10 m data.
  - GID identifiers for parcels do not match LCM2015, affecting direct parcel-ID comparisons over time.

## Access, citation, and reproducibility
- Each LCM2022 dataset has a DOI; citations are provided for the data products (Marston et al. 2024a–g) and for an overview of production methods (Marston et al. 2023).
- Data products include supplementary materials (Appendices) with detailed class definitions, correspondence matrices, and display templates.
- Disclaimer: method changes year-to-year mean some differences between maps reflect methodology as well as real change.

## Appendices and supplementary materials (high level)
- Appendix 1: Notes on UKCEH Land Cover Classes (class-specific nuances and training considerations).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and their relationship to UKCEH classes.
- Appendix 3: Full list of LCM2022 datasets with DOIs and citations.
- Appendix 4: Detailed correspondence matrices (confusion/accuracy by class).
- Appendix 5 & Appendix 6: Recommended colour recipes for displaying classes (including color-blind friendly version) and linked QGIS files.