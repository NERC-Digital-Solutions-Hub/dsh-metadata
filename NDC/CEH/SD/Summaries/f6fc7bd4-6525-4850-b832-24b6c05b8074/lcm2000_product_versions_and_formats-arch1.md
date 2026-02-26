# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based, thematic land-cover map for the entire United Kingdom, including Northern Ireland.
  - Derived from satellite imagery (mainly Landsat) with additional ancillary datasets; updates and upgrades the LCMGB 1990 map.
  - Classified using a hierarchical nomenclature aligned to the Joint Nature Conservation Committee (JNCC) Broad Habitats.
  - Produced in both vector and raster formats, with multiple versions at different detail levels and resolutions.
  - Not directly comparable to the LCM1990 dataset due to different methodologies.

- Product versions and formats
  - Vector data (parcels) with attributes:
    - Level 2: 26 Subclasses (most widely used).
    - Level 3: 72 Variant level (more detailed; variable accuracy; requires special arrangement with CEH).
    - Standard vector format is ESRI shapefile; ArcGIS may require Spatial Analyst for analysis.
  - Raster data (from vector):
    - 25 m grid: 26 Subclasses.
    - 1 km grid: summarised at Subclass and Aggregate class levels; includes Dominant values and Percentage values.
  - Raster formats: GeoTIFF; again, Spatial Analyst extension may be needed in ArcGIS.
  - Important note: Raster data are not directly comparable with LCM1990.

- Dataset coverage and structure
  - Classified on a 100 km tile basis; parcels are added to their corresponding tiles.
  - Tiles may be merged; some edge effects and artefacts can arise at tile boundaries.
  - Edge overlaps were removed through erosion/merging to produce a single parcel layer per tile.
  - Parcels straddling tile edges may be retained in both adjoining tiles.

- Hierarchical nomenclature
  - Vector data include both Subclass and Variant detail (Level 3).
  - Codes correspond to Broad Habitat classifications; Variant level detail provides finer distinctions where available.
  - Classification quality for Level 3 can vary regionally; some labels may depend on dominant land cover at image time.

- Vector polygon attributes (Parcels)
  - SegID: Unique parcel identifier (includes OS 100km square and segment number).
  - BHSub: Dominant land-cover type (Level 2 subclass code).
  - BHSubVar: Dominant land-cover type (Level 3 variant code, when present).
  - PerPixList: Top five spectral-subclass percentages within the parcel (Level 3 only).
  - OpHistory: Processing history details (image date(s), KBC rules applied).
  - TotPixels: Total pixels in the parcel.
  - CorePixels: Pixels in the parcel’s core area used for classification.

- OpHistory attribute and processing history
  - Encodes scene number, sensor, acquisition dates, and per-pixel classification details.
  - Includes knowledge-based corrections (KBC) and whether probability aggregation was applied.
  - Provides a detailed trail of input data and processing steps for quality control and audit.

- Colour recipes for mapping (Table 5)
  - Specifies recommended display colors (Hue, Saturation, Value and approximate RGB) for each of the 26 Subclasses.
  - Also indicates colors for Level 3 variants where available.

- Broad Habitat descriptions (Table 6)
  - Descriptions of the 16 Broad Habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water/ coastal habitats, Montane habitats, Inland bare ground, Built-up areas, Supra-littoral/Littoral habitats, etc.).
  - Defines criteria and nuances for mapping and interpretation of each broad habitat category.

- Practical guidance for use
  - LCM2000 is an information-rich dataset intended for storage, analysis, and as a foundation for further research.
  - Users are encouraged to preserve parcel-level metadata (SegID, lineage, and processing history) to maintain traceability.
  - Customisation is supported; users can alter and expand the database while maintaining documentation of changes.

- Edge overlap and artefacts (Appendix 1)
  - Mosaic construction creates multiple overlapping parcels within 100 km tiles.
  - Overlaps are removed by erosion/merging; edge artefacts can occur (e.g., parcels classified using different imagery, edge boundaries retained, slivers).
  - Artefacts are usually minor (<0.1% of parcels) but may require user tidying.

- Visual and data-handling guidance for edge artefacts
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class without degrading source data.
  - Data handling options in ArcMap:
    - Clip to 100 km edge (note: attributes tied to whole parcels may be invalidated).
    - Use Union to merge tiles (retains multiple attribute sets; may require post-processing).
    - Dissolve boundaries between like classes (careful with Level 3 data via bhsubvar; may lose source detail).
  - Edge-merging priority: the first input tile often prevails at the edge; differences can occur if classifications differ.

- Slivers and small parcels
  - Small parcels (< minimum mappable unit) may be present; can be removed visually, dissolved with neighboring parcels, or dissolved intelligently based on longest shared boundary with similar surroundings.
  - Exercise caution to avoid discarding meaningful information.

- Production philosophy and data governance
  - Emphasises retaining as much information as possible; advise keeping parcel-level metadata to document lineage and processing history.
  - Fully documenting changes is essential for traceability and data integrity.
  - Acknowledges that LCM2000 contains inherent inaccuracies; interpret differences with care and consider scale, resolution, and classification definitions.

- Additional information and references
  - For access and inquiries: CEH data portals and contact details.
  - Key references for methodology and classification framework:
    - Fuller et al. (2002) on construction of parcel-based vector maps from satellite images.
    - Smith et al. (2001) on Land Cover Map 2000 methodology.
    - Jackson (2000) guidance on Broad Habitat Classification.

- Appendix 2
  - Good practice appendix exists (not itemized in detail in this summary).