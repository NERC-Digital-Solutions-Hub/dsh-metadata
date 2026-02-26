# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite image data covering the entire United Kingdom, updating the Land Cover Map of Great Britain (LCMGB) 1990 and producing an all-UK dataset that includes Northern Ireland. It uses Landsat-derived classifications with additional ancillary data and is organized to align with the Joint Nature Conservation Committee (JNCC) Broad Habitats hierarchy.
- Available in both vector and raster formats, with multiple detail levels and resolutions to suit different user needs. Raster data are not directly comparable with LCM1990 due to different construction methods and are not suitable for estimating change over the 10-year period.

- Purpose for monitoring: Provides a detailed, information-rich land cover map suitable for environmental health monitoring, policy scrutiny, and informing future decisions, with explicit attention to data provenance, metadata, and governance.

- Key cautions for users: 
  - Minimum mappable unit is >0.5 ha; parcels smaller than this are dissolved or may remain in limited areas.
  - Some Level 3 (Variant) detail varies in accuracy across regions.
  - Raster and vector outputs differ in compatibility; the raster aggregation may affect change analysis.
  - Edge overlap artefacts can occur when stitching 100 km tiles; users may need to tidy boundaries carefully to preserve parcel-level attributes.

- Data governance and customization:
  - Each parcel carries a unique Segid label; users are advised to retain it to support lineage and traceability.
  - The production philosophy emphasizes preserving information and metadata; changes to data should retain original attributes or document them in new fields.
  - Thorough documentation of changes is encouraged to support data management and security.