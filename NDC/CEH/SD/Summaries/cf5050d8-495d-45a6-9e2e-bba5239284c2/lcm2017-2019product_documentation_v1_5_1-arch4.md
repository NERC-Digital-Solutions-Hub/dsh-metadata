# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide for three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Maps contain 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
  - Production is automated (Bootstrap Training + Random Forest) to enable rapid, co-registered UK-wide mapping.
  - Aims to support informed use, validation, and planning; annual releases planned with ongoing quality checks.

- Datasets and products
  - 20m Classified Pixels: new 20m RF classification results with two bands (class, confidence 0–100).
  - Land Parcels: parcel-level attributes including gid, histogram of class counts, modal class, purity, confidence, and n pixels.
  - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) representing parcel-aggregated output.
  - 1km raster products:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
  - Yearly and regional scope: separate GB and Northern Ireland (NI) datasets; total of 42 datasets.
  - Extents and coordinates:
    - GB: British National Grid (EPSG:27700)
    - NI: Irish Grid (EPSG:29903)
  - Spatial relationships and structure:
    - GB uses overlaid 100x100 km Classification Scenes; NI uses a single 43-band scene per year.
    - Outputs are aligned to UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha) but can be summarized by alternative parcel structures.

- How it was produced
  - Bootstrap Training: automated training data derived from UKCEH LCM2015; uses parcels with ≥99% purity to bootstrap classifiers for 2017–2019.
  - Random Forest classification: balanced sampling (10,000 samples per class per bag) to generate the 20m Classified Pixels product.
  - Training and classification environment: bespoke software integrating Weka, PostGIS, and GDAL.
  - Seasonal and spectral inputs:
    - Sentinel-2 Seasonal Composite Images (TOA reflectance, 20 m resolution) per season (winter, spring, summer, autumn).
    - 9 Sentinel-2 bands used; some cloud gaps exist but no manual gap filling required for overall UK map.
  - Contextual information (Context Rasters): 20m layers to reduce spectral confusion (GB: height, aspect, slope, proximity to buildings/roads/coast/freshwater, foreshore, tidal water, woodland; NI: height, aspect, slope, urban mask, distance to coast/freshwater/roads).
  - The Google Earth Engine infrastructure used to source Sentinel-2 data and generate seasonal composites.

- Data structure and metadata
  - Dataset relationships and content
    - 20m Classified Pixels: two-band raster (class, probability 0–100).
    - Land Parcels: per-parcel attributes including _hist (list of class counts per parcel), _mode, _purity, _conf, _stdev, _n.
    - 25m Rasterised Land Parcels: 3-band raster (mode, conf, purity).
    - 1km datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).
  - Geographic extents and pixel sizes
    - Classified Pixels: 20 m
    - Land Parcels: aligned to 25 m parcel rasters
    - 1 km rasters: aggregated from 25 m outputs
  - Datasets per year and region: GB and NI outputs described in Appendix 5; 42 total datasets.

- Validation and data quality
  - Validation approach: comparison with GB countryside survey (2019), National Forest Inventory, IACS, and bespoke LCM validation points (n ≈ 22,000).
  - Reported overall accuracy (GB, 21 classes):
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Notes on interpretation: validation uses legacy data with some mapping differences; results are good indicators but not absolute truths. Appendix 4 provides full validation tables.

- UK Land Parcel Spatial Framework
  - Parcels designed to represent discrete land units (~0.5 ha MMU) and to reduce classification noise.
  - gid serves as a stable parcel identifier across LCM2017–2019 (but not matched to LCM2015 parcel identifiers).
  - The framework enables change detection but is not the only possible summary structure; users can apply their own boundaries if desired.
  - Future potential: possible refinement toward finer frameworks as higher-resolution data become more available.

- Class definitions and mapping
  - UKCEH Land Cover Classes tied to BAP Broad Habitats; Appendix 1/2 elaborate definitions and caveats regarding remote-sensing detectability.
  - Table 1 maps UKCEH classes to BAP Broad Habitats; distinctions exist (e.g., Heather vs Heather Grassland) due to detection challenges.
  - Appendix 3 provides a color scheme for displaying classes.
  - Acknowledges ongoing alignment and potential refinements as detection improves.

- Seasonal inputs and future directions
  - Sentinel-2 data used to build Seasonal Composite Images; occasional cloud gaps acknowledged; exploring alternatives (e.g., Sentinel-1 SAR) for gap filling.
  - Plans for iterative improvements and potential updates to bootstrap training for future maps.
  - LCM2020 planned for 2021, with a vision to leverage a multi-year majority signal for bootstrap; continued annual releases.

- Access, governance, and documentation
  - Detailed dataset descriptions and metadata are available in the document and Appendix 5.
  - Validation and methodological references provided (RF, bootstrap, etc.), with full documentation to support user understanding and reproducibility.

- Key takeaways for data leadership
  - A scalable, automated framework produces near-daily land cover insights with 21-class taxonomy aligned to historic baselines.
  - The Bootstrap Training approach minimizes field data needs while maintaining UK-wide coverage and improving over time.
  - Outputs include both pixel-level (20 m) and parcel-aggregated (25 m, 1 km) products, enabling versatile analyses and long-term change detection.
  - The UK Land Parcel Spatial Framework provides a stable, interpretable structure for longitudinal analyses, with openness to alternative summarization strategies.
  - Validation indicates substantial accuracy (c. 79%) across years, with transparent caveats related to class definitions and dataset mappings.
  - Future work aims to reduce data gaps, enhance training data, and maintain annual release cadence to monitor land cover change dynamics.