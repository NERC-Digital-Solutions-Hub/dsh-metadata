# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map comprises a set of geospatial datasets mapped to 21 UKCEH Land Cover Classes (based on BAP Broad Habitats).
- Data produced automatically using Bootstrap Training and a Random Forest classifier; emphasizes rapid UK-wide production.
- Documents data content, production choices, validation results, rationale, and future plans to help informed use and governance.

## Data structure and contents
- Release includes 42 datasets (GB and NI): 21 classes each for GB and NI, plus multiple derived products.
- Core products:
  - 20m Classified Pixels (GB and NI)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Dominant Cover (GB and NI)
  - 1km Dominant Aggregate Cover (GB and NI)
  - 1km Percent Cover (GB and NI)
  - 1km Percent Aggregate Cover (GB and NI)
- 20m Classified Pixels retain 20m detail and provide per-pixel class probability; not generalized by parcels to preserve granular features.
- Land Parcels summarize 20m pixels within a fixed spatial framework (~0.5 ha MMU) with attributes such as history, mode, purity, confidence, and pixel counts.
- 1km rasters aggregate parcel data to give per-1km summaries (percent cover, dominant/aggregate classes).

## Production methodology
- Bootstrap Training: uses historic LCM2015 as the training basis to bootstrap the classifier, enabling automatic map updates without fresh field data.
- Training data chosen from parcels with high purity (≥99%) from LCM2015; majority signal assumed stable over time.
- Random Forest classifier trained with labeled samples to produce the 20m Classified Pixels product; balancing samples across classes to avoid bias toward common classes.
- Production tools: bespoke UKCEH software integrating Weka (ML), PostGIS, and GDAL (open-source).
- Seasonal spectral information: Sentinel-2 Seasonal Composite Images (TOA reflectance) for four seasons plus 20m Context Rasters to reduce spectral confusion.

## Features and inputs
- Seasonal Composite Images: derived from Google Earth Engine; 9 Sentinel-2 bands at 20–60 m resolution; some seasons may have cloud gaps; classifier tolerant of partial spectral information.
- Context Rasters (GB and NI): include terrain (Height, Aspect, Slope), proximity masks (buildings, roads, sea, freshwater), foreshore and tidal masks, urban/woodland indicators.
- Classification Scenes: GB uses 100x100 km tiles (74 overlapping scenes); NI uses a single 43-band scene per year (36 spectral + 7 context bands).

## UKCEH Land Parcel Spatial Framework
- Spatial framework retained from LCM2007/LCM2015 lineage; parcels ~0.5 ha MMU; consistent structure for change detection.
- gid remains the unique parcel identifier within each product, but gid values do not match LCM2015 for cross-year comparisons.
- Land Parcels include attributes such as hist (class distribution within parcel), mode, purity, conf (mean class membership probability), stdev, and n (pixel count).
- The framework supports use of users’ own parcel boundaries for summarization beyond the default framework.

## Validation and accuracy
- Validation against GB Countryside Survey 2019, National Forest Inventory, IACS, and manually interpreted validation points (22,325 total).
- Reported overall accuracy (UK scale):
  - 2017: 78.6%
  - 2018: 79.6%
  - 2019: 79.4%
- Validation data were mapped to UKCEH classes; there is inherent uncertainty due to cross-walking older/class definitions.
- Full validation tables and confusion matrices provided in Appendix 4.

## Data quality and limitations
- Automatic classification with no manual corrections for LCM2017-2019; visual checks and formal validation performed.
- Classification errors are expected to be spatially random over time; ongoing improvements anticipated with methodological refinements.
- Some classes (e.g., upland peat, bracken separation) present detection challenges and rely on training data quality and contextual layers.
- Coordinates and grid extents are country-specific (GB and NI); NI uses Irish Grid (TM75) while GB uses British National Grid.

## Data availability and future plans
- Yearly release model aims to annual updates (LCMs2017–2019 plus planned future maps); Bootstrap Training may evolve for LCM2020 and beyond.
- Users can compare across years using gid-based parcel comparisons (where applicable); cross-year parcel IDs do not match LCM2015.
- The framework supports external use with a choice to summarize 20m classified pixels using other parcel structures beyond the UKCEH Spatial Framework.

## Appendices and metadata context
- Appendix 1 & 2: Notes on UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats; definitions, relationships, and detection considerations.
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Detailed validation confusion matrices and producer/user accuracy statistics by class (GB and NI) for 2017–2019.
- Appendix 5: Full dataset lists and descriptions for LCM2017, LCM2018, and LCM2019 (GB and NI products and their dataset names).

## Practical takeaways for data stewards
- Data governance: clear provenance with Bootstrap Training lineage (LCM2015 → 2017–2019); explicit parcel framework and gid-based linking rules.
- Metadata needs: ensure cross-year comparability notes, coordinate systems (GB: EPSG 27700; NI: EPSG 29903), MMU, and dataset attribute schemas are documented.
- Data sharing and reuse: 20m Classified Pixels provide the most detailed per-pixel information with confidence scores; use Land Parcels for aggregated, parcel-based analyses with transparency on hist/mode/purity/conf.
- Validation awareness: expect around 80% accuracy at national scale; refer to Appendix 4 for class-level performance and uncertainties.
- Future-proofing: anticipate evolving Bootstrap Training strategies and potential expansion of input data sources (e.g., broader satellite and SAR inputs); monitor updates for 2020–2021 iterations.