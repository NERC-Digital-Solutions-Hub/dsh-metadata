# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview and purpose
- Release of three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Each map represents 21 UKCEH Land Cover Classes (aligned with 2015 scheme; based on Biodiversity Action Plan Broad Habitats) and is produced automatically.
- Methodology centers on Bootstrap Training with a Random Forest classifier to produce near real-time, annual UK-wide maps.
- Aims to help users understand and map land cover dynamics; annual updates facilitate change detection.

## Data products and structure
- Datasets provided for Great Britain and Northern Ireland, year-specific, creating a total of 42 datasets (GB and NI for 2017, 2018, 2019).
- Dataset families (per year) and formats:
  - 20m Classified Pixels: new 2-band rasters (class and per-pixel confidence 0–100); preserves detailed, narrow features; not generalised by parcel framework.
  - Land Parcels: parcel-level attributes derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; includes gid, _hist (per-class pixel histogram), _mode, _purity, _conf, _stdev, _n; some attribute name changes for production consistency.
  - 25m Rasterised Land Parcels: 3-band rasters (band1 _mode, band2 _conf, band3 _purity).
  - 1km Raster Products: summary rasters derived from 25m parcels:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Class relationships: 21 UKCEH Land Cover Classes anchored to BAP Broad Habitats; generalised Aggregate Classes provided for some users; mapping tables describe relationships and nuances.

## Production methodology
- Bootstrap Training: uses historic, stable land cover observations (from LCM2015, bootstrap-derived) to automatically generate spectral training data for current Sentinel-2 seasonal composites; supports rapid year-to-year mapping without field data collection.
- Random Forest classification: supervised learning using balanced sampling (10,000 samples per class per classification scene); produced with custom UKCEH software integrating WEKA, PostGIS, and GDAL.
- Sentinel-2 seasonal composites: four-season TOA reflectance mosaics at 20m, derived from Google Earth Engine; seasons: winter, spring, summer, autumn.
- Context rasters (20m GB; 20m NI): include terrain (height, aspect, slope) and proximity/land-use context (buildings, roads, coast, freshwater, urban). NI uses a reduced set of context layers.
- Classification Scenes and tiling: GB classified in overlapping 100x100 km tiles to manage phenological variation and processing; NI uses a single 43-band scene per year.
- Land Parcel Spatial Framework: 0.5 ha minimum parcel size; framework used to summarise 20m pixels into parcels; gid identifiers are reset across years, complicating parcel-based year-to-year comparisons except via gid-based cross-year matching.

## Dataset details and attributes (highlights)
- 20m Classified Pixels: 20m, 2-band rasters; contains most detailed per-pixel classifications and confidence.
- Land Parcels: key attributes include gid, _hist (per-class pixel counts), _mode, _purity, _conf, _stdev, _n; attribute names align with production conventions.
- 25m Rasterised Land Parcels: 3-band rasters (dominant class, confidence, parcel purity).
- 1km Datasets:
  - 1km Percent Cover: 21-band raster (per-class percentage cover per 1km cell).
  - 1km Percent Aggregate Cover: 10-band raster (aggregate class coverage per 1km).
  - 1km Dominant Cover: single-band raster (dominant class per 1km).
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate class per 1km).
- Extents and projections:
  - Great Britain: British National Grid, EPSG 27700.
  - Northern Ireland: Irish Grid, EPSG 29903.
- MMU and parcel framework: parcels derived to reflect land units (approx. 0.5 ha MMU); framework supports consistent reduction of detail and change detection over time.

## Validation and accuracy
- Product validation against independent sources (GB countryside survey 2019, National Forest Inventory, IACS, manual validation points).
- Total validation points: 22,325; overall accuracies observed:
  - LCM2017: approximately 78.6%
  - LCM2018: approximately 79.6%
  - LCM2019: approximately 79.4%
- Validation uses a single validation dataset across all three products; accuracy metrics reflect alignment with UKCEH classes after mapping from external schemes.
- No manual corrections were applied in these releases to maintain annual, automatic production; visual checks and formal validation were performed.

## Class definitions and resources
- Appendix resources define UKCEH Land Cover Classes and their relation to UK BAP Broad Habitats; notes clarify detection limitations (e.g., upland peatlands, Bracken vs Acid Grassland) and the intent to maintain a consistent change-detection framework.
- Appendix 3 provides a recommended RGB color recipe for displaying classes.
- Appendix 5 lists the full dataset inventory for each year and region.

## Practical use, cautions, and guidance
- The 20m Classified Pixels dataset preserves landscape detail at the cost of larger data volumes; suitable for detailed mapping and downstream parcel summarisation.
- Land Parcels and 25m Rasterised Land Parcels provide convenient summaries aligned to fixed spatial units; caution when comparing to LCM2015 due to gid changes and spatial framework revisions.
- 1km products enable broad-scale analyses and rapid change assessment; not a direct substitute for higher-resolution classes where fine-scale patterns are critical.
- The class set is designed for compatibility with past UKCEH maps while acknowledging remote-sensing limitations; context rasters help reduce spectral confusion.

## Future plans and development
- UKCEH aims to release a new LCM annually; 2020 vision (LCM2020) to build on bootstrap from 2017–2019 majority signal; potential expansions to input data and upland vegetation detection.
- Ongoing evaluation of training data strategies and validation resources to improve accuracy over time.

## Appendices and references
- Appendices detail class definitions (UKCEH Land Cover Classes and UK BAP Broad Habitats), color schemes, and validation confusion matrices; references include foundational works on Random Forests and the historical context of the LCM series.