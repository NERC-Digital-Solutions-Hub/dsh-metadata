# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Presents three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Each map suite uses 21 UKCEH Land Cover Classes (aligned with BAP Broad Habitats concepts) and is produced automatically using Bootstrap Training plus Random Forest.
  - Data generated from Sentinel-2 Seasonal Composite Images (4 seasons) plus 20m Context Rasters; annual production with plans for yearly updates.
  - No manual corrections were applied this cycle; visual checks and formal validation were performed; map quality is comparable to LCM2015.

- Production approach and methods
  - Bootstrap Training: uses historic LCM data (LCM2015) to bootstrap training observations; selects high-purity land parcels (≥99%) to train the model; aims to leverage majority signal across time.
  - Random Forest classification: trains on balanced samples (10,000 per class) to produce the 20m Classified Pixels product; outputs a per-pixel class plus a probability-based confidence metric.
  - Future direction: planned bootstrap strategies will use majority signals over 2017–2019 and 2018–2020 for subsequent maps.

- Data structure and datasets
  - 20m Classified Pixels: first-ever 20m pixel classification dataset; 2 bands per pixel (class and confidence 0–100); preserves fine landscape detail without parcel generalisation.
  - Land Parcels: parcel-based attributes derived from the 20m dataset within the UKCEH Land Parcel Spatial Framework; key fields include gid, _hist (histogram of pixel counts per class), _mode (dominant class), _purity, _conf, _stdev, and _n; 21 classes; some attribute naming changes from LCM2015.
  - 25m Rasterised Land Parcels: three-band raster (band1 = _mode, band2 = _conf, band3 = _purity) derived from the Land Parcels.
  - 1km Rasters:
    - 1km Percent Cover: 21-band raster giving the percentage cover of each UKCEH Land Cover Class per 1km.
    - 1km Percent Aggregate Cover: 10-band raster for aggregate class percentages per 1km.
    - 1km Dominant Cover: single-band raster showing the dominant class per 1km.
    - 1km Dominant Aggregate Cover: single-band raster for dominant aggregate class per 1km.
  - Geographic scope: Great Britain (GB) and Northern Ireland (NI); each dataset has corresponding GB/NI versions; GB uses 27700 (British National Grid) and NI uses 29903 (Irish Grid) coordinate systems.

- Spatial framework and parcel context
  - UKCEH Land Parcel Spatial Framework: used to group 20m Classified Pixels into land parcels (~0.5 ha MMU); unchanged geometries from LCM2015 but with re-ordered storage and new indices for faster processing; gid values do not match LCM2015 for cross-year parcel comparisons (use gid for year-to-year comparisons within 2017–2019 series).
  - Parcel counts: GB ~6.7 million parcels; NI ~0.9 million parcels; all parcels represent discrete land units (fields, urban areas, etc.).

- Classification scenes and satellite input
  - Seasonal Composite Images: generated with Google Earth Engine from Sentinel-2 TOA reflectance (four seasons); 20m pixels; Section notes potential cloud gaps; classification tolerant to partial data.
  - Context rasters: 20m GB context rasters (height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water, woodland); NI context rasters (height, aspect, slope, urban mask, coast/freshwater/road distances).
  - GB Classification Scenes: 100x100 km tiles; 74 overlapping scenes classified independently to cover GB; NI uses a single 43-band scene per year.

- Output and interpretation
  - Classifications produce a map of 21 UKCEH Land Cover Classes (plus administrative notes about BAP relationships); Appendix 1–2 provide detailed class descriptions and detection considerations.
  - The 20m Classified Pixels retain finer landscape detail (e.g., narrow features) compared to the 25m Land Parcels, which are more generalised.
  - 25m Rasterised Land Parcels provide a harmonised, parcel-based summary suitable for change detection and map display at a coarser scale.
  - 1km rasters enable rapid, landscape-scale summaries (percent cover, dominant class) for broad-scale analyses.

- Validation and quality
  - Validation against multiple sources (GB Countryside Survey 2019, National Forest Inventory, IACS, and bespoke validation points) with 22,325 validation points used to assess correspondence.
  - Overall accuracy at national scale:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation notes: point data are not perfect ground truth; some mismatches due to class mapping and data source differences; ~80% correspondence indicates solid performance with room for improvement.

- Class relationships and terminology
  - LCM2017–2019 map 21 UKCEH Land Cover Classes, tied to UK BAP Broad Habitats; most mappings are one-to-one, with a few refinements (e.g., Urban vs Suburban, specific habitat splits); Appendix notes explain naming conventions and potential ambiguities.
  - The guide uses capitalised UKCEH terms to denote defined classes and italicises UK BAP Broad Habitats when referring to BAP concepts to reduce ambiguity.

- Practical notes for GIS users
  - Data release comprises 42 datasets (GB and NI across three years) at multiple resolutions; the 20m Classified Pixels dataset is the most detailed product and serves as the basis for all summary datasets.
  - When comparing maps across years, use the gid field within the UKCEH Land Parcel Spatial Framework for parcel-level comparisons; direct parcel-id matching with LCM2015 is not supported.
  - Expect some minor attribute changes (e.g., naming conventions) between LCM2017–2019 and LCM2015; the core class set and mapping keep consistency for time-series analysis.
  - Users should consider contextual and seasonal data limitations (cloud gaps, TOA vs SR debate) and potential future enhancements (e.g., incorporation of SAR data for gap filling).

- Accessibility and references
  - Data production relies on open-source components (Weka, PostGIS, GDAL) and Google Earth Engine for seasonal composites.
  - The document includes extensive appendices detailing class definitions, color mappings, and validation results to support application in GIS workflows.