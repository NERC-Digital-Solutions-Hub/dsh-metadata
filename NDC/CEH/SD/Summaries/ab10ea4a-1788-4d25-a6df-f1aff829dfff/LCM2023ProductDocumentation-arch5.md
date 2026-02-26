The UKCEH Land Cover Map 2023

## Purpose and Overview
- User guide for the UKCEH Land Cover Map for 2023 (LCM2023).
- Product consists of seven datasets: three for Great Britain and Northern Ireland each (a 10 m classified pixel dataset, a land parcel dataset, and a 25 m pixel rasterised land parcel dataset), plus a 1 km summary raster product covering GB+NI.
- Aimed at enabling informed use through data production details, validation, and accuracy guidance.

## Product Suite and Dataset Descriptions
- 10 m Classified Pixel datasets (GB and NI)
  - Derived from Classification Scenes using Bootstrap Training and Random Forest.
  - Band 1: UKCEH Land Cover Class; Band 2: classification confidence.
  - For GB and NI, both datasets contain 2 bands; 10 m pixels are not generalised by the Land Parcel Spatial Framework.
- Land Parcel datasets (GB and NI)
  - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to generate parcel attributes.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised version of parcel data with three bands: dominant land cover mode, confidence, and purity.
- Vector Land Parcels
  - Parcel-level attributes including gid, hist, mode, conf, purity, etc., intended for parcel-based analyses.
- 1 km Summary Raster products (GB+NI)
  - Dominant class, dominant aggregate class, and percentage cover products (21 class bands and 10 aggregate bands). Percentages are integer values; sums may deviate from 100 due to rounding and coastal effects.

## Data Production and Methodology
- Seasonal Composite Images
  - Derived from Google Earth Engine; Sentinel-2 reflectance resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10 Sentinel-2 bands.
  - Gaps due to clouds may occur but classification tolerates partial data.
- Context Rasters
  - 10 m context rasters to reduce spectral confusion (GB: height, aspect, slope, distances to buildings/roads/tidal water, freshwater, foreshore, woodland, saltmarsh; NI: height, aspect, slope, urban mask, distances to coast, freshwater, roads, foreshore, tidal water).
- Classification Scenes
  - GB: grid of 32 Classification Scenes (roughly 100 x 100 km tiles) to manage processing and phenology variation; some overlaps occur at scene edges.
  - NI: single 49-band Classification Scene (49 bands) combining a 40-band Sentinel-2 Seasonal Composite with NI Context Rasters.
- UKCEH Land Parcel Spatial Framework
  - Framework used to generalise land parcels; minimum parcel size ~0.5 ha (MMU); designed to reflect discrete real-world units (fields, parks, urban areas, etc.). Parcel identifiers may not align with LCM2015 for direct cross-year comparisons.
- Bootstrap Training
  - Automatic training using historic LCM data (LCM2020–LCM2022) with pixels >80% probability and consistent class across three years.
  - Large bootstrap datasets enable robust RF learning; under-change conditions, majority signal guides classification.
- Random Forest Classification
  - RF classifier trained with 10,000 samples per bag; balanced sampling to ensure rarer classes are learned.
  - Custom UKCEH pipeline integrating Weka, PostGIS, and GDAL (open-source stack).

## Data Quality, Validation, and Known Issues
- Validation
  - 33,107 validation reference points across all 21 LCM2023 classes.
  - Overall accuracy: 83%.
- Known Issues
  - A small number of polygons missing from vector land parcel products (causes nodata in 25 m parcel rasters); negligible effect on 1 km products; 10 m classified pixels unaffected.
- Validation Details
  - Appendix 4 contains detailed confusion matrices, user’s accuracy, and producer’s accuracy by class.
- Methodological Note
  - Data are produced with evolving methods; changes between annual maps may reflect real changes and/or methodological differences.

## Data Governance, Access, and Citations
- Each LCM2023 dataset has a DOI; recommended citation details are provided (Table 5 in the document).
  - Examples include DOIs for 10 m classified pixels (GB and NI), 25 m rasterised land parcels (GB and NI), land parcels (GB and NI), and 1 km summary rasters.
- Formal references include Marston et al. (2023–2024) and earlier UKCEH LCM production literature.
- Temporal context
  - Annual production enables differentiation of random errors from real change; classification accuracy is expected to improve as the time series matures.
- Usage guidance
  - The guide emphasizes understanding data production, validation, and accuracy to support current and future work; differences in year-to-year methods may affect comparability.

## UKCEH Land Cover Classes and Appendix Context
- 21 UKCEH Land Cover Classes are aligned with Biodiversity Action Plan (BAP) Broad Habitats, with some deviations to maintain historical consistency.
- Appendix 1 provides notes on class definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable, Various Grassland types, Wetlands, Freshwater, Saltwater, Urban/Suburban, etc.).
- Appendix 2 offers summaries of BAP Broad Habitats definitions and their relationship to UKCEH classes (including nuances and potential spectral confusion).
- Appendix 3 lists dataset names and DOIs for LCM2023 product family.
- Appendix 4 contains detailed correspondence matrices for class-to-class confusion and accuracy metrics.
- Appendix 5 and Appendix 6 provide recommended colour recipes for displaying land cover classes (standard and color-blind friendly), with downloadable QGIS symbology files.

## Technical Specifications and Access Details
- Coordinate reference systems
  - Great Britain: EPSG 27700 (British National Grid)
  - Northern Ireland: EPSG 29903 (TM75 Irish Grid)
- Pixel resolutions
  - 10 m for classified pixels (GB and NI)
  - 25 m for rasterised land parcels (GB and NI)
- Data extents and parcel counts
  - GB parcels: ~6.74 million; NI parcels: ~902k
- Data products
  - 10 m Classified Pixels (GB and NI): 2 bands (class, conf)
  - 25 m Rasterised Land Parcels (GB and NI): 3 bands (mode, conf, purity)
  - Land Parcels (Vector) (GB and NI)
  - 1 km Summary Rasters (GB and NI)
- Documentation and supplementary resources
  - DOIs and citations per dataset
  - Color recipes and QGIS symbology files included with data products

## Endnotes and Citation Guidance
- Users should cite the corresponding DOIs for each dataset when using LCM2023 data.
- Acknowledgement of methodological evolution is advised; include Marston et al. references as appropriate.