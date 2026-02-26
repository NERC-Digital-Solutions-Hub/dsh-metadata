# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- Purpose and scope
  - Release of three new UKCEH Land Cover Maps: LCM2017, LCM2018 and LCM2019.
  - Each map includes 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) aligned with earlier maps (LCM2015; similar to LCM2007/LCM2000).
  - Maps produced automatically using Bootstrap Training with a Random Forest classifier; intended to enable near-annual UK-wide land-cover mapping.
  - No manual corrections were performed this time; visual checks and formal validation were still conducted and found to be comparable in quality to LCM2015.
  - The document explains data structure, production choices, validation, and future plans to support informed use.

- Class system and terminology
  - 21 UKCEH Land Cover Classes; also an option of UKCEH Aggregate Classes (10) for generalized use.
  - Classes are anchored to UK BAP Broad Habitats but are not exact field-level BAP classifications; emphasis on compatibility for change detection and remote sensing.
  - Clear conventions on capitalized class names and italicized BAP Broad Habitats to reduce ambiguity.

- Data products and dataset structure
  - In total, 42 datasets (three years × GB and Northern Ireland) across multiple product types.
  - 20m Classified Pixels
    - New addition; 2-band, 8-bit rasters.
    - Band 1 = most likely UKCEH Land Cover Class; Band 2 = confidence (0–100) of Band 1.
    - Preserves fine landscape detail (no generalisation by the Land Parcel Spatial Framework).
  - Land Parcels
    - Derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Attributes include: gid, _hist (histogram of pixel-class counts within parcel), _mode, _purity, _conf, _stdev, _n.
    - Some attribute names differ from LCM2015; gid values do not match LCM2015 but can be compared via gid for LCM2017–2019.
  - 25m Rasterised Land Parcels
    - Rasterised to 25m pixels; 3 bands: _mode, _conf, _purity.
    - Includes the parcel-averaged confidence and a third band for purity (improved over LCM2015 which used only two bands).
  - 1km Raster Datasets
    - 1km Percent Cover: 21-band, 8-bit raster showing percentage cover per class in 1km grid.
    - 1km Percent Aggregate Cover: 10-band, 8-bit raster for aggregate classes per 1km.
    - 1km Dominant Cover: 1-band raster of the dominant class per 1km square.
    - 1km Dominant Aggregate Cover: 1-band raster for dominant aggregate class per 1km.
  - Spatial extents and coordinates
    - Great Britain (GB): EPSG:27700 (British National Grid); extents Min East 0 to Max East 700000, Min North 0 to Max North 1300000.
    - Northern Ireland (NI): EPSG:29903 (Irish Grid); extents restricted to NI region.
    - Pixel sizes: Classified Pixels 20m; Land Parcels 25m; Percent/Additional rasters 1km.

- Spatial framework and parcel identifiers
  - UKCEH Land Parcel Spatial Framework remains unchanged in parcel count and geometry from LCM2015, but storage is reorganised with new indices.
  - gid is a stable parcel identifier across LCM2017–2019, but parcel geometries and IDs do not match LCM2015 parcel IDs.
  - Land parcels have a minimum area of ~0.5 hectares (minimum mappable unit).

- Seasonal imagery and input data
  - Seasonal Composite Images created from Google Earth Engine using Sentinel-2 data (TOA reflectance, median per season).
  - Four seasons: winter, spring, summer, autumn; 9 Sentinel-2 bands used (2, 3, 4, 5, 6, 7, 8, 11, 12).
  - Cloud gaps exist but the classifier tolerates partial data; future work may incorporate Sentinel-1 SAR data for cloud resilience.
  - TOA data were used (not SR) as SR did not improve classification for current classes; potential changes considered for higher thematic detail.

- Context rasters and classification scenes
  - Context Rasters (GB 20m): height, aspect, slope, distance to buildings, roads, sea, freshwater, foreshore mask, tidal water mask, woodland mask.
  - NI context rasters include urban mask, coast, freshwater, and road distance.
  - Classification Scenes
    - GB: 74 overlapping 100x100 km tiles used to extract 36-band Seasonal Composite Images; combined with context rasters to create 46-band GB Classification Scenes.
    - NI: a single 43-band (36 spectral + 7 context) Classification Scene per year determined by NI’s bounding tile.
  - Each Classification Scene is trained and classified independently; overlaps may produce minor variations; visual inspection determines final results.

- Bootstrap Training and Random Forest
  - Bootstrap Training: fully automatic training using historic LCM observations to sample spectral training data; relies on majority signal over time to train the RF classifier.
  - Training data for 2017–2019 derived from LCM2015 • sampling 20m pixels per class; balanced sampling to ensure rare classes are learned well.
  - RF classification performed with 10,000 samples per class; implemented with bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.

- Validation and accuracy
  - UK-scale validation against multiple data sources (GB Countryside Survey 2019 data, National Forest Inventory, IACS, bespoke LCM validation points): 22,325 points in total.
  - Reported overall accuracy (agreement with UKCEH Land Parcel datasets):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data are not treated as absolute truth; discrepancies arise from class definition differences and historical data alignment. Validation tables are provided in Appendix 4.

- Visualization and colour encoding
  - Appendix 3 provides recommended RGB colour mappings for the 21 UKCEH Land Cover Classes; used to visually interpret maps.

- Appendix highlights (context for use)
  - Appendix 1: Notes on UKCEH Land Cover Classes (differences, detection considerations, and class-specific caveats).
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (for readers needing habitat context).
  - Appendix 5: Full dataset lists for LCM2017, LCM2018 and LCM2019.

- Practical implications and future directions
  - The automatic, annual workflow enables rapid production of up-to-date land cover maps at UK scale, with attention to maintaining consistency with earlier class schemes for change detection.
  - Future work may include expanding input data types (e.g., Sentinel-1 SAR), refining bootstrap training, and exploring higher-resolution or alternative parcel frameworks.
  - Users should be aware of the changes in parcel identifiers compared with LCM2015 when conducting time-series analyses; comparisons across 2017–2019 use gid as the linking attribute.

- Summary takeaway for GIS use
  - LCM2017, LCM2018 and LCM2019 provide a consistent, automated, 21-class land cover framework with detailed 20m pixel information, parcel-based summaries, and multiple 1km summaries, supported by explicit validation and documentation to aid appropriate application in policy, planning, and public-facing mapping.