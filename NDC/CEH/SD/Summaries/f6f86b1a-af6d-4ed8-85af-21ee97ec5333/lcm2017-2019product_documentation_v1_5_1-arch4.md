# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- Introduces three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map represents a suite of geospatial datasets, produced automatically using Bootstrap Training with a Random Forest classifier.
- Aims to support informed decision-making on land cover by providing standardized, UK-wide classifications aligned with UKCEH classes and Biodiversity Action Plan (BAP) Broad Habitats.
- Documents data production, validation, decisions, and future plans to help users assess suitability for current and future work.

## Data structure and datasets
- 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) mapped consistently with LCM2015; 21-class scheme alongside UKCEH Aggregate Classes (for generalized analyses).
- Yearly dataset package (GB and Northern Ireland): 42 datasets total (three years × GB/NI × product types).
- Core datasets:
  - 20m Classified Pixels: new RF classification results from Sentinel-2 Seasonal Composite Images; two-band rasters per location: band 1 = predicted class, band 2 = class membership probability (0–100).
  - Land Parcels: attribute-rich dataset describing parcel-level results; key fields include gid, _hist, _mode, _purity, _conf, _stdev, _n. Some field names changed from LCM2015 for production consistency.
  - 25m Rasterised Land Parcels: 3-band rasters capturing per-parcel modal class, confidence, and purity.
  - 1km Raster products: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).
- Spatial scopes and resolutions:
  - GB: 20m Classified Pixels; 25m Rasterised Land Parcels; 1km products; Great Britain extents in British National Grid (EPSG:27700).
  - Northern Ireland: 20m Classified Pixels; 25m Rasterised Land Parcels; NI extents in Irish Grid (EPSG:29903).
- Classification framework:
  - 21 UKCEH Land Cover Classes, 10 UKCEH Aggregate Classes, mapped to BAP Broad Habitats where applicable.
  - Datasets include mosaic/interoperability notes and explicit metadata for classification confidence and parcel-level summaries.

## Production workflow and methodology
- Bootstrap Training
  - Fully automatic, self-starting training process using historic LCM observations as training data.
  - For LCM2017–2019, bootstrap samples were drawn from UKCEH LCM2015 parcels with ≥99% purity to balance learning.
  - Future updates planned to use majority signals across multiple years (e.g., 2020–2021 bootstrap strategies).
- Random Forest classification
  - Balanced sampling: from each training bag, 10,000 samples per class to ensure rare classes are adequately represented.
  - Production software integrates Weka, PostGIS, and GDAL; all tools are open source.
- Classification Scenes and satellite inputs
  - Sentinel-2 Seasonal Composite Images (TOA reflectance) per season; seasonal composites include four seasons (winter, spring, summer, autumn) and nine Sentinel-2 bands.
  - Contextual information (Context Rasters) added to reduce spectral confusion before classification.
- Seasonal composites and context
  - Seasonal composites generated via Google Earth Engine; 4-season coverage with some gaps due to cloud; GEE TOA data used as baseline (SR data considered but not found to improve accuracy in this study).

## Classification scenes and contextual information
- GB Classification Scenes
  - 100x100 km tiles used to sample and construct 36-band Seasonal Composite Images.
  - Each Classification Scene combines spectral bands with 20m Context Rasters (46-band final input).
  - 74 overlapping GB Classification Scenes classified independently; visual checks used to resolve overlaps.
- Northern Ireland
  - A single 43-band Classification Scene per year (36 spectral bands + 7 context layers) determined by NI’s minimum bounding rectangle.

## The UKCEH Land Parcel Spatial Framework
- UKCEH Land Parcel Spatial Framework used to structure 20m Classified Pixels into land parcels (minimum MMU ≈ 0.5 ha).
- Parcel geometry remains unchanged from LCM2015, but storage organization and indices updated to enable faster processing.
- gid is consistent within LCM2017–2019 and used for cross-year comparison; direct parcel ID matching with LCM2015 is not possible.
- The framework is designed to represent real-world units (fields, parks, urban areas), but users may apply alternative parcel structures for their own analyses.

## Data quality, validation, and interpretation
- Validation approach
  - UK-scale validation against GB countryside survey 2019 data, National Forest Inventory, IACS data, and bespoke LCM validation points (n ≈ 22,325).
- Reported accuracy
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes on validation
  - Validation uses data sources with different purposes and class definitions; conversions to UKCEH classes introduce subjectivity.
  - Validation figures are indicators of performance, not absolute truth; still, ~80% correspondence across 21-class maps is considered strong and improves with method maturation.
- Manual corrections
  - No manual corrections were applied to LCM2017–2019; visual checks and formal validation were performed to ensure product quality.

## Datasets, metadata, and usage notes
- Dataset metadata and structure
  - Coordinate systems: GB (EPSG:27700), NI (EPSG:29903).
  - 20m Classified Pixels and Land Parcels include detailed attributes; 25m Rasterised Land Parcels add bands for modal class, confidence, and purity.
  - 1km rasters summarize parcel-level classifications across 1km grid squares (Percent Cover, Percent Aggregate Cover, Dominant Cover, Dominant Aggregate Cover).
- Data relationships and visualization
  - UKCEH provides a color recipe (Appendix 3) to map 21 Land Cover Classes to RGB colors for visualization.
  - Appendix 4 includes confusion matrices and user/producer accuracies by year and class, illustrating class-level performance and common misclassifications.
- Important caveats
  - LCM2017 Land Parcels gid values differ from LCM2015; best cross-year comparisons use the gid within the 2017–2019 framework.
  - Some class pairs show inter-class confusion (e.g., Arable vs. Improved Grassland; various upland classes) explained in Appendices.

## Appendices and supporting material
- Appendix 1: Notes on UKCEH Land Cover Classes (class motivations, detection considerations, and common confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and mappings to UKCEH/Land Cover Classes).
- Appendix 3: Recommended RGB color mappings for displaying UKCEH Land Cover Classes.
- Appendix 4: Full validation results, including confusion matrices, user’s and producer’s accuracies per class and year.
- Appendix 5: Full list of datasets and their GB/NI implementations per year (dataset naming and storage specifics).

## Future plans and ongoing evolution
- Annual update cadence announced; go-forward plan to release a new LCM every year.
- Exploration of expanded input data (e.g., broader multi-source inputs, potential use of Sentinel-1 SAR for gap filling).
- Continued refinement of bootstrap strategies and training data to improve class separability and overall accuracy.
- Ongoing development of the UKCEH Land Parcel Spatial Framework to support diverse user-defined parcel structures.