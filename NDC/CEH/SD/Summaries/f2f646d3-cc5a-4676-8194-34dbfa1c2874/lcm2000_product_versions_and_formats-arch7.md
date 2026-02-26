# LCM2000 specification

- Overview
  - LCM2000 is an all-UK parcel-based thematic land cover map derived from satellite imagery (primarily Landsat), updating LCMGB 1990 and covering Northern Ireland as well.
  - Classified within a hierarchical Broad Habitat framework (JNCC) and includes additional detail where possible; available in both vector and raster formats with multiple detail levels and resolutions.
  - Minimum mappable unit is >0.5 ha; parcels ≤0.5 ha are dissolved into surrounding features during production; in some areas very small parcels may remain due to processing.
  - Dataset is organized in 100 km tiles; parcels are classified per tile and later merged; edge overlaps can create artefacts that users may need to tidy.

- Product versions and formats
  - Vector data (parcels with attributes)
    - Level 2: 26 LCM2000 Subclasses (standard, widely used)
    - Level 3: up to 72 Variants (detailed; variable accuracy across the country; requires special arrangement and support)
    - Standard vector format is ESRI shapefile (Spatial Analyst extension may be needed in ArcGIS for advanced analysis)
  - Raster data (derived from the vector)
    - 25 m resolution: 26 Subclasses
    - 1 km resolution: derived from 25 m with two detail options
      - Subclass level: 26 Subclasses
      - Dominant values and Percentage values at 1 km for each grid cell
    - Aggregate class level: 10 simplified Aggregates; with Dominant and Percentage options
    - Standard raster format is GeoTIFF (Spatial Analyst extension may be required in ArcGIS)
  - Important note: The LCM2000 raster is not directly comparable with LCM1990 due to different construction methods; not suitable for estimating change over the 10-year period.

- Dataset coverage and structure
  - Classified on a per-parcel basis and aggregated into 100 km tiles; edge overlaps are retained in adjoining tiles to preserve parcel identity where needed.
  - A 100 km tile diagram and tile-merging approach are used to simplify construction; some artefacts may occur at tile edges.

- Hierarchical nomenclature and codes
  - Vector data provides both Subclass detail and Variant detail (Level 3); a mapping table links concrete land cover types to Subclass and Variant codes.
  - Examples shown include Broad-leaved/mixed woodland (Variants: mixed, open birch, scrub), Coniferous woodland (variants: felled, new plantation), Arable crops (cereals, oats, wheat, etc.), Grassland types, Urban categories, and coastal/estuarine habitats.
  - Note: In some GIS packages, Subclass codes may display as the Level 2 numeric values.

- Vector polygon attributes (key metadata for each parcel)
  - SegID: Unique parcel identifier (includes OS 100 km square and segment number); recommended to retain for traceability.
  - BHSub: Dominant land cover type (Level 2 Subclass)
  - BHSubVar: Dominant land cover type (Level 3 Variant) – provided in Level 3
  - PerPixList: Top five spectral subclass percentages per pixel (Level 3 only)
  - OpHistory: Processing history descriptor detailing image date(s) and KBC rules applied (Level 2 and Level 3)
  - TotPixels: Total pixels in parcel
  - CorePixels: Pixels in the core area used for maximum likelihood classification

- OpHistory (processing history descriptor)
  - Five fields describe input data, scene, sensors, image acquisition dates, and KBC processing; a sixth field captures other information (e.g., flags for special cases like cloud patches, void filling, or training data usage).
  - Includes scene numbers, sensor types (e.g., TM, IRS), acquisition dates, and a compact encoding of processing steps.

- Colour recipes and broad habitat descriptions
  - Colour guidance (Table 5) provides recommended display colors for each of the 26 Subclasses to aid map production and visual differentiation.
  - Broad Habitat descriptions (Table 6) summarize 16+ broad habitat groups with concise definitions (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved/Neutral/Calcareous/Acid grasslands; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Standing water; Montane habitats; Inland bare ground; Built-up areas; Coastal habitats; etc.).

- Production philosophy and data governance
  - Production philosophy emphasizes retaining as much information as possible; users are encouraged to preserve parcel-level metadata to document lineage and processing history.
  - Unique Segid labels should be retained to enable unambiguous communication with data management and other users.
  - Full documentation of changes is essential for data management and traceability.
  - Users should be mindful of differences caused by data model, scale, resolution, and target definitions; inaccuracies are inevitable but should be interpreted in the context of methodology.

- Edge overlaps, artefacts, and data tidying (Appendix 1)
  - Edge overlaps arise from multiple overlapping source images; artifacts can occur where parcels cross tile edges.
  - The recommended approach is to dissolve boundaries between like classes visually or by processing, without removing parcel-level attribute data.
  - When merging tiles, the first input tile often has priority for edge parcels; different edge classifications can occur depending on tile order.
  - The guide provides step-by-step methods for clipping, merging, dissolving, and handling edge artefacts, with cautions about attribute validity after such operations.
  - For Level 3 data, preserve bhsubvar during dissolving to avoid loss of critical Level 3 information.

- Slivers and small parcels
  - Parcels smaller than the minimum mappable unit or slivers may appear; recommended handling includes visual removal, dissolving with adjacent same-class parcels, or intelligent dissolution based on boundary length to adjacent parcels.
  - The goal is to reduce visual clutter while preserving attribute integrity; users should assess artefacts in the context of the whole dataset.

- Customisation and practical usage
  - LCM2000 is designed as a data storage and analysis framework, not just a map; users can tailor and expand their version, retaining essential metadata and provenance.
  - The dataset supports various analyses and applications; keeping the Segid and processing history enables robust traceability and collaboration.

- Further information and references
  - Land Cover Map home page: www.ceh.ac.uk/data/lcm; contact: spatialdata@ceh.ac.uk
  - Key methodological references: Fuller et al. 2002; Smith et al. 2001; Jackson 2000 (JNCC Broad Habitat guidance)
  - Appendix notes and good practice guidance provide detailed instructions for edge-case handling and data quality assurance.

- Key takeaway for GIS specialists
  - LCM2000 provides a richly attributed parcel-based UK land cover dataset with flexible vector and raster formats, detailed provenance, and a strong emphasis on maintainable metadata.
  - Be prepared to manage edge artefacts, perform careful dissolving with attention to attribute integrity, and preserve Segid and OpHistory for reproducibility.
  - Use the vector’s 26 Subclasses (and Level 3 Variants where available) for detailed mapping, or aggregate to 10 broad classes for generalized analyses; raster equivalents offer 25 m and 1 km options with both subclass and aggregate representations.