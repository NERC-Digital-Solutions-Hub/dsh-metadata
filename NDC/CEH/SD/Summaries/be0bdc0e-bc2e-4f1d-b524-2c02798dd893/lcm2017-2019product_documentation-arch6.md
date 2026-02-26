# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Overview
  - Release of three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Map content uses 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed to be compatible with earlier maps (LCM2015/2007/2000) for change detection.
  - Production is fully automated using Bootstrap Training and a Random Forest classifier; aimed at rapid, annual UK-wide mapping.
  - Sentinel-2 Seasonal Composite Images (TOA reflectance) processed in Google Earth Engine, combined with 20m Context Rasters to form Classification Scenes for classification.
  - No manual corrections were performed this release; visual checks and formal validation were still carried out.

- Key datasets and structure
  - 42 total datasets across GB and Northern Ireland, mirroring the 2015 product family with an additional 20m Classified Pixels dataset.
  - 20m Classified Pixels (GB and NI): new, two-band rasters per year; band 1 = predicted class, band 2 = confidence (0–100). Preserves landscape detail (no generalisation by land parcel framework).
  - Land Parcels (GB and NI): attributes describing parcel-level composition (see below); used to derive 25m raster and 1km products.
  - 25m Rasterised Land Parcels: 3-band rasters (band 1 = modal class, band 2 = conf, band 3 = purity).
  - 1km rasters: 
    - 1km Percent Cover (21 bands) 
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - Classification outputs are provided in GB and NI with appropriate coordinate systems (GB: EPSG 27700; NI: EPSG 29903).
  - 1km products use summary over 1km grids; coastal areas near 100% area coverage may yield totals that slightly diverge from 100 due to pixel aggregation.

- Spatial framework and classification approach
  - UK Land Parcel Spatial Framework used to group 20m classified pixels into parcels (minimum mapping unit ~0.5 ha). Parcels provide fixed units for time-series comparison.
  - Lands within the Land Parcel Framework are not identical to LCM2015 parcels; gid values differ, though the parcels exist in the same framework and can be related via spatial overlap.
  - Bootstrap Training: uses historic LCM2015 parcels with high purity (≥99%) to automatically sample current imagery for RF training. The bootstrap can propagate the dominant signal forward to subsequent maps, enabling rapid updates.
  - Random Forest classification: 10,000 samples per class drawn with replacement to train the RF; employs a bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL.
  - Classification Scenes and tiling:
    - GB: 74 overlapping 100x100 km Classification Scenes used to extract Sentinel-2 Seasonal Composite Images (four seasons) and contextual layers; overlaps allowed multiple classifications in a region with visual precedence used to select the best results.
    - NI: a single 43-band Classification Scene per year (36 spectral bands + 7 context layers).
  - Context Rasters (20m): GB includes height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, and a woodland mask; NI includes height, aspect, slope, urban mask, coast, freshwater, road.

- Seasonal imagery and data inputs
  - Seasonal Composite Images derived from Google Earth Engine: median TOA reflectance per season from Sentinel-2 (bands 2,3,4,5,6,7,8,11,12 at 20m for classification; some gaps due to cloud are represented as null).
  - TOA was used (not surface reflectance) after evaluation; ongoing review of input data types, with potential SAR and alternative sources in the future.

- Dataset descriptions and differences from previous releases
  - 20m Classified Pixels: new product; preserves local detail (e.g., narrow features) by avoiding aggregation with Land Parcels; provides per-pixel class with a per-pixel confidence value.
  - Land Parcels: attributes include gid, _hist (histogram of class frequencies within parcel), _mode (dominant class), _purity (percentage of modal class within parcel), _conf (mean class membership probability within parcel), _stdev (uncertainty), _n (npix). Some attribute names changed since LCM2015 to align with production software; the gid values do not match LCM2015 parcels, though spatial overlaps remain usable for time-series comparisons.
  - 25m Rasterised Land Parcels: three bands (mode, conf, purity) derived from Land Parcels.
  - 1km products: percentage cover, aggregate cover, and dominant classes for 1km cells; rounding may cause minor sums to diverge from 100 due to pixel aggregation and edge effects.
  - The 21 UKCEH Land Cover Classes map to a set of broader UK BAP Habitat concepts; Appendix 1/2 explain these mappings and the interpretational caveats for satellite-based detection.
  - Appendix 3/4 provide recommended color schemes for display (including color-blind friendly versions in Appendix 4).

- Validation and accuracy
  - UK-scale validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke LCM validation points (n ≈ 22,325).
  - Reported overall accuracies:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation data are not absolute truth; some class mappings require expert interpretation and conversions from other schemes. The validation set currency varies by product.

- Data use, limitations, and future directions
  - Outputs emphasize self-serve data products (20m Classified Pixels, Land Parcels, 25m Rasterised Parcels, and 1km rasters) for broad-scale land cover analysis and change detection.
  - Some known challenges and caveats:
    - Classification errors are assumed to be randomly distributed; real land cover changes should persist against background noise as the time series grows.
    - Saltwater vs Freshwater distinctions near coasts can be confounded by coastal context layers; upland peatland and dynamic vegetation types remain difficult to separate spectrally.
    - The Land Parcel Spatial Framework may evolve; future products may use a finer or different parcel framework as data and training data improve.
  - Future plans:
    - Continue the annual release cycle (LCM2020 planned for 2021; bootstrap strategy will use majority signals across 2017–2019 for 2020 and across 2018–2020 for 2021).
    - Explore expanding the range of input data and training data to improve classification for challenging habitat types (e.g., upland vegetation, peatland).

- Appendices and extra context (highlights)
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats – overview of definitions and the relationship to UKCEH Land Cover Classes.
  - Appendix 3/4: Colour recipes for displaying UKCEH Land Cover Classes (including color-blind friendly version in Appendix 4).
  - Appendix 5: Confusion matrices for LCM2017/2018/2019 (detailed class-by-class accuracies and producer/user accuracies).
  - Appendix 6: Full list of datasets per year and their metadata, including GB and NI variants.