# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Overview
  - Release of three new UKCEH land cover maps: LCM2017, LCM2018 and LCM2019.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; near-continuity with LCM2015/LCM2007 mappings.
  - Fully automatic classification using Bootstrap Training plus Random Forest; annual map production planned.
  - Sentinel-2 Seasonal Composite Images (median reflectance per season) used for classification; context rasters reduce spectral confusion.
  - No manual corrections in this release; visual checks and formal validation performed; quality deemed similar to LCM2015.

- Data content and structure
  - Product suite includes 42 datasets (GB and Northern Ireland for each year) with multiple scales:
    - 20m Classified Pixels (new addition; per-pixel class probability and dominant class)
    - Land Parcels (20m pixels mapped to land parcel framework; includes hist, mode, purity, conf, stdev, n)
    - 25m Rasterised Land Parcels (3-band: mode, conf, purity)
    - 1km Raster products: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band)
  - Spatial extents:
    - Great Britain: GB National Grid (EPSG:27700)
    - Northern Ireland: Irish Grid (EPSG:29903)
  - Pixel/band details:
    - 20m Classified Pixels: 2-band raster (class, probability 0–100)
    - 25m Land Parcels: 3 bands (mode, conf, purity)
    - 1km products: multi-band rasters as described
  - Parcel framework
    - UKCEH Land Parcel Spatial Framework; minimum parcel size ~0.5 ha; parcels generally dominated by a single class; gid identifiers differ from LCM2015 (affects year-to-year parcel comparisons)

- Production workflow and methodology
  - Seasonal data
    - Google Earth Engine used to generate four-season Sentinel-2 TOA bands (bands 2,3,4,5,6,7,8,11,12)
    - Context rasters (GB: 10, NI: 7) include terrain, proximity to buildings/roads/sea/freshwater, foreshore, tidal water, urban/woodland masks
  - Classification Scenes
    - GB: 100x100 km tiles; 74 overlapping scenes classified independently; scenes overlapped to balance training data
    - NI: single 43-band classification scene per year
  - Bootstrap Training
    - From LCM2015 with >99% purity parcels; bootstrap majority signal used to train RF classifier
    - Aim: enable rapid, annual updates with minimal manual data collection
  - Random Forest classification
    - Training: 10,000 samples per class per scene; balanced learning to avoid dominance by common classes
    - Software: bespoke pipeline integrating WEKA, PostGIS, and GDAL (open-source)
  - Validation and quality
    - Validation against GB countryside survey 2019 data, open National Forest Inventory data, IACS points; 22,325 validation points total
    - UK-scale overall accuracy: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%
    - Validation notes: same validation data used across three products; conversions between classifications introduce some subjectivity

- Class mappings and interpretation
  - 21 UKCEH Land Cover Classes derived from BAP Broad Habitats; intentionally aligned to maintain comparability with earlier maps
  - Appendix guidance clarifies relationships between UKCEH Classes and BAP Broad Habitats; some BAP classes are split or collapsed to improve remote sensing detectability
  - Colour and legend conventions provided for display of UKCEH Land Cover Classes

- Key technical and usage notes
  - 20m Classified Pixels preserve fine details (e.g., narrow features) not captured in parcel-aggregated products
  - 1km products provide aggregated summaries (percent/dominant) across 1km squares
  - Seasonal composition and context rasters support improved discrimination of spectrally similar classes
  - Gid identifiers for LCM2017–2019 parcels do not match LCM2015; comparisons should use gid or re-derive from spatial overlap
  - Future directions indicate potential inclusion of additional data sources (e.g., Sentinel-1 SAR) to fill seasonal gaps; broader use of alternative parcel frameworks

- Practical implications for environmental monitoring
  - Provides a consistent, year-by-year, UK-wide land cover time series suitable for change detection and policy performance assessment
  - Data products allow both detailed (20m Classified Pixels) and aggregated (1km) analyses
  - Outputs can be integrated with other environmental datasets via the standardized UKCEH Land Cover Classes and parcel framework
  - Validation performance supports use in monitoring, with acknowledgment of inherent limitations due to automatic classification and cross-dataset conversions

- Access and references
  - Full dataset descriptions, validation appendix, and dataset lists are provided (Appendix 4 and Appendix 5)
  - References to foundational methods and data sources (Random Forests, Bootstrap Training, Sentinel-2, and previous LCMs) are included for methodological context