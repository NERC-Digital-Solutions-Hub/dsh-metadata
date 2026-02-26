# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

- Purpose and scope
  - User guide accompanying the release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Aims to help users understand data structure, production choices, validation, and future plans to inform appropriate use in current and future work.

- Data products and structure
  - Map products describe 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) plus 10 UKCEH Aggregate Classes; designed to be close to LCM2015/class mappings for comparability.
  - UKCEH LCM product suite comprises 42 datasets (GB and NI versions across three years), including:
    - 20m Classified Pixels (new for these releases), the primary input from which other products are derived.
    - Land Parcels (20m Classified Pixels intersected with the UKCEH Land Parcel Spatial Framework).
    - 25m Rasterised Land Parcels (parcel-based raster summary).
    - 1km Dominant Cover; 1km Dominant Aggregate Cover; 1km Percent Cover; 1km Percent Aggregate Cover (summary rasters at 1km scale).
  - Geographic coverage and formats
    - Great Britain datasets use British National Grid (EPSG:27700); Northern Ireland datasets use Irish Grid (EPSG:29903).
    - Each year’s release provides GB and NI versions, resulting in 42 datasets in total.

- Production approach and data lineage
  - Bootstrap Training and Random Forest classification
    - Automatic training process that uses historic UKCEH LCMs (starting from LCM2015) to sample spectral training data for classification.
    - Bootstrap Training datasets drawn from land parcels with high purity (≥99% from LCM2015) to train the RF classifier (10,000 samples per class, with sampling with replacement to balance classes).
    - The bootstrap for LCM2017-2019 is derived from LCM2015 data; future maps (LCM2020, LCM2021) will use majority signals across multiple years.
  - Seasonal imagery and context
    - Classification Scenes built from 4-season Sentinel-2 seasonal composites (TOA reflectance, median per season) at 20m resolution.
    - Each classification scene combines seasonal spectra with 20m context rasters (terrain, proximity to features) to improve discrimination.
    - Google Earth Engine used to generate seasonal composites; SR (surface reflectance) data were considered but TOA data were used for these products.
  - Classification framework
    - A patchwork of GB 100x100 km tiles used to assemble 36-band Seasonal Composite Images, merged with 46-band GB Classification Scenes; NI uses a single 43-band scene per year.
    - 74 GB classification scenes produced; overlapping regions classified multiple times with selection by visual/quality checks to maximize accuracy.
  - UK Land Parcel Spatial Framework
    - Framework originally developed for LCM2007; retained in LCM2017–LCM2019 with minor updates for processing efficiency.
    - Unique parcel identifiers (gid) do not match LCM2015, but comparisons can be made using spatial overlap via gid.

- Data types and dataset descriptions
  - 20m Classified Pixels
    - New 20m RF classification outputs; two-band, 8-bit rasters: band 1 = most likely land cover class; band 2 = per-pixel confidence (0–100).
    - 20m pixels preserved to retain fine landscape detail; not generalised by the Land Parcel Framework.
  - Land Parcels
    - Attributes describe parcel composition derived from 20m Classified Pixels and the Parcel Framework (e.g., hist, mode, purity, conf, n).
    - Provides a fixed framework for change detection; supports further summarisation.
  - 25m Rasterised Land Parcels
    - Rasterised representation (3 bands): dominant class (_mode), confidence (_conf), and purity (_purity) averaged at parcel level.
  - 1km rasters
    - 1km Percent Cover (21-band, 8-bit); 1km Percent Aggregate Cover (10-band, 8-bit); 1km Dominant Cover (single-band); 1km Dominant Aggregate Cover (1-band).
    - Rounding/aggregation can cause minor total deviations around 100% for the 21-band set.
  - Seasonal Composite Images and Context Rasters
    - Seasonal TOA reflectance per season derived from Sentinel-2; context rasters include height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore, tidal water, urban mask, etc., with variations between GB and NI.
  - Classification Scenes and tile structure
    - GB uses 100x100 km tiles for classification; NI uses a single, country-wide scene per year; total 74 GB scenes across years.
  - Summary and metadata
    - Appendix 6 lists full dataset inventories; Appendix 2–5 provide detailed descriptions, class mappings to BAP Broad Habitats, color recipes, and validation results.

- Validation and accuracy
  - Validation framework
    - UK-scale validation against multiple resources: GB countryside survey data (2019), open National Forest Inventory data, IACS data, and bespoke LCM validation points (n ≈ 22,325).
  - Reported accuracy
    - LCM2017: ~78.6% overall accuracy.
    - LCM2018: ~79.6% overall accuracy.
    - LCM2019: ~79.4% overall accuracy.
  - Interpretation
    - Validation data are not an absolute truth; conversions between class schemes may introduce subjectivity.
    - Around 80% correspondence across 21-class maps is considered strong for an automatic, annually produced product; improvements expected as methods mature.
  - Per-class performance
    - The document provides detailed confusion matrices and producer/user accuracies by land cover class (Appendix 5), illustrating where misclassifications occur (e.g., between Arable and Improved Grassland, or various upland and coastal classes).

- Classification considerations and limitations
  - Spectral and contextual differentiation
    - Some habitat types (e.g., Neutral Grassland, Bracken) present spectral confusion; the inclusion of context layers (slope, distance to rivers, etc.) helped improve detection in several cases.
  - Coastal and water classes
    - Saltwater vs Freshwater confusion near coasts and tidal rivers can occur; water bodies beyond 0.5 ha and >40 m wide are mapped with higher accuracy.
  - Upland and peatland mappings
    - Broad Habitat categories like Bog, Fen, Marsh, Swamp, Heather, and Heather Grassland show interclass confusion due to spectral similarity and landscape mosaics; ongoing development aims to improve upland habitat mapping subject to training data availability.
  - Data gaps and future improvements
    - Cloud gaps in seasonal data acknowledged; potential future use of alternative optical sources or SAR (Sentinel-1) to fill gaps.
    - The production intentionally avoids manual corrections to enable annual updates; expects iterative improvement through Bootstrap Training and expanded training data in future releases.

- Visuals, color coding, and documentation
  - Appendix 3 and Appendix 4 provide recommended color schemes for displaying Land Cover Classes, including color-blind friendly alternatives.
  - Appendix 5 contains per-class confusion matrices and accuracy metrics to support monitoring and interpretation.

- Practical considerations for monitoring and policy use
  - The product suite is designed to support rapid, annual monitoring of land cover change across the UK, with explicit documentation of data lineage, class definitions, and validation near the 80% accuracy mark.
  - The fixed UK Land Parcel Spatial Framework enables temporal comparisons at parcel-level, while the 20m Classified Pixels retain finer landscape detail for exploratory analyses and threshold-based monitoring.
  - Users should account for potential misclassifications among spectrally similar classes and the ongoing evolution of training data when interpreting time-series changes or making policy decisions.

- Future directions and plans
  - Annual LCM releases are planned going forward (aim to extend to yearly updates and to broaden data inputs with advancing remote sensing sources and training.
  - Ongoing work to refine upland and peatland vegetation classifications; potential integration of additional data sources (e.g., SAR) to improve performance under cloud cover and in challenging habitats.
  - Continued emphasis on transparent methodology, metadata, and validation to support monitoring frameworks and evidence-based decision-making.