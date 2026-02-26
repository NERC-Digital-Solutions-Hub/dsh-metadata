# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and scope
- Presents three new UKCEH Land Cover Maps: LCM2017, LCM2018, LCM2019.
- Each map includes 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; designed to support annual, UK-wide change monitoring.
- Production is fully automatic, using Bootstrap Training + Random Forest; annual updates planned.
- Aims to help users assess environmental condition and policy performance over time with standardized outputs.

## Data content and structure
- Product suite totals 42 datasets (GB and NI for each year): 
  - 20m Classified Pixels
  - Land Parcels
  - 25m Rasterised Land Parcels
  - 1km Dominant Cover
  - 1km Dominant Aggregate Cover
  - 1km Percent Cover
  - 1km Percent Aggregate Cover
- GB and NI versions exist for applicable datasets; some 1km products are not available for NI in certain years.
- 20m Classified Pixels
  - 2-band rasters: band 1 = nominated UKCEH Land Cover Class; band 2 = membership probability (0–100) for confidence.
  - Preserves fine detail (not generalised by parcel framework).
- Land Parcels
  - Attributes per parcel: gid (stable within this release), _hist (histogram of class counts per parcel), _mode (dominant class), _purity (dominant share), _conf (mean per-pixel membership probability), _stdev (uncertainty), _n (pixel count).
  - Minor attribute changes vs LCM2015; notes on field naming alignment.
- 25m Rasterised Land Parcels
  - 3 bands: _mode (dominant class), _conf (confidence), _purity (parcel-level purity).
  - Provides a summarized, parcel-based view of the 20m classifications.
- 1km rasters
  - 1km Percent Cover: 21-band raster (percent cover per class).
  - 1km Percent Aggregate Cover: 10-band raster (cover by UKCEH Aggregate Classes).
  - 1km Dominant Cover: single-band raster (dominant class per 1km cell).
  - 1km Dominant Aggregate Cover: single-band raster (dominant aggregate class per 1km cell).
- Dataset structure is provided for GB and NI, with corresponding coordinate systems (GB: EPSG 27700; NI: EPSG 29903).

## Production methodology
- Bootstrap Training
  - Fully automated training from historic UKCEH LCMs (LCM2015) to bootstrap training data for 2017–2019.
  - Selection of high-purity parcels (≥99% purity) from LCM2015 to form training samples.
  - Intends to update bootstrap strategy for future maps (e.g., 2020 uses 2017–2019 majority signal; 2021 will use 2018–2020 majority).
- Random Forest classification
  - Training samples: 10,000 per class, drawn with replacement to balance classes.
  - Software: bespoke RF pipeline integrating Weka, PostGIS, and GDAL (all open source).
- Validation and accuracy
  - UK-scale validation using GB countryside survey 2019 data, open data from National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points).
  - Reported overall accuracy: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4%.
  - Validation notes: same validation dataset used for all three products; accuracy pertains to mapping to UKCEH classes; some conversion/label uncertainties acknowledged.

## Imagery, data sources, and temporal context
- Seasonal imagery
  - Sentinel-2 Seasonal Composite Images created per season (winter, spring, summer, autumn) using median TOA reflectance.
  - Bands used reflect spectral information across seasons to differentiate vegetation types.
  - Some seasonal gaps due to cloud; the algorithm tolerates partial data and previously required manual gap filling (future work includes exploring Sentinel-1 SAR and other sources).
  - TOA data chosen over SR for this release; future work may revisit data inputs as benefits are demonstrated.
- Context rasters
  - 20m context rasters to reduce spectral confusion, including terrain (height, aspect, slope) from NEXTMap; distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland presence (derived from open data).
- Classification Scenes and tiling
  - GB: 100x100 km tiles used to extract 36-band Seasonal Composite Images; combined with 20m context rasters to form 46-band GB Classification Scenes; 74 overlapping scenes classified independently; visual checks used to resolve overlaps.
  - NI: single 43-band Classification Scene per year for the region (36 spectral bands + 7 context layers); determined by the minimum bounding rectangle of NI land mass.

## UKCEH Land Parcel Spatial Framework
- Framework retained from LCM2007/LCM2015 with minor updates for performance.
- Total land parcels unchanged; gid identifiers do not match LCM2015 parcel IDs, though parcel-level comparisons can be made via gid.
- MMU ~0.5 hectares; parcels represent discrete real-world units (fields, parks, urban areas, etc.) and help reduce classification noise and support change detection.
- Framework supports user-defined parcel summarization of the 20m Classified Pixels; potential for refinement to finer resolutions as data sources evolve.

## Practical implications for environmental monitoring
- Standardized, time-series-ready outputs enable consistent evaluation of environmental health and policy performance over time.
- Multiple data products (pixel-level, parcel-level, and aggregated 1km summaries) support diverse analysis needs, from detailed habitat mapping to broad regional change assessments.
- Documented relationships and glossary clarify mapping to BAP Broad Habitats and UKCEH Land Cover Classes, aiding comparability and interpretation across datasets and time.

## Future plans and considerations
- Annual release intention to improve timeliness of land cover change detection.
- Exploration of additional satellite input (e.g., Sentinel-1 SAR) to fill seasonal gaps and improve classification robustness.
- Planned refinement of Bootstrap Training for future maps and potential updates to the Land Parcel Spatial Framework to accommodate higher-resolution data.

## Appendices and references
- Appendix materials explain how UKCEH Land Cover Classes relate to BAP Broad Habitats and provide class definitions, data interpretation notes, and recommended colour schemes for visualization.
- References cover foundational methods (Bootstrap Training, Random Forest) and related UK land cover mapping work.