# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map for the entire United Kingdom (including Northern Ireland), updating the Land Cover Map of Great Britain (LCMGB) 1990. It combines Landsat imagery with ancillary data and uses a hierarchical nomenclature aligned with JNCC Broad Habitats. Available in both vector and raster formats with multiple detail levels and resolutions.

- Minimum mapping unit and edge handling:
  - Minimum mappable area > 0.5 ha.
  - Parcels ≤ 0.5 ha dissolved into surrounding areas; some very small parcels may remain due to processing challenges.
  - Edge overlaps between 100 km tiles were resolved through erosion/merging, but artefacts can occur at tile edges.

- Product versions and formats:
  - Vector data (polygons): standard ESRI shapefile.
    - Level 2: 26 Subclasses (most widely used).
    - Level 3: up to 72 Variant level detail (high detail may vary; Level 3 available by special arrangement with CEH).
  - Raster data (GeoTIFF):
    - 25 m resolution with 26 Subclasses.
    - 1 km resolution with Subclass level, Dominant values, and Percentage values; also 10 Aggregate classes with Dominant and Percentage.
  - Raster datasets are not directly comparable with LCM1990 and are not suitable for estimating change over the 10-year period.

- Dataset coverage and structure:
  - Compiled on a 100 km tile basis; parcels are classified per tile and then merged.
  - Vector attributes include unique parcel SegID, dominant class (BHSub), optional Variant (BHSubVar), PerPixList (Level 3), OpHistory (processing history), TotPixels, and CorePixels.

- Nomenclature and data detail:
  - Vector provides Subclass and Variant detail; a coded mapping (Subclass/Variant codes) is documented.
  - The ability to distinguish at Variant level depends on the dominant land cover at image time; post-harvest distinctions may not be possible.

- OpHistory and data lineage:
  - Each parcel contains an OpHistory field describing input data, imaging dates, processing steps, knowledge-based corrections (KBC), and other info.
  - Includes scene/sensor/date details and six key indicators (spectral probability, probability aggregation flag, Phase 1 and Phase 2 KBC rules, plus an edge/quality flag).

- Colour mapping and habitat descriptions:
  - Table-driven colour recipes provide display colors for the 26 Subclasses (HSV/RGB and approximate RGB).
  - Broad Habitat descriptions (Table 6) define 16 broad habitat categories (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Inland water, Montane habitats, Inland rock, Built-up areas, Coastal habitats).

- Usage, customization, and governance:
  - LCM2000 is intended as a data storage/analysis framework; users are encouraged to customize and expand while retaining parcel-level metadata and SegID for traceability.
  - Unique SegID labeling should be retained to enable unambiguous communication with the data management team.
  - The production philosophy emphasizes preserving information richness and documenting changes; any attribute modifications should preserve lineage.

- Production philosophy and accuracy:
  - Emphasis on retaining as much information as possible; maintain lineage and metadata for transparency.
  - Users should distinguish between true inaccuracy and differences due to data model, scale, resolution, interpretation, or classification targets.
  - Acknowledges inherent inaccuracies but frames them within the data’s purpose and design.

- Practical guidance and references:
  - See the Land Cover Map home page for data access and enquiries; methodology references include Fuller et al. (2002) and Smith et al. (2001) on parcel-based map construction; detailed Broad Habitat guidance by Jackson (2000).