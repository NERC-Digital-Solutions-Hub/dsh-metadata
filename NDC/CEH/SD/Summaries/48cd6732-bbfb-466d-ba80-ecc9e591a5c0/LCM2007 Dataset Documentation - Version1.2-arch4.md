# LAND COVER MAP 2007 DATASET DOCUMENTATION

- overview
  - UK-wide parcel-based land cover classification using 23 classes aligned with UK Broad Habitats.
  - Based on 20–30 m satellite imagery; advances LCM2000 through OSMM-based vectorization for better object representation.
  - Maps land cover (not land use); minimum mappable unit is 0.5 ha; parcels smaller than this are dissolved into surrounding areas.
  - Complex methodology with rich metadata and knowledge-based enhancements; final report Morton et al., 2011 provides detailed methodology and limitations.

- data concepts and structure
  - vector data set
    - approx. 10 million polygons across GB and NI with 10 attributes per polygon.
    - key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
    - unique Parcel_ID enables unambiguous communication; BHSub provides additional context but may have lower validation certainty.
  - raster data sets
    - 25 m raster: 23 LCM2007 classes; derived from the vector; used for detailed mapping.
    - 1 km raster: aggregate products (dominant class, percentage cover) using 23 classes and aggregate classes; suitable for larger-area analyses.
    - GB and NI provided as separate tiles due to different projections; GB uses British National Grid, NI uses Irish National Grid (with NI migrating toward ITM).

- data access and licensing
  - 1 km raster products accessible via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; fees may apply.
  - Documentation notes that data access may require licensing arrangements and that system integration may require reprojection to local coordinate systems.

- data quality, validation, and limitations
  - validation against ground reference polygons (~9,127) yielded average accuracy around 83%, with acknowledged local variability.
  - change detection is not well-suited for LCM2007 due to differing class definitions, spatial structure, and typical spectral classification error (~20%).
  - LCM2007 provides both direct class labels (LCM2007 class) and Broad Habitat sub-classes (BHSub); using sub-classes requires user validation, as QA primarily covers main LCM2007 classes.

- data management, metadata and usage guidance
  - rich metadata per polygon (processing history, KBE history, ProbList, etc.) supports traceability and reproducibility.
  - recommended practice: retain Parcel_ID and validate Broad Habitat sub-classes if used for detailed analyses.
  - caution that LCM2007 maps land cover, not strictly land use; spectral similarity may blur distinctions between certain land-use-like features (e.g., arable crops vs. non-cropped areas).

- product specifics and examples
  - vector vs. raster trade-offs:
    - vector: high detail and metadata but large file sizes; suitable for precise queries and communications.
    - 25 m raster: easier processing with complete thematic detail, but without polygon-level metadata.
    - 1 km raster: efficient for national-scale modeling and integration with other large-scale datasets; provides dominant and percentage coverage for both full and aggregated classes.
  - example outputs illustrate differences in spatial resolution and associated metadata.

- usage considerations for data leaders
  - assess whether high thematic resolution (23 classes) or broad-scale aggregation (1 km) better fits organizational needs.
  - plan data governance around retaining unique Parcel_IDs for clarity in cross-team communication and version control.
  - factor in data size, licensing, and projection compatibility when integrating with internal systems.
  - leverage the change-detection caveats when designing longitudinal analyses; consider using the Final Report and Appendices for class-relationship mappings and colour coding if visualization is required.

- updates, version history, and acknowledgements
  - Version 1.2 (May 2014): updates to include OS tiles Fair Isle and Stranraer; NI water class addition; water class added to 1 km aggregates.
  - Acknowledges multiple data sources (Landsat, SPOT, AWIFS, OS, etc.) and collaboration within the Countryside Survey framework.
  - Appendices cover LCM2007 class definitions, relationships to Broad Habitats, colour mappings, and specific update details.