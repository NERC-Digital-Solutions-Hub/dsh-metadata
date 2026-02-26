# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map for the entire United Kingdom, derived from satellite imagery (mainly Landsat) and supplementary datasets, covering Great Britain and Northern Ireland to form an all-UK dataset.
- It is classified against a hierarchical Broad Habitat framework aligned with JNCC Broad Habitats, capturing a wide range of UK habitats and offering detailed subclass/variant information where possible.
- Available in both vector and raster formats, with multiple product versions offering different levels of detail and spatial resolutions.
- Aims to support data use across topics by enabling data extraction, combination, analysis, and the creation of user-self-serve products (dashboards, reports, charts).

- Minimum mapping unit is 0.5 ha; parcels and 0.5 ha or smaller are dissolved into surroundings during production; in limited areas some sub-0.5 ha parcels may remain due to processing.

- Important caveats: LCM2000 raster data are not directly comparable with LCM1990 and are not suitable for estimating change over the 10-year period.

## Product formats and versions

- Vector data (polygons for land parcels) with:
  - Level 2: 26 LCM2000 Subclasses (standard level).
  - Level 3: up to 72 Variant level (more detailed; availability may require special arrangement and additional user support).
  - Standard format: ESRI Shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.

- Raster data (derived from vector):
  - 25 m resolution raster with 26 Subclasses.
  - 1 km resolution raster derived from 25 m data, with two detail levels:
    - Subclass level: data for 26 Subclasses.
    - Aggregate level: 10 simplified aggregates with Dominant and Percentage values per 1 km pixel.
  - Raster formats are GeoTIFF; Spatial Analyst may be needed for analysis.

- Notes:
  - Raster data are not directly comparable to LCM1990 for change detection.
  - 1 km rasters provide either Subclass-level or Aggregate-level summaries.

## Dataset coverage and structure

- Compiled on a 100 km tile basis; images are classified per parcel and added to their 100 km tile.
- Tiles may be merged during production; some tiles are merged to simplify construction (edge overlaps are common).

## Hierarchical nomenclature

- Vector data offer Subclass detail and, for Level 3, Variant detail.
- Codes map to a structured scheme (Subclass code and Variant codes) with descriptive labels (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, etc.), and Variant codes provide finer distinctions where possible.
- Classification depth and availability of Level 3 variants depend on dominant land cover and imaging context at the time of capture.

## Vector polygon attributes

- SegID: Unique parcel identifier (tracks to the OS 100 km square and segment).
- BHSub: Dominant land cover type (Level 2 Subclass code).
- BHSubVar: Level 3 Variant code (where present).
- PerPixList: Per-pixel top five spectral subclasses within the segment (Level 3 only).
- OpHistory: Processing history details (image dates and knowledge-based correction steps).
- TotPixels: Total pixels within the parcel.
- CorePixels: Pixels used for the maximum likelihood classification.

- OpHistory is a multi-field descriptor documenting input data, phase 1 and 2 KBC (knowledge-based correction) rules applied, and other information.

## OpHistory attribute details

- Contains a per-segment descriptor with fields recording:
  - Scene number and sensor, acquisition dates.
  - Single-date cloud-hole patches and spectral probability metrics.
  - Counts of phase 1 and phase 2 KBC rules applied.
  - An additional processing history flag, and other metadata.

- Tables provide the mapping of scenes, sensors, and dates used during classification.

## Colour mapping (colour recipes)

- A predefined colour ramp for display of the 26 Subclasses (and associated subclasses) is provided, with HSV/RGB values to ensure consistent visual representation in GIS/visualisation software.

- Examples include colours for Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Setaside grass, Neutral grassland, Calcareous grassland, Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Inland water, Montane habitats, Inland bare ground, Suburban/urban development, Continuous urban, Supra-littoral and Littoral habitats, etc.

## LCM2000 Broad Habitat descriptions

- 16 broad habitat groups (and associated labels) with descriptive definitions, including:
  - Broad-leaved/mixed and yew woodland; Coniferous woodland; Arable and horticulture; Improved grassland; Neutral grassland; Calcareous grassland; Acid grassland; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing open water and canals; Rivers/streams; Montane habitats; Inland rock; Built-up areas and gardens; Supra-/Littoral habitats (coastal).
- Each description outlines typical vegetation structure, management considerations, and distinctions between similar habitat types.
- Some marine and coastal categories are described at subclass/habitat level rather than distinct in every coastal zone.

## Further Information

- Data access and support: CEH Land Cover Map page, CEH contact details, and pricing information.
- Methodology references:
  - Fuller et al. 2002: The UK Land Cover Map 2000 – construction of a parcel-based vector map from satellite images.
  - Smith et al. 2001: Land Cover Map 2000 – a parcel-based map from satellite images.
  - Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification.
- For Broad Habitat classification details, refer to JNCC guidance (Table and descriptions provided in the document).

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaic stitching of multiple overlapping images and cloud-hole patches; 100 km tiles may contain multiple overlapping parcels.
- Overlaps were removed via erosion/merging to create a single parcel layer; some edge parcels straddle tile edges and may be duplicated across adjacent tiles.
- Artefacts at tile edges are typically very rare (<0.1%) and can be mitigated by user-led tidying.
- Practical guidance for users:
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class using legend tools (avoid dissolving across the whole dataset to preserve parcel-level attributes).
  - Clipping or merging tiles can affect parcel-level attributes; consider the implications on per-parcel metadata when choosing to clip or union.
  - For Level 3 data, preserve BHSubVar during dissolve to avoid losing Level 3 information.
  - Use selective dissolves and the ArcMap select feature tool to manage edge areas efficiently.
  - Priority when merging: the first input tile’s attributes can take precedence at the edge; some parcels may show differing classifications at the edge depending on tile order.
  - Slivers: small parcels (< minimum mappable size) can be dissolved or intelligently dissolved into neighboring parcels; retain awareness of their potential impact on the dataset.

## Appendix 2: Good practice

- (Not detailed in the provided text; referenced as an additional guidance section.)

## Customisation and production philosophy

- LCM2000 is designed as a data storage and analysis framework; users are encouraged to customize and expand their version.
- Unique SegID labels should be retained to maintain traceability and facilitate communication with data management teams and other users.

- Production philosophy: retain as much information as possible and document lineage; when altering data, maintain a copy of original attributes or record changes in new attributes to preserve provenance.

## Accuracy and interpretation

- Users should differentiate between actual inaccuracies and differences due to data model, scale, resolution, interpretation, or target class definitions.
- LCM2000 acknowledges inherent inaccuracies; discrepancies with user needs may stem from modeling or classification choices rather than measurement error alone.