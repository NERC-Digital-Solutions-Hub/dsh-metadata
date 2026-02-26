# The UKCEH Land Cover Map 2023

- Scope and purpose
  - UKCEH LCM2023 is the eleventh annual UK land cover map, produced to support monitoring of state and change in the UK countryside.
  - Product consists of seven datasets: three for Great Britain and Northern Ireland (GB/NI) each (10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster covering GB and NI.
  - The guide describes data production, validation, and data accuracy to help users make informed decisions about applying LCM2023 data.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
    - Generated from multiple Classification Scenes; use Bootstrap Training with a Random Forest classifier.
    - Output includes two bands: the dominant UKCEH Land Cover Class and the associated confidence/probability.
    - Maintains full 10 m detail (not generalized by the Land Parcel Spatial Framework) to preserve narrow features; validation focused on the 25 m rasterised parcels.
  - Land Parcel datasets
    - Result from intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to produce parcel attributes.
  - 25 m Rasterised Land Parcel datasets
    - Rasterised from the Land Parcel data; three attributes per parcel: dominant land cover (mode), confidence (conf), and purity.
  - 1 km raster products
    - Derived by aggregating 25 m rasters to 1 km; provide dominant class per 1 km pixel and percentage cover for both classes (21) and aggregates (10). Rounding may cause sums to deviate from 100%, especially near coastlines.
  - Coordinate systems and extents
    - GB: British National Grid (EPSG 27700); NI: Irish Grid (EPSG 29903); parcels: GB and NI extents and counts detailed in the dataset descriptions.

- Production methodology
  - Seasonal Composite Images
    - Derived from Google Earth Engine using Sentinel-2 data; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10 m resolution; 12 Sentinel-2 bands used; gaps due to cloud are tolerated by the classifier.
  - Context Rasters
    - 10 m context rasters to reduce spectral confusion (e.g., height, aspect, slope; distances to buildings, roads, water; foreshore, woodland, saltmarsh masks; separate sets for GB and NI).
  - Classification Scenes and Bootstrap Training
    - GB classified in 32 tiles; NI in a single scene; Bootstrap Training samples from historic maps (LCM2020–2022) filtered to >80% probability and consistent across three years.
    - Random Forest classifier trained with 10,000 samples per class per bag; balanced learning to avoid dominance by common classes.
  - UKCEH Land Parcel Spatial Framework
    - Defines land parcels (~0.5 ha MMU) to reduce classification noise and enable change detection; gid identifiers may not match across LCM2015 due to dataset reorganization.
  - Validation
    - 33,107 validation points across 21 classes; overall accuracy reported at 83%.
  - Software and provenance
    - Classification software combines Weka, PostGIS, and GDAL; methods and processes are continuously evolving; annual production aims for temporal consistency to distinguish real change from method-induced differences.

- Dataset metadata, access, and citation
  - Each LCM2023 dataset has a DOI and recommended citation (Table 5 in the guide); related publications include Marston et al. (2023, 2024) documenting methods and data products.
  - Known issue: a small number of vector land parcels are missing, causing nodata areas in the 25 m rasterised parcels; these gaps have negligible impact on 1 km products and do not affect 10 m pixels.
  - Disclaimer: methodological changes across annual maps may cause differences beyond real land-cover change.

- UKCEH Land Cover Classes and BAP relationships
  - The 21 UKCEH Land Cover Classes are aligned with Biodiversity Action Plan (BAP) Broad Habitats but are not identical; BAP terms are italicized to differentiate and avoid ambiguity.
  - Appendices explain how UKCEH classes map to BAP Broad Habitats (e.g., Broadleaved woodland, Coniferous woodland, Arable, Grasslands, Wetlands, Coastal, Built-up, etc.), including notes on spectral overlap and classification challenges.
  - Some regional nuances exist (e.g., saltwater vs freshwater distinctions, bracken confusions, and peat-related classes).

- Appendices and supporting resources
  - Appendix 3: Full list of LCM2023 datasets and DOIs.
  - Appendix 4: Correspondence matrices showing observed vs predicted classifications and accuracy metrics by class.
  - Appendix 5 & 6: Recommended color recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options and accompanying QGIS symbology files. 
  - Appendices provide detailed class definitions, training considerations, and guidance for users on interpretation and potential confusion between classes.

- Practical considerations for data stewards and users
  - Data governance and provenance
    - Clear lineage from seasonal composites, context rasters, Bootstrap Training, and RF classification; alignment with the UKCEH Land Parcel Spatial Framework for project-level analysis.
  - Temporal consistency and change monitoring
    - Annual updates reduce random errors and help distinguish real land-cover changes; classification errors tend to flicker over time.
  - Data quality and limitations
    - 83% overall accuracy; known issues with vector parcel completeness; 10 m pixel dataset retains fine detail but lacks parcel-level generalization; 1 km products provide summary statistics with coastal rounding considerations.
  - Use-case considerations
    - Suitable for large-scale change detection, habitat monitoring, and integration with BAP Broad Habitat planning; caveats include potential spectral confusion among grassland types, bracken, peat-related classes, and coastal zones.

- How to cite and further information
  - Each dataset has a DOI; users should cite the appropriate LCM2023 dataset (e.g., 10 m Classified Pixels GB/NI, 25 m Rasterised Land Parcels GB/NI, Land Parcels GB/NI, 1 km Summary Rasters).
  - For overview of production methods, see Marston et al. (2023/2024) as referenced in the guide.