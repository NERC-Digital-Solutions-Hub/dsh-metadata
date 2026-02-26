# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for the UKCEH Land Cover Map 2020 (LCM2020), the eighth UK land cover map, produced annually.
  - LCM2020 comprises six datasets (three for GB and Northern Ireland): for each region, a 10 m classified-pixel dataset, a land parcel dataset, and a 25 m pixel rasterised land parcel dataset.
  - The aim is to enable informed decision-making about land cover use, change detection, and data quality, with attention to production methods, validation, and accuracy.

- Product structure and datasets
  - GB and Northern Ireland datasets:
    - 10 m Classified Pixels: pixel-level land cover classification with a second band giving the classification confidence.
    - Land Parcel Dataset: land parcel attributes created by intersecting the 10 m pixels with the UKCEH Land Parcel Spatial Framework.
    - 25 m Rasterised Land Parcel: per-parcel raster products (mode, confidence, purity) derived from the land parcel framework.
  - Extents and CRS
    - GB: British National Grid (EPSG: 27700).
    - Northern Ireland: Irish Grid (EPSG: 29903).
  - Sample sizes and structure
    - GB and NI together include over 7 million parcels across datasets; 10 m pixels are not generalized to preserve fine features below the 0.5 ha minimum mappable unit (MMU).
  - Data quality and metadata
    - Appendix 4 provides formal validation; overall thematic accuracy is just over 79%.

- How LCM2020 was produced
  - Seasonal data and context
    - Seasonal Composite Images (Sentinel-2) across four seasons (winter to autumn) using 9 bands; data gaps due to cloud are tolerated.
    - 10 m Context Rasters address spectral confusion (terrain, proximity to features, distance to water/roads/buildings, coastal masks, etc.).
  - Classification framework
    - Classification Scenes: GB uses 100 x 100 km tiles producing 46-band scenes (36-band Sentinel-2 + 10 context rasters); NI uses a single 43-band scene per year.
    - Bootstrap Training: automatically sampled from historic LCMs (LCM2017–2019) to train the classifier; only parcels with >99% purity across three years retained, yielding large training sets (GB ≈ 941,027; NI ≈ 214,833).
    - Random Forest: supervised learning with balanced sampling across classes; two-band 10 m pixel outputs (class, confidence). The RF model integrates bespoke UKCEH software with WEKA, PostGIS, and GDAL.
  - Land parcels and spatial framework
    - UKCEH Land Parcel Spatial Framework defines ~0.5 ha MMU parcels to reduce noise and support change detection; parcels unify diverse land-cover patches into discrete units for analysis.

- Class system and interpretation
  - UKCEH Land Cover Classes
    - 21 classes, aligned with Biodiversity Action Plan (BAP) Broad Habitats definitions, but not identical to BAP (spectral classification constraints discussed).
    - Appendices explain nuanced relationships and note where spectral confusion can occur (e.g., between arable and improved grassland; bog vs. acid grassland; upland vegetation complexities).
  - Relationship to BAP Broad Habitats
    - Table 1 outlines relationships between UKCEH Land Cover Classes, UK BAP Broad Habitats, and aggregate class mappings; some BAP categories collapse or split into multiple UKCEH classes for remote sensing purposes.
  - Colour recipe and display guidance
    - Appendix 3 provides RGB color mappings for display of each class to support visualization.

- Validation and accuracy
  - Validation approach
    - Validation against GB countryside survey data (2019–2020), National Forest Inventory, IACS data, and bespoke LCM validation points (34713 locations intersected with Land Parcel datasets).
  - Accuracy
    - Overall accuracy: 79.2%.
    - Appendix 4 includes detailed producer’s and user’s accuracies across all classes, highlighting common misclassifications and class-specific performance (e.g., higher accuracy for many dominant classes; lower for some heterogeneous or spectrally similar classes).

- Practical use and considerations for data leaders
  - Time-series and change detection
    - Annual production enables differentiation of random classification noise from real change; persistent changes across years indicate true land-cover transitions.
  - Data usage guidance
    - Prefer Land Parcel datasets for standardized area-based analyses and change detection; use 10 m Classified Pixels for detailed landscape features (with awareness of the lack of generalisation to the Land Parcel framework).
  - Limitations and challenges
    - Some classes exhibit spectral confusion; accuracy varies by class and region.
    - Differences in land parcel identifiers between LCM2015 and LCM2020 may affect direct parcel-based comparisons if using old IDs; spatial overlap remains usable for most comparisons.
  - Data governance and standards
    - Clear mapping to UKCEH Land Cover Classes and BAP Broad Habitats; detailed metadata and Appendix material support consistent interpretation and cross-walks to biodiversity/habitat frameworks.

- Access and provenance
  - Full LCM2020 dataset list
    - GB and NI: 10 m Classified Pixels, Land Parcel Product, 25 m Rasterised Land Parcel Product.
  - Official dataset naming and citations provided in Appendix 5.
  - Data readiness for discovery and reuse
    - Datasets include extensive metadata, spatial extents, coordinate reference systems, and per-class accuracy information to support data governance and decision-making.

- Future directions
  - The methodology emphasizes automation and annual updates; ongoing improvements may lead to re-application across the full catalogue to maximize temporal consistency, comparability, and change-detection capabilities.

- Quick strategic takeaways for Data Leaders
  - LCM2020 provides annual, high-resolution land-cover maps with parcel-level framing for robust change detection and trend analysis.
  - The combination of Bootstrap Training and Random Forest supports wall-to-wall mapping with scalable, automated production, reducing the need for manual corrections.
  - The 21-class schema, aligned with BAP broad habitats, allows integration with biodiversity and habitat assessments, while acknowledging spectral limitations.
  - The Land Parcel Spatial Framework enhances analysis reliability and comparability over time; however, parcel IDs may not be directly compatible with older datasets.
  - Use 10 m classified pixels for detailed landscape work, and land parcels for standardized area-based analyses; rely on the 79.2% overall accuracy as a baseline for planning and risk assessment, with class-level accuracies consulted from Appendix 4.