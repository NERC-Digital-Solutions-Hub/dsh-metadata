# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Release of three national land cover maps: LCM2017, LCM2018, and LCM2019.
  - Maps show 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, intended to support time-series analysis and policy monitoring.
  - Classification produced automatically (no manual corrections this cycle) to enable rapid annual updates; validation shows similar quality to LCM2015.

- Data content and structure
  - Datasets included for each year (GB and NI):
    - 20m Classified Pixels: per-pixel class label with a second band indicating classification confidence (0–100).
    - Land Parcels: parcel-level attributes aggregating 20m pixel classifications; includes histograms, mode, purity, confidence, and counts; gid identifiers; SSF framework.
    - 25m Rasterised Land Parcels: 3-band rasters (mode, confidence, purity).
    - 1km Raster products: 
      - 1km Percent Cover (21-band)
      - 1km Percent Aggregate Cover (10-band)
      - 1km Dominant Cover (1-band)
      - 1km Dominant Aggregate Cover (1-band)
  - Spatial reference and extents
    - Great Britain: GB National Grid (OSGB) EPSG 27700
    - Northern Ireland: Irish Grid (TM75) EPSG 29903
  - Spatial framework and MMU
    - Land Parcels ~0.5 ha minimum mappable unit (MMU); designed to capture discrete land units (fields, parks, urban areas, etc.).
    - 20m Classified Pixels preserve fine landscape details; 25m rasters aggregate to reduce noise.
  - Transmission and dataset relationships
    - 20m Classified Pixels feed Land Parcels; parcels provide a fixed structure for time-series comparison.
    - Cross-year parcel IDs (gid) do not match LCM2015; cross-year comparisons rely on spatial overlap rather than parcel ID.

- Production methods and inputs
  - Bootstrap Training and Random Forest classification
    - Bootstrap Training uses majority signals from UKCEH LCM2015 (and earlier) to automatically train RF classifiers for 2017–2019.
    - For each year, training samples are drawn to balance the 21 classes; 10,000 samples per class per Classification Scene.
  - Seasonal inputs and classification scenes
    - Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) used to build Classification Scenes.
    - 9 Sentinel-2 bands used; 4 seasons (winter, spring, summer, autumn); some seasons have cloud gaps.
    - Context Rasters (20m) provide spatial context (terrain, urban proximity, water, roads, etc.) to reduce spectral confusion.
    - Great Britain uses 100x100 km overlapping tiles to create 74 Classification Scenes; Northern Ireland uses a single 43-band scene per year.
  - UK Land Parcel Spatial Framework
    - Based on framework used since LCM2007/2015; minor updates for performance; parcels unchanged in geometry but gid can differ between years.
    - Framework supports collocation and change detection while allowing user-defined parcel schemes.

- Validation and accuracy
  - Validation against GB countryside survey 2019 data, National Forest Inventory data, IACS, and bespoke validation points (22,325 points total).
  - Overall accuracy (UK scale):
    - 2017: 78.6%
    - 2018: 79.6%
    - 2019: 79.4%
  - Notes
    - Validation uses data with different purposes and class mappings; results should be viewed as indicative rather than absolute truth.
    - Approximately 80% correspondence across the 21-class products; further improvements anticipated as methods mature.

- Class definitions and interpretation
  - 21 UKCEH Land Cover Classes anchored to UK BAP Broad Habitats; mappings explained with notes on nuances (e.g., distinctions between Heather vs Heather Grassland; Saltwater vs Freshwater in coastal contexts).
  - Appendices provide detailed habitat definitions, crosswalks, and recommended display colors for mapping outputs.

- Technical considerations and future directions
  - TOA vs Surface Reflectance: production used Sentinel-2 TOA; SR did not improve classification in this context; ongoing assessment for higher thematic detail.
  - Gap handling: seasonal gaps due to clouds acknowledged; exploration of using Sentinel-1 SAR and other sources to fill gaps and improve seasons completeness.
  - Annual updates: intention to continue annual releases (LCM2020 planned for 2021; bootstrap strategies evolving with each cycle).
  - Data access and reuse for monitoring
    - Multi-resolution outputs support both fine-grained analysis (20m Classified Pixels) and broad policy metrics (1km and aggregated products).
    - The 20m dataset preserves detailed landscape features; parcel-based summaries facilitate change detection and reporting at parcel or boundary scales.
    - Product suite and underlying data are compatible with standard geospatial tools (Weka, PostGIS, GDAL) and open-source workflows.

- Practical considerations for analysts monitoring the environment
  - Use standardized 21-class outputs for consistent temporal comparisons; leverage the 20m Classified Pixels for detailed mapping and the 1km products for regional assessments.
  - When comparing years, rely on spatial overlap of land parcels rather than parcel IDs due to gid changes.
  - Be mindful of known classification uncertainties in certain upland/peatland and transitional habitats; context rasters mitigate some confusions but some misclassifications may persist.
  - Data provenance and reproducibility: Bootstrap Training and RF approach provide reproducible pipelines; documentation and Appendix resources aid interpretation and cross-walks with BAP Broad Habitats.