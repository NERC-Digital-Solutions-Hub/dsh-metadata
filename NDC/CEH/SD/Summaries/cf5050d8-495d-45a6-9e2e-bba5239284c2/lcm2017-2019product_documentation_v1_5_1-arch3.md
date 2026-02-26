# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map provides a suite of geospatial datasets mapping land cover across the UK, aligned to 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and 10 UKCEH Aggregate Classes.
  - Aims to help users make informed decisions about applying UKCEH LCM data in current and future work, including data production decisions, validation, and validation context.

- Content and structure
  - Maps are produced automatically using Bootstrap Training plus a Random Forest classifier.
  - Inputs include Sentinel-2 Seasonal Composite Images (seasonal median reflectance) and 20m Context Rasters to form Classification Scenes.
  - Seasonal coverage includes winter, spring, summer, and autumn; TOA reflectance used (not SR) after assessment.
  - Outputs come in multiple linked data products (see below) and are provided for Great Britain and Northern Ireland.

- Production methodology (highlights)
  - Bootstrap Training: automatic, uses historic UKCEH LCMs to sample training data; relies on majority signal over time.
  - Random Forest classification: trained with balanced sampling from Bootstrap Training data; aims to stabilize learning across classes.
  - Classification Scenes: GB uses 100x100 km tiles (36 spectral bands + 10 context layers, total ~46 bands); NI uses a single 43-band scene.
  - Context rasters: 20m data (terrain, proximity to buildings/roads/coast, etc.) to resolve spectral confusions.
  - Land parcel framework: 0.5 ha minimum mapping unit; 21 classes within a UKCEH Land Parcel Spatial Framework, designed for change detection over time.
  - No manual corrections for the 2017–2019 production cycle; visual checks and formal validation performed.

- Datasets and data products (structure and extents)
  - Dataset family: 20m Classified Pixels; Land Parcels; 25m Rasterised Land Parcels; 1km Percent Cover (21 bands); 1km Percent Aggregate Cover (10 bands); 1km Dominant Cover; 1km Dominant Aggregate Cover.
  - GB and NI versions produced for each year, yielding 42 datasets per year in total (duplicated across years as described in Appendix 5).
  - 20m Classified Pixels: two-band rasters (Band 1 = predicted class; Band 2 = confidence 0–100); preserves detailed landscape features not captured in parcel-level products.
  - Land Parcels: parcel-level attributes including gid (unique parcel id), _hist (histogram of class counts per parcel), _mode (dominant class), _purity (parcel-level proportion of modal class), _conf (mean class membership probability), _stdev (uncertainty), _n (number of pixels).
  - 25m Rasterised Land Parcels: three-band rasters (Band 1 = _mode; Band 2 = _conf; Band 3 = _purity).
  - 1km products: grid-based summaries — 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).
  - Pixel/parcel extents and coordinate systems
    - Great Britain: British National Grid, EPSG 27700.
    - Northern Ireland: Irish Grid, EPSG 29903.
  - File details and metadata are described in Tables 2–4 and Appendix 5 (full dataset list and naming).

- Classification concept and class relationships
  - 21 UKCEH Land Cover Classes derived from UK BAP Broad Habitats; most mappings provide a one-to-one or near one-to-one relationship with the BAP classes.
  - Acknowledges limitations around detection of BAP Broad Habitats from satellite data; sometimes splits (e.g., Dwarf Shrub and Heath into Heather and Heather Grassland; Built-up Areas and Gardens into Urban and Suburban) to improve detectability.
  - Appendix 1 and Appendix 2 provide detailed notes on species/habitat interpretation and detection caveats.

- Validation and accuracy
  - Validation conducted against UK countryside survey 2019 data, National Forest Inventory data, IACS, and bespoke LCM validation points (22,325 total).
  - Reported overall accuracy at national scale:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data were common across the three products; accuracy reflects currency and class-mapping differences relative to validation sources.
  - Validation tables and accuracy details (Appendix 4) note ongoing improvements and caveats about class definitions and alignment with validator datasets.

- Practical notes for users (data usage and governance)
  - Gid values for Land Parcels do not match across LCM2015 and LCM2017–2019; comparisons should use the gid for 2017–2019 parcel-level comparisons, acknowledging changes in spatial framework.
  - The Land Parcel Spatial Framework is fixed to 0.5 ha MMU; it is designed to enable change detection but may not align perfectly with all alternative parcel systems users wish to apply.
  - Bootstrap Training is designed to maximize the majority signal; some minor class changes over time may occur, but the approach supports near-continuous annual updates.
  - The dataset suite is designed to be openly accessible with detailed metadata and documentation; however, users should be aware of class definition changes and comparability issues when linking to historic maps.

- Temporal dimension and future plans
  - UKCEH aims to release a new LCM annually, with LCM2020 planned and development toward more frequent updates.
  - Considerations for satellite input and data sources include:
    - Assessment of Sentinel-2 Surface Reflectance (SR) versus Top of Atmosphere (TOA) reflectance; TOA was chosen for current classification effectiveness; continuous review planned.
    - Exploration of supplementary optical sources and Sentinel-1 radar data to fill seasonal gaps and improve classification in cloudy conditions.
  - Ongoing refinement of the UK Land Parcel Spatial Framework and potential evolution toward higher-resolution or alternative parcel definitions to support finer-scale monitoring.

- Appendix highlights (for context and interpretation)
  - Appendix 1: Notes on UKCEH Land Cover Classes (detailed class interpretations and potential confusion with BAP Broad Habitats).
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (mapped relationships to UKCEH classes).
  - Appendix 3: RGB color recipe for displaying UKCEH Land Cover Classes.
  - Appendix 4: Full confusion matrices and validation metrics for LCM2017, LCM2018, LCM2019 (summary of producer’s and user’s accuracies by class and cross-class confusion).
  - Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019 (dataset names, year associations, and storage context).