# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Purpose and scope
- User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map suite combines multiple geospatial datasets to provide 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and align with prior maps (LCM2015, LCM2007, LCM2000).
- Aims to help users understand production, validation, and appropriate application of the data for current and future work.
- Plan to release new LCMs annually; automatic classification reduces lag between updates.

## Datasets and structure
- Core datasets include:
  - 20m Classified Pixels (new for these releases): RF classification results from Sentinel-2 Seasonal Composite Images, with per-pixel class probabilities.
  - Land Parcels: parcel-level attributes including gid, hist (histogram of class frequencies), mode (dominant class), purity, conf (confidence), stdev, and n (pixel count). Note gid values do not match LCM2015; use for cross-year comparisons via parcel overlap or the gid where possible.
  - 25m Rasterised Land Parcels: three-band rasters (mode, conf, purity) summarising the 20m pixels within parcels.
  - 1km Raster datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), and Dominant Aggregate Cover (1 band).
- Geographic coverage:
  - Great Britain (GB): British National Grid (EPSG:27700).
  - Northern Ireland (NI): Irish Grid (EPSG:29903).
- Product count: 42 datasets total (yearly set for 2017–2019 × GB/NI × dataset type).

## Production approach and methodology
- Bootstrap Training: automatic, self-starting training using historic LCM data to generate spectral training observations for current classification. For LCM2017–2019, bootstrap samples were drawn from UKCEH LCM2015 with high purity (>99%) to seed training; intention to use multi-year majority signals for future bootstraps.
- Random Forest classification: supervised learning with balanced sampling (10,000 samples per class per Classification Scene) to mitigate dominance by common classes.
- Production stack: bespoke software integrating WEKA, PostGIS, and GDAL (all open-source components).

## Classification scenes and context
- Seasonal data: Sentinel-2 Seasonal Composite Images (TOA reflectance) by season (winter, spring, summer, autumn) derived via Google Earth Engine. Four-season data capture phenology to aid discrimination.
- Context rasters (20m) provide additional spatial context to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, coast, water, etc.).
- GB Classification Scenes: 100x100 km tiles; 74 overlapping scenes classified independently with visual checks to resolve overlaps and quality.
- NI Classification Scenes: single 43-band scene per year reflecting minimum bounding rectangle of NI land mass.

## Data production notes and terminology
- UK Land Parcel Spatial Framework: maintains a fixed 0.5 ha minimum parcel size; parcels are aligned to a standardized framework to reduce classification noise and enable change detection over time.
- Bootstrap Training is designed to leverage the “majority signal” across years; ongoing evolution expected in training strategies and future bootstraps.
- Acknowledges potential future improvements with higher-resolution data and additional optical/sensor sources (e.g., Sentinel-1), especially for gaps or cloud-related issues.

## Class definitions and relationships
- 21 UKCEH Land Cover Classes derived from UK BAP Broad Habitats; relationship and derivations documented in Appendices 1–2.
- General mapping aims to keep compatibility with legacy classes to facilitate change detection, while reflecting updated habitat definitions and detection capabilities.
- Appendix 3 provides RGB color recipe for display; Appendix 4 includes validation details; Appendix 5 lists datasets per year.

## Validation and accuracy
- Validation dataset: GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke LCM validation points (22,325 total).
- Reported overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation data are not an absolute truth; they come from sources with different class mappings and purposes. Approximately 80% correspondence is considered strong for an automatic 21-class map, and accuracy is expected to improve as methods mature.
- Confusion matrices and class-level producer’s and user’s accuracies are provided in Appendix 4.

## Data quality, metadata, and accessibility
- 20m Classified Pixels preserve fine landscape details; 25m Land Parcels summarize those pixels within parcel boundaries.
- The LCM2017–2019 products include explicit metadata about extents, pixel sizes, band counts, and class mappings; some attribute names differ from LCM2015 for production efficiency.
- Data formats include 8-bit rasters at multiple resolutions and parcel-centric attribute tables; Great Britain and Northern Ireland datasets are provided separately with region-specific coordinate systems.

## Limitations and challenges
- Some landscapes remain spectrally ambiguous (e.g., upland peatlands, bracken vs acid grassland, certain grasslands) leading to misclassifications.
- Small patches and MMU constraints limit detection of some habitats; many aquatic/shoreline features near coastlines can be confused with non-vegetated surfaces.
- Unique parcel IDs (gid) do not match the LCM2015 parcel IDs, complicating direct cross-year parcel comparisons, though gid remains usable for cross-year linkage within the new framework.
- Validation uses diverse data sources with some misalignment to UKCEH classes; results are best treated as indicators rather than absolute truth.

## Practical implications for monitoring and policy
- Provides an annual, consistent suite of land cover products suitable for monitoring land cover change, habitat extent, and trend analysis across the UK.
- Enables time-series analysis at multiple spatial scales (pixel, parcel, 1 km) and supports integration with habitat/biodiversity frameworks.
- Promotes transparency via detailed metadata, validation results, and documented class mappings; however, users should exercise caution when linking to older datasets due to changes in parcel identifiers and class definitions.

## Future directions and plans
- Continue annual releases (LCM2020, LCM2021, etc.) with evolving bootstrap strategies and training data.
- Explore expanding input data sources (e.g., Sentinel-1 SAR, alternative optical sources) to improve gap-filling and year-to-year consistency, especially under cloud cover.
- Potential refinement of the Land Parcel Spatial Framework to accommodate higher-resolution data and finer MMU as satellite data quality and availability improve.

## Appendices and resource notes (highlights)
- Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relation to UK BAP Broad Habitats.
- Appendix 3: RGB color mapping for visualization of classes.
- Appendix 4: Comprehensive confusion matrices and accuracy metrics by class for LCM2017, LCM2018, and LCM2019.
- Appendix 5: Full list of datasets per year and per region (GB/NI) with dataset names and storage details.