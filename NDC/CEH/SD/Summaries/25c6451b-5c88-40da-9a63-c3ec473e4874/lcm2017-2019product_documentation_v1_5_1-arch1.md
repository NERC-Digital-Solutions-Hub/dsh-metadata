# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map presents 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with content matching but not claiming exact equivalence to BAP classes.
  - Maps produced automatically using Bootstrap Training with a Random Forest classifier; aim for annual releases moving forward.
  - Validation and visual checks indicate the maps are of comparable quality to the latest predecessor (LCM2015); no manual corrections were applied this time.

- Data inputs and classification approach
  - Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) used to generate 4-season data (winter, spring, summer, autumn).
  - Seasonal data combined with 20m Context Rasters to create Classification Scenes.
  - Context Rasters include terrain (Height, Aspect, Slope) and proximity metrics (distance to buildings, roads, sea, freshwater) and coastal/foreshore indicators.
  - Google Earth Engine used to generate Seasonal Composite Images; SR (land surface reflectance) data considered but TOA adopted because SR offered no improvement for this classification task.
  - Classification Scenes: GB produced as overlapping 100x100 km tiles (74 scenes total); NI produced as a single 43-band scene per year.

- Bootstrap Training and modeling
  - Bootstrap Training: fully automatic, using historic maps as training data to bootstrap the next map; relies on majority signals across time to mitigate small changes in land cover.
  - Bootstrap Training for 2017–2019 derived from LCM2015; selects parcels with high purity (≥99%) to sample spectral training observations.
  - Random Forest classifier trained with balanced sampling (10,000 samples per class per scene) to ensure rare classes are learned effectively.
  - Production software integrates Weka (machine learning) with PostGIS and GDAL (open-source tools).

- UK Land Parcel Spatial Framework and MMU
  - UKCEH Land Parcel Spatial Framework unchanged in geometry but reindexed for faster processing; gid identifiers differ from LCM2015 (use gid for cross-product comparisons).
  - Land Parcels have a minimum mapped unit of ~0.5 hectares (MMU); parcels generally dominated by a single land cover type.
  - Framework enables consistent change-detection and provides a fixed structure for inter-annual comparisons; users can alternatively summarize 20m pixels using their own parcel boundaries.

- Outputs and dataset structure
  - 42 datasets in total (GB and NI) across years; designed to support different scales and users.
  - 20m Classified Pixels (new): 2-band rasters; band 1 = class with highest membership probability; band 2 = probability (0–100) indicating classification confidence.
  - Land Parcels: 2 attributes (gid and _hist) plus derived attributes; notes on changes from LCM2015 and schema updates.
  - 25m Rasterised Land Parcels: 3-band rasters; bands = _mode (dominant), _conf (confidence), _purity (per-parcel proportion).
  - 1km Raster datasets:
    - 1km Percent Cover: 21-band raster (percentage cover per class).
    - 1km Percent Aggregate Cover: 10-band raster (percent cover per UKCEH Aggregate Class).
    - 1km Dominant Cover: 1-band raster (dominant class per 1km cell).
    - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km cell).
  - Pixel resolutions and extents
    - 20m Classified Pixels (GB and NI versions)
    - 25m Rasterised Land Parcels
    - 1km raster outputs
  - Coordinate systems
    - GB: EPSG 27700 (British National Grid)
    - NI: EPSG 29903 (TM75 Irish Grid)

- Dataset specifics and interpretation
  - 20m Classified Pixels preserve finer landscape detail (e.g., narrow features) but are not generalised by parcel boundaries.
  - Land Parcels summarise 20m results within the Land Parcel Spatial Framework; attributes include histogram of class counts, modal class, purity, confidence, and pixel counts.
  - 25m Rasterised Land Parcels aggregate parcel data to 25m cells, providing a coarser overview with a third band for parcel purity.
  - 1km outputs illustrate generalisation effects (compare 1km Dominant with 25m parcel data) and provide per-class coverage data for larger-scale analyses.

- Production notes, limitations, and future plans
  - No manual corrections applied this cycle to enable annual production; visual checks and formal validation still performed.
  - Validation against GB Countryside Survey 2019, National Forest Inventory, IACS, and bespoke validation points (22,325 total).
  - Reported accuracy (UK scale, 21-class maps):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data recognize potential mismatches in class definitions and currency of points; results are best-available indicators rather than absolute truth.
  - Future improvements contemplated include expanding input data sources (e.g., Sentinel-1 radar, alternative optical sources) to address gaps and gaps filling, and continuing to refine bootstrap strategies (e.g., 2020 bootstrap from 2017–2019 majority signal).

- Appendices and supporting materials (overview)
  - Appendix 1: Notes on UKCEH Land Cover Classes and UK BAP Broad Habitats; guidance on class derivations and detection challenges (e.g., upland peat, bracken, brackish waters).
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions.
  - Appendix 3: Recommended RGB color mapping for displaying UKCEH Land Cover Classes; example confusion matrix from LCM2017.
  - Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019 (dataset titles and GB/NI scope).