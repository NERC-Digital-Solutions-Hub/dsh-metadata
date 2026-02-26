# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- Presents user guidance for three national UKCEH Land Cover Maps (LCMs): LCM2017, LCM2018, and LCM2019.
- Documents content, structure, production decisions, validation, and future plans to help users apply the data in current and future work.
- Maps 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; aims for timely, annual updates to monitor land cover change.

## Data products and formats
- 21 UKCEH Land Cover Classes; available as multiple, linked datasets per year:
  - 20m Classified Pixels (primary pixel-class map; includes per-pixel membership probability)
  - Land Parcels (parcel-level attributes derived from 20m pixels)
  - 25m Rasterised Land Parcels (three-band raster: mode, conf, purity)
  - 1km Raster products:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Separate GB (Great Britain) and NI (Northern Ireland) versions; 42 datasets in total (per year: GB and NI variants).
- 20m Classified Pixels provide class membership with a second band indicating classification confidence (0–100).

## Production approach and inputs
- Automated production combining Bootstrap Training with Random Forest (RF) classification to enable near-automated, rapid mapping.
- Data inputs:
  - Sentinel-2 Seasonal Composite Images (median TOA reflectance per season; 20m resolution)
  - 10 Context Layers per region to reduce spectral confusion (e.g., terrain, proximity to buildings/roads/coast, etc.)
  - Use of Google Earth Engine for data processing; TOA reflectance chosen over surface reflectance after validation.
- Seasonal framework:
  - Seasonal Composite Images per season (winter, spring, summer, autumn) across the four seasons to capture phenology.

## Classification scenes and spatial framework
- GB classification uses 100x100 km overlapping tiles (36 spectral bands + 10 context bands; total 46 bands) to produce 74 GB Classification Scenes; each scene trained and classified independently with overlap used to ensure varied training and coverage.
- NI uses a single 43-band Classification Scene per year (36 spectral + 7 context bands) determined by the NI extent.
- UKCEH Land Parcels Spatial Framework:
  - 0.5 ha minimum mapping unit (MMU); parcels used to summarise 20m pixel data into discrete land parcels (fields, parks, urban areas, etc.).
  - Parcel identifiers (gid) do not match LCM2015 for cross-year comparisons; comparisons should use the gid across LCM2017–2019, not historic parcel IDs.
  - The framework allows summarisation using alternative boundaries (catchments, administrative boundaries, reserves, etc.) beyond the official parcel framework.
- Bootstrap Training:
  - Training data are bootstrapped from LCM2015 parcels with high purity (≥99%) to seed the RF classifier.
  - The bootstrapped training set evolves over time as new maps are produced; future maps may use multi-year majority signals (e.g., 2017–2019) for training.
- Random Forest classification:
  - Balanced sampling (10,000 samples per class per training set) to ensure rare classes are learned effectively.
  - Production software integrates WEKA, PostGIS, and GDAL (open-source tools).

## Dataset specifics and attributes
- 20m Classified Pixels: new high-detail dataset (2-band rasters: predicted class; confidence 0–100).
- Land Parcels: per-parcel attributes including gid, histogram of class counts, modal class, purity, confidence, standard deviation, and pixel count within parcel.
- 25m Rasterised Land Parcels: three bands (mode, conf, purity); last two bands reflect parcel-averaged confidence and purity.
- 1km Raster Datasets:
  - 1km Percent Cover (21 bands)
  - 1km Percent Aggregate Cover (10 bands)
  - 1km Dominant Cover (1 band)
  - 1km Dominant Aggregate Cover (1 band)
- Coordinate systems:
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid (EPSG: 29903)

## Validation and accuracy
- Product validation undertaken against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke validation points (22,325 total points).
- Reported accuracy (overall) at UK scale:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes on validation:
  - Validation data are not a gold standard; they are best-available indicators with some misclassifications.
  - Validation points come from sources with different class schemes; conversions introduce subjectivity.
  - Approximately 80% correspondence across 21-class maps is considered strong given the automated approach.
- Class-level and producer’s accuracy metrics are provided in confusion matrices (Appendix 4) for each year.

## Comparability and year-to-year changes
- Parcel identifiers (gid) do not match across LCM2015 and LCM2017–2019; cross-year parcel comparisons require using the new gid reference (not historical parcel IDs).
- The Land Parcel Spatial Framework remains stable in geometry but was reorganised for faster processing; minor attribute changes occurred since LCM2015.
- The 20m Classified Pixels retain more detail than the aggregated 25m or 1km products, enabling detection of narrow features but requiring parcel-based summarisation for certain analyses.

## Contextual and seasonal inputs
- Context rasters (20m) provide spatial context to disambiguate spectrally similar classes (e.g., coastal proximity, urban proximity, terrain).
- GB-specific context layers include height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, and woodland mask.
- NI context layers include height, aspect, slope, urban mask, distance to coast, distance to freshwater, and distance to road.

## Appendices and class framework
- Appendix 1 and Appendix 2 provide notes on UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats, including mapping considerations, potential spectral confusions, and guidance for interpreting classes such as Broadleaved woodland, Coniferous woodland, Arable, Grasslands, Bracken, Peaty habitats, Coastal classes, Urban/Suburban, and more.
- Appendix 3 offers a recommended RGB color recipe for displaying Land Cover Classes.
- Appendix 4 contains the full confusion matrices and class-level validation metrics for LCM2017–LCM2019, including producer’s and user’s accuracies.
- Appendix 5 lists the full dataset inventory for LCM2017, LCM2018, and LCM2019.

## Future directions and ongoing development
- Plans to release new LCMs annually (e.g., LCM2020, LCM2021) using progressively refined Bootstrap Training strategies (evolving bootstrap from majority signals across recent years).
- Exploration of expanding input data sources (e.g., Sentinel-1 SAR, additional optical sources) and addressing potential gaps in cloudy periods.
- Continuous review of data inputs and metadata to improve traceability, openness, and data governance.

## Data governance, openness and usage considerations
- Outputs are designed for clear presentation (reports, charts, dashboards) and stakeholder consultation.
- Underlying data and metadata handling are emphasized, with attention to quality assurance, data cleaning, transformation, and appropriate sharing.
- The workflow is designed to minimize duplication and maintain consistency with prior maps while enabling rapid annual updates, albeit with acknowledged limitations in automated accuracy and absence of manual corrections in this cycle.