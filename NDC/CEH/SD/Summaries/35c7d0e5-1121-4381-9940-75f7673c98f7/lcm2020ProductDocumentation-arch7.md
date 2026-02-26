# The UKCEH Land Cover Map for 2020

- Purpose: User guide for LCM2020, detailing that the product comprises six datasets (three for Great Britain and Northern Ireland): 10m classified pixels, land parcels, and 25m rasterised land parcels (with NI also documented for a 20m classified raster option in Appendix notes). The guide explains data production, validation, and accuracy to help users apply UKCEH LCM2020 data in current or future work.

- Product suite (datasets and structure):
  - 10m Classified Pixel datasets (GB and NI): classification scenes produced from Sentinel-2 Seasonal Composite Images plus 10 Context Rasters; each pixel’s first band stores the most likely UKCEH Land Cover Class, and the second band stores the associated class probability/confidence.
  - Land Parcel datasets (GB and NI): derived by intersecting the 10m classified pixels with the UKCEH Land Parcel Spatial Framework; includes parcel-level attributes (e.g., _hist, _mode, _purity, _conf, _stdev, _agg, _n) and a fixed spatial framework with a minimum area of ~0.5 ha (MMU).
  - 25m Rasterised Land Parcel datasets (GB and NI): rasterised per-parcel outputs with 3 bands: dominant land cover (mode), mean confidence (conf), and parcel purity (purity).
  - NI additional note: Appendix 5 references an NI-specific 20m Classified Raster Product as an additional dataset option.
  - Dataset metadata: GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (EPSG: 29903); parcel counts and extents provided (GB ~6.74 million parcels; NI ~0.90 million parcels).

- Classification and data production workflow:
  - Classification Scenes: GB uses 100x100 km tiles, producing 74 overlapping scenes to cover the GB land surface; NI uses a single 100x100 km tile derived from the minimum bounding rectangle of NI land mass.
  - Seasonal and contextual inputs: Classification Scenes combine Sentinel-2 Seasonal Composite Images (winter, spring, summer, autumn) with 10 Context Rasters to reduce spectral confusion.
  - Bootstrap Training: Automatic, historical maps (2017–2019) provide training data; training samples filtered to high-purity parcels (>99% across three years), yielding about 941k GB and 214k NI training objects.
  - Random Forest: Balanced sampling (10,000 samples per class per training bag) to train the RF classifier; outputs the 10m Classified Pixel dataset.
  - Automation emphasis: Annual production reduces manual corrections; aims to differentiate real change from random classification noise via time series.

- Validation and accuracy:
  - Validation approach: 34,715 validation points derived from GB countryside surveys (2019–2020), National Forest Inventory, IACS data, and bespoke image-interpretation points; these were intersected with Land Parcel datasets to assess accuracy.
  - Overall accuracy: 79.2% at full thematic detail (Appendix 4).

- Land cover classes and relationships:
  - 21 UKCEH Land Cover Classes, tied to Biodiversity Action Plan (BAP) Broad Habitats but not identical to BAP definitions; differences acknowledged and bridged with guidance.
  - Classes are described with capitalised terms for consistency; some BAP Broad Habitats are split or merged to form UKCEH classes (e.g., Heather vs Heather Grassland; Urban vs Suburban).
  - For users needing generalised classifications, UK CEH Aggregate Classes are provided in Land Parcel products.

- Context and methodology notes:
  - Context rasters help resolve spectral confusion (e.g., bare rocks, urban surfaces) using terrain, proximity to features, and land-use masks.
  - Seasonal signals and context layers enable robust discrimination of vegetation and land cover types.
  - Bootstrap Training relies on wall-to-wall coverage from historic maps, acknowledging that some training data may be outdated for newly changed areas; the majority signal guides classification.

- Data quality and interpretation guidance:
  - All land cover products have errors; early manual corrections are not performed to maintain annual production pace.
  - Annual maps help distinguish real change from random errors; most classification errors are random in space/time and should not repeat at the same locations year after year.
  - The Land Parcel Spatial Framework has been updated since LCM2015, so parcel identifiers (gid) may not align for direct year-to-year parcel-based comparisons; spatial overlap remains valid for most analyses.

- Practical guidance for GIS work:
  - Use cases include monitoring state and change of the UK countryside and supporting environmental objectives; the 10m pixel data preserves fine features (e.g., narrow patches) not generalised by the parcel framework.
  - Be aware of the 0.5 ha MMU when working with parcels; parcels are designed to provide stable units for time-series analysis.
  - Data use should consider the 21-class structure, potential class confusions described in the Appendices, and the recommended color recipes for display.

- Appendix highlights (what to consult for implementation details):
  - Appendix 1: Notes on UKCEH Land Cover Classes (descriptions and interpretation notes per class).
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats and their relationship to UKCEH classes.
  - Appendix 3: Recommended color recipes for displaying UKCEH Land Cover Classes.
  - Appendix 4: Detailed validation matrices including user’s and producer’s accuracies by class.
  - Appendix 5: Full list of datasets and official dataset names, extents, and metadata for LCM2020 (including 10m classified, land parcel, 25m rasterised parcels, and NI 20m variant).