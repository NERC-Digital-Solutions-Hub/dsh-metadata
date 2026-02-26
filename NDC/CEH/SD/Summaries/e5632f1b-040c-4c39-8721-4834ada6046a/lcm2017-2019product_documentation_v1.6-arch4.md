# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Purpose and scope
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map comprises a range of geospatial datasets; aims to help users understand production, structure, validation, and future plans to apply UKCEH LCM data effectively.
  - Maps are generated automatically using Bootstrap Training and a Random Forest classifier; intended to enable annual UK-wide land cover maps.
  - Visual checks and formal validation indicate data are of similar quality to the prior LCM2015; no manual corrections were performed in these releases.

- Data model and key datasets
  - Product suite and class structure
    - 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats; consistent with LCM2015 and aligned with prior maps for comparability).
    - UKCEH Land Parcel Spatial Framework underpins parcel-based summarisation; minimum mappable unit ~0.5 ha.
    - UKCEH Aggregate Classes dataset available as a coarser generalisation.
  - Dataset families (per year, GB and NI)
    - 20m Classified Pixels (new): 2-band rasters; band 1 = most probable UKCEH Land Cover Class; band 2 = classifier confidence (0–100). Preserves detailed landscape features.
    - Land Parcels: parcel-level attributes (e.g., _hist, _mode, _purity, _conf, _stdev, _n); minor attribute changes since LCM2015.
    - 25m Rasterised Land Parcels: three-band rasters (dominant class _mode, confidence _conf, purity _purity).
    - 1km Percent Cover: 21-band rasters; percentage cover per 1 km square.
    - 1km Percent Aggregate Cover: 10-band rasters; percentage cover per UKCEH Aggregate Class per 1 km.
    - 1km Dominant Cover: 1-band raster; dominant class per 1 km square.
    - 1km Dominant Aggregate Cover: 1-band raster; dominant aggregate class per 1 km square.
  - Production and geographic scope
    - Data produced for Great Britain (GB) and Northern Ireland (NI); each year has GB and NI versions.
    - In total, 42 datasets produced (for 3 years × GB/NI × dataset types; Appendix 6 lists full dataset names).

- Production methodology
  - Sentinel-2 Seasonal Composite Images
    - Use Google Earth Engine to create four seasonal composites (winter, spring, summer, autumn) from Sentinel-2 TOA reflectance; 20 m resolution; median per season.
    - Some seasonal gaps due to cloud; classifier tolerates partial spectral information; no manual gap filling planned for these releases.
  - Context rasters
    - 20 m context rasters provide surrounding information to reduce spectral confusion (terrain, proximity to buildings/roads/coast/freshwater, foreshore, tidal water, woodland; GB and NI differences listed).
  - Classification Scenes
    - GB: 100 x 100 km tiles used to extract 36-band Seasonal Composite Images; combined with 20 m context rasters to form 46-band GB Classification Scenes; 74 overlapping scenes classified independently; visual checks determine precedence in overlaps.
    - NI: single 43-band Classification Scene per year (36 spectral + 7 context) per year.
  - UKCEH Land Parcel Spatial Framework
    - Maintains the same parcel geometry as LCM2015; parcel identifiers (gid) do not match LCM2015; fixed structure supports time-series comparison via spatial overlap.
    - MMU ~0.5 ha; parcels typically dominated by a single land cover class; parcel-based summarisation reduces noise.
    - Provides option for users to apply their own parcel structures for summarisation.
  - Bootstrap Training
    - Fully automatic training using historic maps as training data; samples the current satellite image to produce spectral training observations.
    - Bootstrap Training for 2017–2019 uses UKCEH LCM2015 parcels with purity ≥ 99% to train; future maps (LCM2020, LCM2021) planned to use majority signals across multiple years.
  - Random Forest classification
    - Balanced training with bootstrap data; 10,000 samples per class; uses Weka, PostGIS, and GDAL tools.
    - Produces 20 m Classified Pixels as the base product; remaining products derived from these pixels.
  - Validation and quality assessment
    - UK-scale validation uses GB countryside survey 2019 data, open-source National Forest Inventory data, IACS data, and bespoke validation points (n=22,325).
    - Reported overall accuracies: LCM2017 ~78.6%, LCM2018 ~79.6%, LCM2019 ~79.4%.
    - Validation data have caveats: data sources differ from classification classes; conversions required; no absolute truth; results indicate strong but improvable performance as methods mature.

- Data presentation and accessibility
  - Color and display guidance provided (Appendix 3) with recommended color recipes for displaying each UKCEH Land Cover Class; separate color-blind friendly versions (Appendix 4).
  - Full confusion matrices and producer/user accuracy metrics provided (Appendix 5) to aid interpretation of accuracy and class-specific performance.
  - Datasets documented with detailed metadata (Appendix 6); GB NI coordinate systems indicated (GB: EPSG 27700; NI: EPSG 29903).

- Practical considerations, limitations, and caveats
  - Spectral similarity and context-driven misclassifications remain, especially for:
    - Saltwater vs Freshwater in coastal/estuarine zones.
    - Upland peatland and peat-dominated vegetation (confusion with Bog, Acid Grassland, Fen, Marsh, Swamp).
    - Bracken and Acid grassland boundary separability; some classes remain spectrally challenging.
  - Some regional habitat classifications rely on broad habitat concepts (BAP Broad Habitats) rather than exact spectral equivalents; emphasis on maintaining consistency for change detection.
  - 4-season data gaps may occur; future work may use Sentinel-1 SAR or other sources to fill gaps.
  - Parcel identifiers differ from LCM2015; cross-map comparisons by parcel require gid-based matching rather than prior parcel IDs.

- Use and governance implications for Data Leaders
  - Annual release cadence supports near-term monitoring of land cover change with longitudinal consistency via the Land Parcel Spatial Framework.
  - Bootstrap Training enables rapid production using existing maps as training data; helps minimise field data collection while enabling timely updates.
  - 42-dataset product suite offers multi-resolution summaries (20 m detailed pixels, 25 m parcel summaries, and 1 km aggregated views) suitable for policy analysis, management, and partner networks.
  - Clear provenance and validation reporting facilitate risk assessment, quality assurance, and governance of land cover data assets.
  - Awareness of data limitations and class ambiguities supports appropriate interpretation and adoption in decision-making and policy contexts.

- Next steps and future plans
  - Continue annual LCM production; planned LCM2020 and beyond with expanded bootstrap bases (multi-year majority signals).
  - Ongoing review of input data (e.g., potential inclusion of Sentinel-1 SAR) and expansion of training data to improve class separability.
  - Potential enhancements to the Land Parcel Framework as resolution and data sources evolve; maintain ability for users to apply alternative parcel structures for time-series analyses.