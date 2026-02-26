# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and overview
- User guide for three new UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019).
- Each map covers 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and matches the class set used for LCM2015.
- Data produced automatically via Bootstrap Training plus Random Forest (RF) classifier.
- Sentinel-2 Seasonal Composite Images (TOA reflectance) by season are classified after combining with 20m Context Rasters.
- Aim to produce UK-wide maps annually; no manual corrections were applied this time.
- Validation shows maps are of similar quality to the latest predecessor (LCM2015), with ~80% correspondence against validation data.
- The document explains data production decisions, terminology, and future plans to help users apply the data appropriately.

## What’s included (data content and structure)
- 21 UKCEH Land Cover Classes, linked to UK BAP Broad Habitats (with careful terminology distinctions and a generalization option via UKCEH Aggregate Classes; see Appendix for mappings).
- Datasets are provided for Great Britain (GB) and Northern Ireland (NI) across multiple spatial scales, with consistent year-by-year structure.
- Coordinate systems:
  - GB: Great Britain British National Grid, EPSG: 27700.
  - NI: Irish Grid, EPSG: 29903.
- Dataset suite (per year) includes:
  - 20m Classified Pixels (new): two-band raster (class with highest probability; band 2 is the per-pixel confidence 0–100). Preserves detailed landscape features below 0.5 ha MMU.
  - Land Parcels: attributes per parcel, including gid, _hist (class frequency per parcel), _mode, _purity, _conf, _stdev, _n; slight attribute name changes from LCM2015.
  - 25m Rasterised Land Parcels: three-band raster (band 1 _mode, band 2 _conf, band 3 _purity).
  - 1km Raster datasets:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Additional context: 20m Context Rasters (GB NI differences described below) and Seasonal Composite Images derived from Google Earth Engine.
- Product structure is duplicated for each year, yielding 42 datasets in total (GB and NI across 3 years).

## Production approach and key methods
- Bootstrap Training: automatic, uses historic LCM observations (from 2015) to seed training data for current classification; aims to leverage majority signal over time.
- Random Forest (RF) classification: training samples drawn with replacement to balance classes; 10,000 samples per class per training run to produce the 20m Classified Pixels.
- Seasonal Composite Images: four-season Sentinel-2 TOA reflectance (median per season) at 20m, used with Context Rasters to form Classification Scenes.
- Context Rasters: 20m resolution layers to reduce spectral confusion (GB: height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore, tidal water, woodland; NI: height, aspect, slope, urban mask, distance to coast/freshwater/roads).
- Classification Scenes: GB uses 100×100 km overlapping tiles (36-band seasonal data + 10 context layers → 46-band scenes; 74 overlapping scenes classified independently and visually reconciled). NI uses a single 43-band scene per year for the country’s extent.
- UK Land Parcel Spatial Framework: maintained 0.5 ha MMU and parcel generalization for stable representation; gid changes mean LCM2017–2019 parcel IDs do not match LCM2015, though parcel geometry remains equivalent. The framework supports time-series comparison and pooling through parcels (gid-based matching).
- Validation and quality control: UK-scale validation against multiple sources (GB countryside survey 2019, open-source National Forest Inventory, IACS, manual validation points). Validation results indicate ~78–80% overall correspondence across 2017–2019.

## Data structure and specifics by year

- 20m Classified Pixels
  - New 20m pixel-level RF classification with per-pixel class and confidence.
  - Not generalised by the Land Parcel Framework to preserve fine detail (e.g., narrow features).

- Land Parcels
  - Attributes per parcel:
    - gid: unique parcel ID (stable within a year, not reused across LCM2015 vs 2017–2019).
    - _hist: list of class-frequency tuples per parcel (e.g., "2:3, 11:361").
    - _mode: most frequent class in the parcel.
    - _purity: percentage of the modal class within the parcel.
    - _conf: mean class-membership probability (0–100) across pixels in the parcel.
    - _stdev: standard deviation of _conf.
    - _n: total number of 20m pixels intersecting the parcel.
  - Changes from LCM2015 documented; text descriptions of attributes updated (e.g., no Composite field; no BHAB text field).

- 25m Rasterised Land Parcels
  - Bands: 3 bands
    - Band 1: _mode
    - Band 2: _conf
    - Band 3: _purity
  - Rationale: third band (purity) added to convey confidence.

- 1km Raster Datasets
  - 1km Percent Cover: 21 bands (percent cover per class).
  - 1km Percent Aggregate Cover: 10 bands (aggregate classes).
  - 1km Dominant Cover: 1 band (dominant class per 1km cell).
  - 1km Dominant Aggregate Cover: 1 band (dominant aggregate class per 1km cell).

- Seasonal and Classification Scenes
  - GB: 74 overlapping 100×100 km tiles; 46-band GB Classification Scenes per year.
  - NI: single 43-band Classification Scene per year (per minimum bounding rectangle).

## Context, classification, and visualization
- Context Rasters help resolve spectral confusion (e.g., distinguishing coastal or urban contexts).
- GB Context Rasters include terrain (Height, Aspect, Slope), proximity (buildings, roads, sea, freshwater), foreshore, tidal water, woodland.
- NI Context Rasters include terrain plus urban mask and proximity layers (coast, freshwater, roads).

## Data use, standards, and metadata considerations
- 21 UKCEH Land Cover Classes are standard across years; a UKCEH Aggregate Class set provides generalization when needed.
- BAP Broad Habitats names are italicized for clarity; defined class relationships are detailed in Appendix 1 and 2.
- The Land Parcel Spatial Framework remains the standard for parcel-based comparison, but comparisons to LCM2015 require gid-based linkage (parcels have different gid values between products).
- MMU and spatial resolution considerations: parcels ~0.5 ha MMU; 20m classification preserves fine features; 25m rasterised parcels aggregate to 1km rasters for summary products.

## Validation results and caveats
- Validation dataset: 22,325 points across LCM2017, LCM2018, LCM2019.
- UK-scale accuracy:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation points span multiple sources; label mapping from external datasets to UKCEH classes involves some subjectivity.
- Validation figures reflect currency of validation data and year-specific comparisons; changes in class definitions could affect exact correspondences.

## Appendix highlights and references (high level)
- Appendix 1 and 2: Detailed notes on UKCEH Land Cover Classes and UK BAP Broad Habitats definitions (with nuances and detection considerations for remote sensing).
- Appendix 3: Recommended RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Full confusion matrices and accuracy statistics per year (LCM2017–LCM2019) including producer’s and user’s accuracies.
- Appendix 5: Full list of datasets per LCM2017, LCM2018, and LCM2019 (dataset names, GB/NI scope, and storage references).
- References: foundational sources for RF, bootstrap training, Sentinel-2 processing, and UK habitat classifications.

## Future plans and ongoing development
- Annual LCM releases with ongoing improvements; 2020 plan references bootstrap updates (e.g., 2020 bootstrap from 2017–2019 majority signal).
- Potential expansion of input data (e.g., including Sentinel-1 SAR) and refinement of training data as new observations and higher-resolution inputs become available.
- Continued validation resource development to improve comparability and accuracy.