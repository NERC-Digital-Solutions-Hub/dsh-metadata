# LCM2000 specification

- Purpose and scope
  - Parcel-based thematic map of land cover for the entire United Kingdom, updating and upgrading the Land Cover Map of Great Britain (LCMGB) 1990.
  - Derived from satellite image classifications (mainly Landsat) with additional ancillary data.
  - Classified against a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, covering broad habitat categories plus additional detail where possible.
  - Produced in vector and raster formats, with multiple product versions offering different levels of detail and spatial resolutions.

- Product versions and formats
  - Vector data
    - Level 2: Standard detail with 26 LCM2000 Subclasses (most widely used).
    - Level 3: Detailed to 72 Variants; higher detail may vary by area; provided by special arrangement with CEH.
    - Format: ESRI shapefile; may require Spatial Analyst extension in ArcGIS for advanced analysis.
  - Raster data
    - 25 m resolution: 26 Subclasses.
    - 1 km resolution: Derived from the 25 m raster; provides Subclass level data (plus Dominant and Percentage values) and a simplified Aggregate class level (10 aggregates) with Dominant and Percentage outputs.
    - Standard raster format: GeoTiff; ArcGIS Spatial Analyst may be required.
  - Important caveat: Raster data are not directly comparable with LCM1990 due to different construction methods and are not suitable for estimating change over the 10-year period.

- Dataset coverage and structure
  - Compiled on a 100 km tile basis; land parcels classified per tile and then assembled into a UK-wide mosaic.
  - Minimum mappable unit is >0.5 ha; parcels of 0.5 ha or smaller are dissolved into surrounding areas during production, though some very small parcels may remain due to processing limits.
  - Edge overlaps between tiles are addressed through erosion and merging operations to produce a single-layer parcel map; parcels crossing tile edges are retained in both adjoining tiles in some cases.
  - Edge artefacts may occur (classification or geometry differences near tile edges) but are typically very rare (<0.1% of parcels). Users may visually tidy edges by dissolving boundaries between same-class parcels, with caveats about losing parcel-level attributes.

- Classification terminology and nomenclature
  - Vector data provide Subclass detail and, for Level 3, Variant detail; codes and mappings are provided (including complex Variant coding).
  - The 26 Subclasses map to 16 Broad Habitats (as described in the Broad Habitats descriptions).
  - The dataset includes contextual and per-pixel information where available (e.g., PerPixList for Level 3).

- Vector parcel attributes
  - SegID: Unique parcel identifier (including OS 100 km square and segment number) to enable traceability and communication with the data management team.
  - BHSub: Dominant land cover type at Level 2 (Subclass).
  - BHSubVar: Dominant land cover type at Level 3 (Variant) when available.
  - PerPixList: Per-pixel list of the top spectral subclasses within the parcel (Level 3 only).
  - OpHistory: Processing history descriptor detailing input data, image dates, and knowledge-based corrections applied.
  - TotPixels: Total number of pixels within the parcel.
  - CorePixels: Pixels within the parcel core used for maximum likelihood classification.

- OpHistory attribute (processing history)
  - Encodes input scene numbers, sensors (e.g., Landsat TM, IRS), image dates, and KBC (knowledge-based correction) steps.
  - Includes a six-field descriptor (plus a sixth field for additional information) indicating scene, sensor, dates, cloud-hole patches, and other metadata.
  - Includes information on the use of single-date cloud-hole patches and flags for processing variations.

- Colour recipes for mapping
  - Provides recommended color display values for all 26 Subclasses to aid visualization (Hue, Saturation, Value; and RGB equivalents).
  - Each Subclass has a defined color to support consistent display across outputs and maps.

- Broad Habitat descriptions (high-level categories)
  - Broad-leaved, mixed and yew woodland
  - Coniferous woodland
  - Boundaries and linear features
  - Arable and horticulture
  - Improved grassland
  - Neutral grassland
  - Calcareous grassland
  - Acid grassland
  - Bracken
  - Dwarf shrub heath
  - Fen, marsh and swamp
  - Bog
  - Standing open water and canals
  - Rivers, streams
  - Montane habitats
  - Inland rock
  - Built-up areas and gardens
  - Supra-littoral rock
  - Supra-littoral sediment
  - Littoral rock
  - Littoral sediment
  - Inshore sublittoral sediment
  - Inshore sublittoral rock
  - Offshore shelf sediment
  - Offshore shelf rock
  - Continental shelf slope
  - Oceanic seas
  - Note: Distinctions at various levels (subclass/variant) depend on imagery and timing.

- Practical guidance for users (data management and use)
  - Production philosophy emphasizes retaining as much information as possible; document lineage and changes with parcel-level metadata.
  - Encourage retaining SegID for traceability; maintain metadata when altering data.
  - Fully document changes to support data management and security.
  - Be mindful of accuracy and differences due to data model, scale, resolution, and interpretation; LCM2000 is information-rich but not a perfect, error-free representation.

- Appendix highlights (edge, slivers, and data handling)
  - Edge overlap problems: Overlaps between multiple source images within 100 km tiles lead to artefacts; guidance provided for visual tidying and for data processing steps to minimize impact.
  - Edge management approaches: clipping, merging (with attention to attribute validity), union, and dissolving boundaries between like classes; cautions about losing certain source attributes when performing these operations.
  - Level 3 data preservation: When dissolving, maintain bhsubvar to preserve Level 3 information.
  - Slivers and very small parcels: Various options to address, including visual removal, dissolving with adjacent same-class parcels, or intelligent dissolution based on boundary length with surrounding parcels.
  - Priority in tile merging: First input tile often takes precedence for edge parcels; differences across tiles can occur but are typically minor.

- Access and further information
  - Land Cover Map home page and contact details for data, sales, and methodology references.
  - Key literature for methodology and Broad Habitat classifications is cited (Linked to Fuller et al. 2002; Smith et al. 2001; Jackson 2000).

- Important cautions
  - LCM2000 raster data are not directly comparable with LCM1990, and should not be used to estimate change over the 1990–2000 period.
  - The Level 3 detail and accuracy vary spatially and depend on image timing and data availability.