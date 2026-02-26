# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, updating the Land Cover Map of Great Britain (LCMGB) 1990 and extending to include Northern Ireland for an all-UK dataset.
  - Derived mainly from Landsat imagery, with additional ancillary data; produced in vector and raster formats; consists of a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats.
  - Available in multiple product versions with varying levels of detail and resolutions.

- Data formats and coverage
  - Vector data
    - Polygons representing land parcels with attached attributes.
    - Level 2: 26 Subclasses (standard, most widely used).
    - Level 3: 72 Variants (more detailed), with variable accuracy; Level 3 available by special arrangement.
    - Standard vector format is ESRI shapefile; ArcGIS users may need Spatial Analyst.
  - Raster data
    - Derived from the vector database and provided at two resolutions (25m and 1km).
    - 25m grid: 26 Subclasses.
    - 1km grid: Subclass level (26), and Aggregate level (10) with Dominant and Percentage values per pixel.
    - Not directly comparable to LCM1990 due to different construction methods; not suitable for estimating change over the 10-year period.
  - Dataset coverage
    - Compiled on a 100km tile basis; parcels are classified per tile and assembled into the UK-wide mosaic.

- Nomenclature and classification detail
  - Vector data supports Subclass and Variant detail; a hierarchical code (and alpha codes) defines land cover types.
  - Class Variants (Level 3) provide additional detail, though accuracy and consistency may vary geographically.
  - A note: the ability to distinguish at Variant level depends on the dominant land cover at imaging time and available contextual information.

- Vector polygon attributes and processing history
  - SegID: Unique parcel identifier; stored for all users and recommended to be retained.
  - BHSub: Dominant land cover type at Subclass level (Level 2).
  - BHSubVar: Dominant land cover type at Variant level (Level 3), when present.
  - PerPixList: Percentage area by the top five spectral Subclasses within the parcel (Level 3 only).
  - OpHistory: Processing history descriptor (PHD) for each parcel, detailing input data, classification stages, knowledge-based corrections (KBC), and dataset compilation.
  - TotPixels: Total pixels within the parcel.
  - CorePixels: Pixels within the core area used for maximum likelihood classification.
  - OpHistory fields summarize scene number, sensor, acquisition dates, cloud-hole patches, and KBC rule usage.

- Processing history and scene metadata
  - Scene/Sensor/Date information accompanies each parcel (e.g., TM, IRS sensors; various summer/winter dates).
  - Additional descriptors cover cloud holes, per-pixel classification, and KBC-related changes.
  - The data structure provides a detailed provenance trail for reproducibility and auditing.

- Colour mapping and broad habitat descriptions
  - Colour recipes assign distinct colours to each of the 26 Subclasses for display and interpretation.
  - Broad Habitat descriptions (16+ categories) provide higher-level habitat groupings (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Heaths, Wetlands, Inland water, Montane habitats, Inland bare ground, Built-up areas, Coastal habitats, etc.).

- Usage, limitations, and best practices
  - Not designed for direct change detection; LCM2000 and LCM1990 were produced with different methods, so separate change analysis requires careful methodological treatment.
  - The dataset is described as information-rich and suitable as a storage/analysis framework; users are encouraged to maintain parcel-level lineage and metadata when modifying data.
  - Production philosophy emphasizes preserving as much information as possible and documenting changes to support data management and provenance.

- Edge overlaps, artefacts, and data cleaning (Appendix 1)
  - Edge overlaps arise from mosaicked imagery and cloud-hole patching, resulting in multiple overlapping parcel layers within 100km tiles.
  - Artefacts are rare (often <0.1% of parcels) but may occur; recommended user approaches:
    - Visual tidying: dissolve boundaries between adjacent parcels of the same class using legend/ArcMap tools.
    - Data-level adjustments: clip to tile edges, union tiles (aware of attribute validity), then dissolve as needed; be mindful that clipping/merging can invalidate parcel-level attributes (especially for Level 3).
    - For Level 3 data, preserve bhsubvar during dissolves to avoid losing important information.
    - Use selective dissolves or data selection to streamline processing at tile edges without compromising overall dataset integrity.
  - Edge priority: when merging tiles, the first input tile often prevails at the edge; some differences may occur if classifications diverge.

- Slivers and small parcels
  - Small parcels or slivers (below minimum mappable unit) may persist due to edge overlaps or patching.
  - Users can address them via visual removal, dissolving with adjacent same-class parcels, or intelligent dissolution based on shared boundaries to maintain data integrity.

- Customisation, lineage, and good practice
  - LCM2000 is intended as a flexible data framework; users should document and preserve parcel-level metadata and maintain a clear lineage when expanding or altering the dataset.
  - Maintaining the SegID facilitates communication with the data management team and other users.
  - Practice recommends retaining original attributes while adding new attributes to capture changes, ensuring traceability.

- Accuracy and correspondence
  - Acknowledges inevitable inaccuracies due to data models, scale, resolution, and interpretation; users should distinguish between structural differences and true inaccuracies.
  - The methodology preserves information richness, but users should interpret results with awareness of underlying data characteristics.

- Further information and references
  - Land Cover Map homepage: www.ceh.ac.uk/data/lcm; contact: spatialdata@ceh.ac.uk; phone: 01491 692315.
  - Key references for methodology and broad habitat classifications (Fuller et al. 2002; Smith et al. 2001; Jackson 2000) for detailed methods and classifications.

- Practical takeaway for environmental analysts
  - Use LCM2000 as a comprehensive UK-wide baseline of land cover with rich parcel-level data, usable in reports, maps, and analyses.
  - Leverage both vector (parcel-based) and raster (2 resolutions) outputs, while respecting limitations for change estimation.
  - Retain SegID and maintain provenance through OpHistory; apply careful edge-management techniques when combining tiles.
  - When integrating with other datasets, consider the 100km tile structure and the hierarchical Broad Habitat framework to ensure consistent interpretation across time.