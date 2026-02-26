# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose: User guide for three UKCEH land cover maps (LCM2017, LCM2018, LCM2019); explains content, production decisions, validation, and future plans to help users apply the data appropriately.

## Key aims and context for monitoring frameworks

- LCMs provide standardized, UK-wide environmental health land cover data to scrutinize change and inform policy decisions.
- Data are produced automatically to enable annual updates; terminology and class mappings are aligned with UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats.
- Acknowledges data challenges (gaps, metadata quality, transformation needs) and aims for openness, quality assurance, and transparent governance in production.

## Data content and structure

- Land Cover Classes: 21 UKCEH Land Cover Classes (mapped to BAP Broad Habitats) reused from LCM2015 with careful cross-referencing to maintain comparability.
- Dataset suite (for each year): 20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, plus 1km raster products (Percent Cover, Percent Aggregate Cover, Dominant Cover, and Dominant Aggregate Cover).
- Extents and coordinate systems:
  - Great Britain: British National Grid (EPSG:27700)
  - Northern Ireland: Irish Grid (EPSG:29903)
- Output structure:
  - 20m Classified Pixels: 2 bands (top class, and per-pixel class membership probability 0–100); preserves detailed features below 0.5 ha MMU.
  - Land Parcels: attributes including gid, _hist (histogram of class counts within parcel), _mode, _purity, _conf (mean class probability), _stdev, _n.
  - 25m Rasterised Land Parcels: 3 bands (band 1 = _mode, band 2 = _conf, band 3 = _purity).
  - 1km products: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).
- Parcel framework: UKCEH Land Parcel Spatial Framework with ~0.5 ha MMU; designed to stabilise change detection and facilitate time-series comparisons (gid changes mean LCM2015 comparisons require alternative matching).

## Production methodology

- Bootstrap Training: Automatic training data derived from historic LCMs (LCM2015 bootstrap used for 2017–2019) to seed classifiers; aims to capitalise on majority-signal training data for robustness across years.
- Random Forest classification: Balanced sampling (10,000 samples per bag) across 21 classes; integrates open-source tools (WEKA, PostGIS, GDAL) for classification.
- Seasonal and spectral inputs:
  - Seasonal Composite Images: Sentinel-2 TOA reflectance, four seasons (winter, spring, summer, autumn), 20m resolution; uses nine bands (2,3,4,5,6,7,8,11,12).
  - Seasonal bands are combined with 20m Context Rasters to form Classification Scenes.
- Context rasters (20m GB and NI examples): include terrain (Height, Aspect, Slope) and proximity/land-use masks (buildings, roads, sea, freshwater, urban, etc.) to reduce spectral confusion.
- Data sources and processing scale: GB uses 100x100 km tiles to manage processing; NI uses a single 43-band scene per year; the system tolerates occasional missing seasonal data.

## Validation and accuracy

- Validation approach: UK-scale validation against countryside survey data, National Forest Inventory data, IACS, and bespoke validation points (22,325 points total).
- Reported overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Caveats:
  - Validation data were not perfectly matched to UKCEH class definitions (converted to UKCEH classes), so accuracy is indicative, not absolute.
  - Validation points reflect currency and sampling differences; ongoing improvement is anticipated.

## Production decisions and data governance

- Automatic production (no manual map corrections this cycle) to enable annual updates; visual checks and formal validation still performed.
- Bootstrapping approach relies on stable, long-running land cover signals; the plan is to evolve bootstrap strategies (e.g., 2020 bootstrap from 2017–2019 majority signals).
- Data transparency and reuse:
  - The Land Parcel Spatial Framework is fixed between 2017–2019; gid values do not match LCM2015 for parcel-level comparisons, though gid can be used for year-to-year parcel comparisons within the same product family.
  - Users can apply their own parcel structures beyond the UKCEH framework.
- Future development:
  - Annual releases planned; continuous review of input data (e.g., exploring alternatives to fill seasonal gaps with different optical sources or radar data).
  - Potential improvements in upland vegetation mapping and peatland-related classes with new training data.

## Classification scenes and data accessibility

- GB classification: 74 overlapping 100x100 km GB scenes used to build 36-band Seasonal Composite Images plus 20m context, resulting in 46-band GB Classification Scenes; classifications from overlaps are resolved via visual precedence to produce final maps.
- NI classification: a single 43-band scene per year (36 spectral + 7 context bands) determined by the minimum bounding rectangle of NI land mass.
- Accessibility and metadata: extensive appendix material (Appendix 4 and 5) provides validation details, class mappings, and dataset inventories; Table 1–5 (and Appendix 1–3) document data relationships, class derivations, and color conventions.

## Appendix highlights (for context and detailed interpretation)

- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats; guidance on class interpretation, calibration, and limitations in remote sensing detection (e.g., upland peat, bracken, salts, and linear features).
- Appendix 3: Recommended RGB color recipe for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation results details (confusion matrices, user/producer accuracies) for each LCM year.
- Appendix 5: Full datasets listing and naming conventions across LCM2017, LCM2018, and LCM2019.

## Bottom line for monitoring and policy use

- The UKCEH LCM2017–2019 suite provides annually updated, 21-class land cover maps with multi-scale raster products and accompanying metadata to support change detection, trend analysis, and environmental health monitoring.
- Methodology emphasizes automation, bootstrap-based learning, and transparent documentation, while acknowledging data and metadata challenges and the need for ongoing validation and methodological refinement.