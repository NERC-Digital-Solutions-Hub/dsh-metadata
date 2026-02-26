# The UKCEH Land Cover Map for 2021

## Overview and Aim
- User guide for UKCEH Land Cover Map 2021 (LCM2021), a multi-dataset national land cover product designed to help users make informed decisions and understand data production, validation, and accuracy.
- LCM2021 aims to maximise temporal consistency, enable change detection, and support environmental objectives through annual updates and robust governance of land cover data.

## Datasets and Holdings
- LCM2021 comprises six datasets across Great Britain and Northern Ireland (GB and NI):
  - 10 m Classified Pixel datasets (GB and NI)
  - Land Parcel datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets (GB and NI)
- Additional related data structures described include:
  - Seasonal Composite Images (Sentinel-2 based) used for classification
  - Context Rasters (10 m) to reduce spectral confusion
  - Classification Scenes framework for GB and NI (GB uses 32 GB tiles; NI uses a single Scene)

## Production and Methodology
- Classification approach:
  - Bootstrap Training: automatic training data drawn from historic LCMs (LCM2018–LCM2020) to train a Random Forest classifier, reducing need for new field data.
  - Random Forest classification of Classification Scenes to produce 10 m Classified Pixels.
  - Balanced learning with sampling with replacement to ensure rare classes are well represented.
- Data inputs and structure:
  - Seasonal Composite Images derived from five Sentinel-2 bands, aligned to 10 m resolution, with four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - 10 m Context Rasters (GB: height, aspect, slope, proximity to buildings/roads/seawater/freshwater, foreshore and tidal masks, woodland). NI includes urban mask and coast/freshwater/road proximity masks.
  - The UKCEH Land Parcel Spatial Framework used to aggregate 10 m pixels into land parcels (MMU ~0.5 ha) to produce cleaner parcel-level data.
- Processing and software:
  - Bespoke UKCEH software integrates Weka, PostGIS, and GDAL; runs on Google Earth Engine for Seasonals; classification results are stored in structured datasets with metadata.
- Outputs and data structure:
  - 10 m Classified Pixels: first band = UKCEH Land Cover Class, second band = class membership probability.
  - 25 m Rasterised Land Parcels: a 3-band raster with dominant class (mode), confidence, and purity per parcel.
  - 1 km products: summarize 25 m rasters to provide dominant class and percentage cover (with rounding implications near coast).
- Temporal and methodological notes:
  - Annual production intended to improve temporal consistency and facilitate change detection.
  - If new methods yield significant accuracy improvements, full catalogue re-application may occur.
  - Bootstrap Training uses parcels with >80% purity classified consistently across three years.

## Spatial, Classification, and Validation Details
- Coordinate systems and extents:
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid TM75 (EPSG: 29903)
- Land Parcel Spatial Framework:
  - Minimum parcel area ~0.5 ha; designed to represent discrete real-world units (fields, parks, urban areas, etc.).
  - Unique parcel identifiers (gid) differ from LCM2015; historical comparisons by parcel ID may not be possible.
- Validation:
  - Validation dataset: 35,182 reference points across all 21 UKCEH Land Cover Classes.
  - Overall accuracy: 82.6% with 95% CI of 82.19%–82.99%.
  - Validation based on comparison between 25 m Rasterised Land Parcel data and reference points.
- Accuracy and classification nuances:
  - The 10 m dataset preserves fine detail not generalised by the Land Parcel Spatial Framework; validation assessments are anchored to the 25 m parcel data, so users should interpret 10 m details with this caveat.
  - The dataset establishes relationships to BAP Broad Habitats (Appendices); some mappings are non-trivial due to differences between satellite-detectable land cover and field-based habitat classifications.
  - Seasonal and context layers help reduce spectral confusion among spectrally similar classes (e.g., different grassland types, wetlands, urban features).

## Data Governance, Accessibility, and Use
- Metadata and naming:
  - Appendix 3 provides the official dataset names for each dataset and region.
  - Documentation includes detailed attribute definitions for 10 m pixels and 25 m parcels (e.g., _hist, _mode, _conf, _stdev, _agg, _n for parcel attributes).
- Data quality and caveats:
  - 10 m Pixel data are not generalised; best for specialist users who understand the implications of higher detail versus parcel-based validation.
  - 1 km percentage data are rounded; coastal areas may sum to slightly less or more than 100% due to aggregation and coastal edge effects.
- Colouring and accessibility:
  - Appendices provide recommended colour recipes (standard and color-blind friendly) for display of UKCEH Land Cover Classes.
- Relation to broader frameworks:
  - UKCEH Land Cover Classes are aligned with, but not identical to, UK BAP Broad Habitats; italicised usage signals reference to BAP where relevant.

## Practical Considerations for Data Stewards
- Data governance and updates:
  - LCM2021 is part of an ongoing annual series; plan for regular updates and potential re-application across the catalogue if new methods yield significant gains.
- Interoperability and continuity:
  - Be aware of changes in parcel identifiers between LCM2015 and LCM2021 for cross-era comparisons.
  - Understand that 10 m detail is preserved, but validation is anchored to 25 m parcel data, affecting certain comparative analyses.
- Use case considerations:
  - Suitable for high-resolution land cover mapping, change detection, and ecosystem monitoring, with explicit caveats about spectral similarity and habitat mapping nuances.
- Documentation and provenance:
  - Maintain access to appendices for a thorough understanding of class definitions, BAP relationships, and classification decisions.

## Endnotes and References
- Validation and methodological references include Breiman (Random Forest), Carrasco et al. (Sentinel-2 combinations), and Morton et al. (LCM2007 framework).
- The guide includes extensive Appendices (UKCEH Land Cover Classes; BAP Broad Habitats; dataset lists; correspondence matrices; display color recipes) to support interpretation and consistent usage.