# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- User guide for three UKCEH land cover maps: LCM2017, LCM2018 and LCM2019.
- Maps comprise 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; aligned with LCM2015 conventions.
- Production uses Bootstrap Training plus Random Forest classification to generate UK-wide maps automatically (Sentinel-2 seasonal composites with contextual rasters).
- Intent is rapid, annual updates and to help users make informed decisions about application and limitations.
- Validation indicates maps are of similar quality to recent predecessors, with formal validation and Appendix references.

## Data Content and Structure
- Datasets included per year ( GB and NI versions; total 42 datasets): 
  - 20m Classified Pixels: new 20m RF classification results with per-pixel class and an 8-bit probability indicator.
  - Land Parcels: parcel-level attributes including _hist, _mode, _purity, _conf, _stdev, _n; gid as parcel identifier.
  - 25m Rasterised Land Parcels: three bands per parcel (band 1: modal class; band 2: confidence; band 3: purity).
  - 1km Raster datasets: 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant/ Aggregate Cover (1 band each).
- Spatial coverage and formats:
  - Great Britain and Northern Ireland versions; 100x100 km GB classification tiles; complete NI single tile approach.
  - Pixel resolution, extents, and class counts summarized in Tables; 21 classes with a defined color scheme (Appendix 3).
- Parcel framework and MMU:
  - UKCEH Land Parcel Spatial Framework with minimum mapping unit ~0.5 ha; framework unchanged from LCM2015 but with storage and indexing updates.
  - gid identifiers do not match LCM2015 parcels; cross-year comparisons require parcel-based overlap or use of gid for 2017–2019 comparisons.

## Production Methods and Data Lineage
- Bootstrap Training:
  - Automatic, self-starting training that samples historic maps (LCM2015) to bootstrap training data; future bootstraps planned from majority signals across years.
- Random Forest classification:
  - Balanced sampling (e.g., 10,000 samples per class per Classification Scene); stereo training from Bootstrap Training data; RF classifier outputs 20m Classified Pixels (GB/NI).
- Seasonal Composite Images and Context:
  - Sentinel-2 median TOA reflectance per season (winter, spring, summer, autumn) at 20m; combined with 20m Context Rasters (terrain, proximity to buildings/roads/seawater, etc.) for classification scenes.
- Classification Scenes:
  - GB: 74 overlapping 100x100 km tiles; NI: single 43-band scene per year; scenes classified independently with manual quality checks for precedence where overlaps occur.
- Satellite input and future plans:
  - TOA data used (not surface reflectance) due to data availability; ongoing evaluation of input sources and potential future inclusion of more data types (e.g., SAR).

## UKCEH Land Parcel Spatial Framework
- Parcel framework unchanged in geometry from LCM2015, but with re-ordered storage and new indices to speed processing.
- gid values do not match LCM2015; cross-year comparisons should use gid only for 2017–2019, not cross-year with 2015.
- MMU ~0.5 ha; framework supports summarising 20m Classified Pixels into parcels; users can apply their own parcel structures for time-series comparisons.

## Validation and Quality
- Validation against GB countryside survey 2019, National Forest Inventory, IACS, and bespoke validation points (22,325 locations).
- Reported overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Important caveats:
  - Validation uses data sources with different purposes; class mappings may require interpretation.
  - Approximately 80% correspondence is considered strong for an automatic 21-class map; accuracy is expected to improve with methodological maturation.
  - Detailed confusion matrices and producer/user accuracies are provided in Appendix 4.

## Data Access, Metadata, and Governance
- Data format and metadata:
  - 21 UKCEH Land Cover Classes; mapping to BAP Broad Habitats described; Appendix 1–2 provide interpretation and notes.
  - Datasets have explicit coordinate systems: GB (EPSG 27700, British National Grid) and NI (EPSG 29903, Irish Grid).
  - Pixel sizes, extents, and class identifiers documented (Tables 3–4).
- Dataset naming and availability:
  - Datasets include GB and NI equivalents; naming indicates year-specific products; Appendix 5 lists full dataset inventory.
  - 20m Classified Pixels are the primary zoomed-in dataset; higher-level summaries (1km, 25m) aggregate 20m results.
- Considerations for use and governance:
  - Changes to parcel identifiers limit direct cross-year parcel comparisons; use gid for 2017–2019 comparisons.
  - Some attribute names changed from LCM2015 to align with production software; users should map fields as needed.
  - Regular annual updates planned, with Bootstrap Training evolving over time; users should monitor methodological notes for reproducibility and comparability.

## Limitations and Considerations for Data Stewards
- Automated production without manual corrections may introduce classification noise in certain habitats and transition areas.
- Seasonal gaps due to cloud cover are handled by the algorithm, but full gap filling is not guaranteed; SAR or alternative sources may be explored in the future.
- Differences in BAP Broad Habitats vs UKCEH Land Cover Classes can cause ambiguity; Appendix notes provide guidance on interpretation and relationships.
- Cross-year comparisons require careful handling of the parcel framework and gid differences; recommended approach is to use the parcel identifiers (gid) and consistent framework for time-series analysis.

## Appendices and Glossary (Key References)
- Appendix 1–2: UKCEH Land Cover Classes and BAP Broad Habitat relationships; detailed notes to reduce ambiguity.
- Appendix 3: RGB color recipes for map display by class.
- Appendix 4: Validation confusion matrices and accuracy metrics for 2017–2019.
- Appendix 5: Full dataset list and naming conventions for LCM2017, LCM2018, and LCM2019.
- Glossary: Terms such as Bootstrap Training, Classification Scene, Context Raster, Seasonal Composite Image, and Land Parcel Spatial Framework defined for user clarity.