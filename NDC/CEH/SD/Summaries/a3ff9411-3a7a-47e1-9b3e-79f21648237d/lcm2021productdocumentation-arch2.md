# The UKCEH Land Cover Map for 2021

## Purpose and Intended Use
- User guide for the UKCEH Land Cover Map 2021 (LCM2021), detailing data production, validation, and accuracy.
- LCM2021 comprises six geospatial datasets (three per region: Great Britain and Northern Ireland) and supports monitoring environmental health and change over time.
- Emphasizes annual production to improve temporal consistency, comparability, and change detection; formal validation indicates overall accuracy of 82.6%.

## Product Structure and Datasets
- Six geospatial datasets (three per region):
  - 10 m Classified Pixel datasets
  - Land Parcel datasets (attributes derived from the Parcel Framework)
  - 25 m Rasterised Land Parcel datasets
- Additional derived data product:
  - 1 km Summary Rasters (dominant and percentage cover for LCM2021 classes and aggregates)
- Regions and projections:
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: Irish Grid TM75 (EPSG 29903)
- Parcel framework:
  - Land Parcel Spatial Framework with a minimum mapping unit ~0.5 ha; parcels used to reduce classification noise.
  - Unique identifiers (gid) differ from LCM2015; comparability by parcel ID across years is limited.
- Extents and scale:
  - GB: coordinates ~0–700,000 East, 0–1,300,000 North
  - NI: truncated Irish Grid extents
- Output specifics:
  - 10 m Classified Pixels: two-band raster (class ID, confidence); detailed features preserved (not generalized to the parcel framework)
  - 25 m Rasterised Land Parcels: three-band rasters (dominant class, confidence, purity)
  - Land Parcel dataset: per-parcel attributes including _hist, _mode, _purity, _conf, _stdev, _agg, _n
- Classification outputs:
  - 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats (with noted alignment caveats)
  - 10 m Context Rasters and Seasonal Composite Images used to improve spectral separation

## Data Production and Methodology
- Seasonal Composite Images:
  - Derived from Google Earth Engine using Sentinel-2 data; 10 m resolution; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec)
  - Bands used: 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12
  - Data gaps from clouds tolerated; classifier handles partial spectral information
- Context Rasters:
  - 10 m GB context rasters (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal water masks, woodland mask)
  - 10 m NI context rasters (height, aspect, slope, urban mask, distances to coast/road/freshwater, foreshore and tidal water masks)
- Classification Scenes:
  - GB classified into 32 tiles (~100 x 100 km); NI uses a single scene (49-band) for Northern Ireland
  - Each Classification Scene trained and classified independently
- Bootstrap Training:
  - Automatic training approach using historic LCM data (LCM2018–LCM2020)
  - Filtering: parcels with >80% purity and consistent class across three years
  - Creates large training sets to bootstrap the classifier for 2021
- Random Forest (RF) Classification:
  - Training: 10,000 samples per bag, with replacement to balance class representation
  - Output: 10 m Classified Pixel product and associated confidence
  - Software: bespoke UKCEH tool integrating WEKA, PostGIS, and GDAL
- Validation:
  - 35,182 validation points across 21 classes
  - Overall accuracy: 82.6% (95% CI: 82.19%–82.99%)
- Methodological notes:
  - Continual evaluation of methods; potential re-application across entire catalogue if accuracy improves
  - Aims to maximize temporal consistency for change detection and monitoring

## Data Content and Structure (Detailed)
- 10 m Classified Pixels:
  - Band 1: most likely UKCEH Land Cover Class ID
  - Band 2: class membership probability/confidence
  - Not generalized by the UKCEH Land Parcel Spatial Framework to preserve small features
  - Recommended for specialist users who understand confounding and uncertainty
- Land Parcel Datasets:
  - Per-parcel attributes: gid, _hist (list of class frequencies), _mode (dominant class), _purity, _conf (mean class membership probability), _stdev, _agg (aggregate class), _n (pixel count)
  - Purpose: provide a stable structural framework for time-series comparisons and change detection
- 25 m Rasterised Land Parcel Datasets:
  - 3-band raster: band1 = modal land cover (mode), band2 = conf, band3 = purity
- 1 km Summary Rasters:
  - Dominant cover at 1 km (21-class and 10-class aggregates)
  - Percentage cover at 1 km for both class sets
  - Rounding may cause totals to slightly differ from 100%; coastal pixels may sum to less due to resolution and mapping rules
- Coordinate Systems and Extents:
  - GB: EPSG 27700; NI: EPSG 29903
- Dataset Listings (Appendix 3):
  - Specific dataset names and citations for GB and NI versions of 10 m Classified Pixels, Land Parcel Product, and 25 m Rasterised Land Parcels
  - Combined 1 km Summary Rasters provided as a separate product

## Data Use and Visualization
- Colour and symbology:
  - Appendix 5: Standard colour recipe for UKCEH LCM classes with recommended QGIS symbol file lcm_raster.qml
  - Appendix 6: Colour-blind-friendly palette with QGIS symbol file lcm_raster_cb_friendly.qml
- Practical guidance for analysts:
  - Use the 10 m classified pixels for high-detail mapping and fine-scale monitoring; be mindful of MMU implications
  - Use Land Parcel datasets for robust change detection at the parcel level
  - Use 1 km rasters for broad-scale summaries and cross-year comparability
  - Leverage context rasters to reduce spectral confusion, especially in complex landscapes
- Validation and quality context:
  - Validation reference data drawn from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points
  - Validation results provide a quantified confidence baseline for informing policy monitoring and decision-making

## Appendices: Contextual Guidance for Users
- Appendix 1: Notes on UKCEH Land Cover Classes (class definitions, training considerations, potential spectral confusions)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and mapping relationships; notable distinctions between BAP and UKCEH classes)
- Appendix 3: Full list of datasets for UKCEH LCM2021 (dataset names, geographic scope, citations)
- Appendix 4: Validation correspondence matrices (confusion matrices and accuracy statistics by class)
- Appendix 5: Standard colour recipe for display (class-specific RGB values; display guidance)
- Appendix 6: Colour-blind-friendly colour recipe (adjusted RGB values)
- Supporting files: QGIS symbology files for standard and colour-blind palettes

## Key Takeaways for Analysts Monitoring the Environment
- LCM2021 provides a standardized, annually updated, high-resolution data framework (10 m) for monitoring land cover and environmental change across the UK, with region-specific parcel and raster products.
- The methodology combines automated Bootstrap Training with Random Forests, enriched by Seasonal Sentinel-2 imagery and contextual data to improve classification in spectrally similar landscapes.
- Validation demonstrates solid accuracy (82.6%), enabling reliable trend analysis and policy evaluation across time.
- The three core dataset types (10 m classified pixels, land parcels, 25 m rasterised parcels) support both detailed mapping and robust change detection at multiple scales; 1 km summary rasters offer efficient coarser-scale summaries for broader analyses.
- Users should account for MMU implications, potential parcel-ID comparability issues with past releases, and class-definition nuances when comparing across years or with BAP Broad Habitats.
- Visualization aids (standard and color-blind palettes) and GIS symbol files enable consistent, accessible mapping for monitoring dashboards and reporting.