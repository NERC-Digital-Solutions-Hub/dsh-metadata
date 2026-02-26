# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

- Overview and purpose
  - Provides three new UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019) representing 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
  - Maps produced automatically using Bootstrap Training and Random Forest classification; annual updates are planned going forward.
  - Aimed to enable rapid, consistent, UK-wide land cover mapping with validated performance and clear documentation to inform current and future work.

- Data structure and classes
  - 21 UKCEH Land Cover Classes (aligned with LCM2015; near match to older LCMs). Includes distinct classes such as Broadleaved woodland, Coniferous woodland, Arable, Improved Grassland, Neutral/Calcareous/AcidGrasslands, various upland and coastal habitats, Freshwater, Saltmarsh, Urban/Suburban, etc.
  - Datasets provided per year and per region (Great Britain and Northern Ireland), with UKCEH describing both aggregate and detailed classes.
  - Core dataset suite and products (duplicated for each year) totaling 42 datasets across the three years:
    - 20m Classified Pixels (new in 2017–2019)
    - Land Parcels
    - 25m Rasterised Land Parcels
    - 1km Dominant Cover
    - 1km Dominant Aggregate Cover
    - 1km Percent Cover
    - 1km Percent Aggregate Cover

- Data and production specifics
  - Satellite imagery and inputs
    - Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) at 20m resolution for classification.
    - Seasonal composites merged with 20m Context Rasters to form Classification Scenes.
    - Context rasters include topography (Height, Aspect, Slope) and spatial-context features (distance to buildings, roads, seas, rivers, etc.).
  - Classification approach
    - Bootstrap Training: automatic sampling of historical land cover observations (from LCM2015; bootstrap from 99% pure parcels) to create large training sets for the Random Forest classifier.
    - Random Forest classification used to generate the 20m Classified Pixels; subsequent products are derived from these pixels using the UKCEH Land Parcel Spatial Framework.
    - No manual corrections are performed in 2017–2019 due to the automated production approach; visual checks and formal validation were conducted.
  - Spatial framework and outputs
    - UKCEH Land Parcel Spatial Framework used to summarise 20m pixels into parcel-level attributes; MMU approx. 0.5 ha.
    - Outputs include 20m Classified Pixels (with class and per-pixel confidence), Land Parcels (with a set of attributes), 25m Rasterised Land Parcels (3 bands: mode, conf, purity), and 1km products aggregating parcel-level data into 1km grids.
    - 1km products come in multiple bands: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band). Percent products are integer-valued and may not sum exactly to 100 due to rounding.
  - Geographic coverage and coordinate systems
    - Great Britain: GB National Grid (EPSG: 27700)
    - Northern Ireland: Irish Grid (TM75, EPSG: 29903)
  - Classification scheme and visualization
    - Appendix 3/Appendix 4 provide recommended color schemes, including color-blind friendly options.
  - Validation and quality
    - UK-scale validation against Countryside Survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (n ≈ 22,325).
    - Reported accuracy: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4% overall (UK-wide 21-class accuracy). Validation data are not perfect truth; results are best available indicators given differing underlying data sources and class definitions.
  - Production governance and reproducibility
    - Distinctive approach with automatic classification and no manual corrections to maintain annual timeliness; visual checks and formal validation remain in place.
    - GID (land parcel) identifiers from LCM2017–LCM2019 do not match LCM2015, due to changes in the UKCEH Land Parcel Spatial Framework, though parcel-level comparisons can be based on gid across 2017–2019.
    - Bootstrap Training lineage is from LCM2015; future maps (LCM2020 and beyond) plan to use majority signals across consecutive years.

- Notable methodological choices and limitations
  - Automatic classification versus manual correction
    - To enable annual updates, production relies on automated processes; manual corrections from earlier maps are not applied in these years.
  - Gaps and data completeness
    - Some 4-season data gaps due to cloud cover are allowed; the classification method tolerates partial data, with ongoing exploration of alternative data sources (e.g., Sentinel-1 SAR) to fill gaps.
  - Coastal and complex areas
    - Coastal and mixed habitats can present spectral confusion; context rasters and parity with BAP Broad Habitats are used to improve separation, but some cross-class confusion remains (e.g., Saltmarsh vs Freshwater vs Saltwater boundaries; bog vs acid/calcareous grasslands in peat-rich regions).
  - Land Parcel Spatial Framework
    - The framework emphasizes 0.5 ha MMU and parcel-based summarization; it is not the only possible summarization approach and future refinements may address high-resolution feature detection.

- Data governance, metadata, and access
  - Documentation and glossary
    - Comprehensive glossary and appendices (e.g., BAP Broad Habitats mapping, class definitions, and RGB color recipes) accompany the data to support correct interpretation and usage.
  - Data availability and lineage
    - Outputs are designed for robust discovery and reuse, with explicit metadata (coordinate systems, extents, class mappings, and dataset descriptions) to facilitate discovery, provenance tracking, and cross-year comparisons where feasible.
  - Appendix highlights
    - Appendix 1/2 provide background on UK BAP Broad Habitats and their relationship to UKCEH Land Cover Classes, including notes on detection limits and class derivations.
    - Appendix 3/4 provide color schemes for visualization, including color-blind friendly options.
    - Appendix 5 contains confusion matrices for validation (LCMs 2017–2019), detailing per-class accuracies and user/producer accuracies.
    - Appendix 6 lists full dataset inventories per year and region.

- Practical considerations for Data Stewards
  - Use and interoperability
    - The 20m Classified Pixels dataset preserves finer landscape details and can be summarized using user-defined parcel structures, enabling custom analyses beyond the UKCEH Land Parcel Spatial Framework.
    - 1km and 25m products allow rapid regional/ national-scale analysis with aggregated class information.
  - Change detection and longitudinal analysis
    - Bootstrap Training and annual production enable rapid updates while maintaining a coherent class framework; users should be aware of partial year-to-year differences in parcel identifiers and the generalization levels across products.
  - Validation and quality tracking
    - Validation results indicate good-but-improvable accuracy; continuous validation and potential refinement of training data and class mappings are anticipated as methodologies evolve.

- Future plans and ongoing developments
  - Annual release cycle with potential expansion of input data types (e.g., more extensive use of surface reflectance and SAR data).
  - Potential refinements to the UKCEH Land Parcel Spatial Framework and improved cross-year comparability, including more stable parcel identifiers or alternative matching strategies.