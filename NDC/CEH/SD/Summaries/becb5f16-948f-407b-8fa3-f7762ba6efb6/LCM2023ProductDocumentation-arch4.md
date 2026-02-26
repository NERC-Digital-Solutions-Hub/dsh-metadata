# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - User guide for the UKCEH Land Cover Map 2023 (LCM2023).
  - Product comprises seven datasets: three for Great Britain and Northern Ireland (GB and NI) plus a 1 km summary raster product.
  - Datasets: 10 m classified pixel dataset, land parcels (classified), 25 m rasterised land parcel dataset, and a 1 km summary raster; an additional 1 km product covers GB and NI.
  - Aims to help users understand data production, validation, and accuracy to inform current and future work.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class with a second band indicating classification probability/confidence.
  - 25 m Rasterised Land Parcel datasets (GB and NI): parcels created by rasterising land parcels at 25 m with bands for dominant class, confidence, and purity.
  - Land Parcel Vector datasets (GB and NI): linked to the UKCEH Land Parcel Spatial Framework; approximately 0.5 ha minimum parcel size.
  - 1 km summary rasters: dominant class and percentage cover for each 1 km pixel (GB and NI), with both class-level and aggregate-class summaries.
  - Classification framework uses 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan Broad Habitats (with careful notes on mapping differences).

- Production methodology
  - Classification Scenes: GB uses 32 tiles; NI uses a single 49-band classification scene (Sentinel-2 Seasonal Composite Images plus Context Rasters).
  - Seasonal Composite Images: Sentinel-2 data across four seasons (January–March, April–June, July–September, October–December); 10 spectral bands used.
  - Context Rasters: 10 GB context rasters (e.g., height, aspect, slope, distances to buildings/roads/water, foreshore, woodland, saltmarsh); NI uses a mix of terrain, urban mask, and proximity layers.
  - Bootstrap Training: automatic, uses historic LCM observations (LCM2020–LCM2022) with high-confidence pixels to train a Random Forest classifier; avoids need for new field data.
  - Random Forest: balanced sampling; produces per-pixel class with probability/confidence; proprietary UKCEH software integrating WEKA, PostGIS, and GDAL.
  - Land Parcel Spatial Framework: fixed 0.5 ha MMU to generalise 10 m pixels into parcels; aids change detection and data usability.
  - Temporal strategy: annual production to improve temporal consistency, enable change detection, and separate real change from classification error.

- Data quality, validation, and accuracy
  - Formal validation: 33,107 validation points across all 21 classes.
  - Overall accuracy: 83%.
  - Validation data sources: GB countryside survey, National Forest Inventory, Rural Payments Agency data, and bespoke validation points.
  - Known issues: a small number of polygons missing from vector land parcel products (affects only 25 m rasterised parcels; 10 m classified pixels are unaffected).

- Data management, metadata, and dissemination
  - DOIs and formal citations provided for each dataset; multiple publications cited for production methods (e.g., Marston et al. 2023/2024).
  - Data extent and coordinate systems:
    - GB: British National Grid (EPSG 27700) for GB datasets.
    - NI: Irish Grid (TM75, EPSG 29903) for NI datasets.
  - Documentation includes appendices detailing relationships between UKCEH LC Classes and UK BAP Broad Habitats, methodological notes, and guidance on data interpretation.
  - Display guidance: recommended colour schemes and QGIS symbology files are provided (with both standard and color-blind friendly versions in appendices).

- Practical implications for data strategy and use (Data Leaders focus)
  - Temporal consistency and change detection: annual maps reduce ambiguity between real change and methodological differences; enables robust monitoring of UK countryside state and trends.
  - System-wide data governance: clear data lineage (from Sentinel-2 seasonal composites and context rasters to classification and parcel frameworks) supports reproducibility and auditing.
  - Data accessibility and reuse: DOIs and citations facilitate proper data attribution; open-source tooling enhances portability and collaboration across organisations.
  - Metadata richness and standards: explicit validation metrics, uncertainty (probability/confidence per pixel), and detailed appendix on classes and BAP mappings improve data understanding for policy, planning, and environmental reporting.
  - Limitations and risk management: acknowledged gaps (e.g., missing parcels in vector products) and method-change caveats inform users when integrating LCM2023 with prior years or other datasets.
  - Cross-domain interoperability: land parcel framework and 1 km summaries support scale-up analyses, aggregation, and integration with other geospatial data systems.

- Known issues and caveats
  - A small subset of land parcel vectors missing, causing nodata regions in the 25 m rasterised parcels; effect is negligible for 1 km summaries; 10 m classified pixels remain unaffected.
  - Annual methodological changes can introduce differences between consecutive maps; users should consider both real change and methodological variation when comparing years.

- Citations, references, and data access
  - Each LCM2023 dataset has a DOI; cited works include Marston et al. (2023, 2024) and Morton et al. (2011, 2015) among others.
  - Data products include 10 m classified pixels (GB/NI), 25 m rasterised parcels (GB/NI), land parcels (GB/NI), and 1 km summary rasters.
  - Appendix materials provide detailed class definitions and relationships to BAP Broad Habitats, plus display palettes for mapping.

- Summary of key takeaways for decision-making
  - LCM2023 provides an annual, well-documented, openly referenced land cover dataset suite with transparent validation, enabling robust monitoring and reporting.
  - The combination of high-resolution classification (10 m), parcel-based summaries (25 m), and scalable 1 km outputs supports policy analysis, environmental reporting, and long-term data governance.
  - The Bootstrap Training and RF-based approach, coupled with rich context information, offers a reproducible framework with documented uncertainties and improvement trajectories.