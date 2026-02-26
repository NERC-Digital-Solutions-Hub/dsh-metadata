# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose
  - User guide for three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Describe content, structure, production decisions, validation, and future plans to help users apply the data appropriately.

- What UKCEH Land Cover Classes are
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; matched to LCM2015 conventions for comparability.
  - Tables explain relationships between UKCEH classes, UK BAP Broad Habitats, and aggregated classes; some refinements exist to balance detectability with change detection.

- How the maps were produced
  - Automatic classification using Bootstrap Training plus Random Forest (RF).
  - Sentinel-2 Seasonal Composite Images (median reflectance per season) plus 20m Context Rasters used to create Classification Scenes.
  - Bootstrap Training relies on historic maps (LCM2015) to generate spectral training data; RF trained with balanced sampling (10,000 samples per class per bag).
  - Training data derived from LCM2015; future maps aim to bootstrap from majority signals across 2017–2019 (and 2018–2020 for future maps).
  - Visual checks and formal validation performed; no manual corrections applied this release to maintain rapid annual updates.
  - Aim to release a new LCM annually; future expansion may include additional data sources (e.g., Sentinel-1) to fill gaps.

- Data products and structure (42 datasets in total across Great Britain and Northern Ireland)
  - 20m Classified Pixels (GB and NI): new 20m RF classification outputs with two bands (class label and confidence 0–100); preserves detail without applying Land Parcel generalisation.
  - Land Parcels: summary attributes produced by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Key fields: gid, _hist (histogram of class counts per parcel), _mode (dominant class), _purity (percentage of modal class), _conf (mean class membership probability), _stdev, _n (number of pixels).
    - Some attribute names updated to align with production software; minor deltas from LCM2015 noted.
  - 25m Rasterised Land Parcels: three-band rasters (band1 = _mode, band2 = _conf, band3 = _purity).
  - 1km Raster Datasets (per year): 1km Percent Cover (21-band), 1km Percent Aggregate Cover (10-band), 1km Dominant Cover (1-band), 1km Dominant Aggregate Cover (1-band).
  - Seasonal Composite Images and Classification Scenes:
    - Seasonal composites from Sentinel-2 (bands 2,3,4,5,6,7,8,11,12) at 20m, with some nulls due to cloud.
    - 100x100 km GB tiles (36 spectral bands + 7 context bands) to produce 46-band GB Classification Scenes; NI uses a single 43-band scene per year.
  - The UKCEH Land Parcel Spatial Framework
    - Minimum parcel size around 0.5 ha; used to structure and reduce classification noise; parcels align with real-world land units (fields, parks, urban areas, etc.).
    - gid values differ from LCM2015 for cross-year comparisons; comparisons should use gid across LCM2017–2019.
  - Context Rasters
    - GB 20m context layers (height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland).
    - NI 20m context layers include urban mask, distance to coast, freshwater, and road.
  - Classification Scenes and Tiles
    - GB: overlapping 100x100 km tiles used to extract 36-band Seasonal Composite Images; 74 overlapping GB scenes classified independently with visual quality precedence when overlaps occur.
    - NI: single 43-band classification scene per year determined by NI land mass.

- Data quality and validation
  - Validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke validation points.
  - Validation set: 22,325 points; overall accuracy across years:
    - 2017: 78.6%
    - 2018: 79.6%
    - 2019: 79.4%
  - Validation uses a common set of points across products; not an absolute truth but a robust performance indicator.
  - About 80% correspondence overall; plan to improve with better training data and resources.

- Class framework and interpretation
  - Appendix notes explain UKCEH Land Cover Classes (21) and their relationship to BAP Broad Habitats.
  - Some categories are generalized (UKCEH Aggregate Classes) for users who require less thematic detail.
  - RGB color recipes are provided to display classes consistently.

- Datasets and metadata (Appendix 5)
  - Full list of datasets per year (LCM2017–LCM2019), including GB and NI versions of each product (20m classified pixels, land parcels, 25m raster parcels, 1km cover products, etc.).
  - Coordinate systems:
    - Great Britain: British National Grid, EPSG 27700
    - Northern Ireland: Irish Grid, EPSG 29903
  - Pixel resolution and bands:
    - 20m Classified Pixels: 2 bands (class label, confidence 0–100)
    - 25m Rasterised Parcels: 3 bands (_mode, _conf, _purity)
    - 1km rasters: multiple bands (percent cover, dominant, etc.)
  - Datasets are produced for each year and region, yielding 42 datasets in total.

- Appendices: key reference material
  - Appendix 1: Notes on UKCEH Land Cover Classes (detailed class definitions and detection notes)
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions
  - Appendix 3: Recommended color mapping for displaying classes
  - Appendix 4: Validation confusion matrices and accuracy metrics (per class; producer's and user’s accuracy)
  - Appendix 5: Detailed list of all datasets per year

- Future plans and considerations
  - Maintain annual release cadence; plans to broaden input sources (e.g., Sentinel-1 radar) and refine training data over time.
  - Potentially refine UKCEH Land Parcel Spatial Framework as higher-resolution data become available.

- Takeaway for users
  - LCM2017–2019 provide a rapid, automatically produced national set of land cover maps with 21 UKCEH classes, aligned to BAP habitats, using Bootstrap Training and RF classification on Sentinel-2 seasonal imagery with context layers.
  - A rich multi-resolution product suite (20m pixels to 1km grids) and parcel-based summaries support self-serve analysis, trend detection, and integration with spatial planning or policy work.
  - While automated and with high-level accuracy, users should review per-class performance (Appendix 4) and consider cross-year comparability constraints due to parcel ID changes.