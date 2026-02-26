# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite image data covering the United Kingdom, updating and upgrading the Land Cover Map of Great Britain (LCMGB) 1990.
- Derived primarily from Landsat imagery with additional ancillary data; provides an all-UK dataset including Northern Ireland.
- Classified using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, and extended where possible for wider user needs.
- Produced in both vector (parcels) and raster formats, with multiple versions at varying detail and resolutions.
- Important caution: the LCM2000 raster dataset is not directly comparable with the LCM1990 dataset due to different construction methods and should not be used to estimate change over the 10-year period.

## Product versions and data formats

- Vector data formats
  - Level 2 (standard detail): 26 LCM2000 Subclasses.
  - Level 3 (detailed): 72 Variant level, available by special arrangement; higher detail may vary by area and requires expert interpretation.
  - Standard vector format is ESRI shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.
- Raster data formats
  - 25m resolution: 26 Subclasses.
  - 1km resolution: derived from 25m data; includes Subclass level (26), Dominant values and Percentage values at 1km; also Aggregate class level (10 areas) with Dominant and Percentage values.
  - Raster data are provided as GeoTIFF; Spatial Analyst may be required in ArcGIS.
- Minimum mapping unit: >0.5 ha; parcels smaller than 0.5 ha are dissolved into surrounding landscape during production.
- Note: Raster data are not directly comparable to LCM1990.

## Dataset coverage and hierarchical nomenclature

- Data compiled on a 100km tile basis; parcels classified per tile and then added to the tile dataset.
- Vector data provides both Subclass (Level 2) and Variant (Level 3) details.
- Subclass and Variant codes are defined in accompanying tables; broad habitat classes reflect UK habitats per JNCC standards.
- Class Variants (Level 3) provide additional detail but may not always achieve the same accuracy/consistency across all areas.
- The ability to distinguish at Variant level depends on the dominant land cover at imaging time; distinctions may be limited after harvest or other seasonal changes.

## Vector polygon attributes

- Each land parcel (segment) carries a set of attributes:
  - SegID: unique identifier for each parcel, including OS 100km square and segment number.
  - BHSub: dominant land cover type at Subclass level (Level 2).
  - BHSubVar: dominant land cover type at Variant level (Level 3).
  - PerPixList: top five spectral subclasses per pixel list within the parcel (present in Level 3).
  - OpHistory: processing history descriptor detailing input data, classification steps, and knowledge-based corrections (KBC).
  - TotPixels: total number of pixels in the parcel.
  - CorePixels: pixels within the core area used for maximum likelihood classification.
- The OpHistory descriptor (PHD) includes six fields (scene, sensor, image dates, patch status, KBC rule counts, and an additional flag/notes) and a sixth field with other information; an example and a companion table explain the field codes.

## OpHistory attribute (processing history)

- Each parcel records input data and classification steps, including:
  - Scene number and the specific imagery used (different sensors such as TM, IRS; summer/winter images).
  - Image acquisition dates and whether cloud holes were patched from alternate dates.
  - The number of phase 1 (scene-dependent) and phase 2 (UK-wide) KBC rules applied.
  - A spectral probability indicator and aggregation flags indicating the use of probability rules.
  - A flag describing edge conditions or artefacts (e.g., eroded, grown, void filled, training data references).

## Colour mapping for display (LCM2000)

- Colour recipes define display colors for the 26 Subclasses, including hue, saturation, value, and approximate RGB equivalents.
- Examples include:
  - Broad-leaved / mixed woodland (1.1): vivid display with specific RGB values.
  - Coniferous woodland (2.1): distinct hues and RGB values.
  - Arable cereals (4.1) and Arable non-rotational (4.3) with unique color ramps.
  - Built-up areas / urban (17.x): dark tones for urban development.
  - Water-related classes (13.1 Inland water and 22.x Sea & estuary) with blues and related palettes.
- These color assignments facilitate quick visual interpretation of 26 Subclasses across maps and displays.

## LCM2000 Broad Habitat descriptions

- Broad Habitat categories provide a high-level interpretation of UK land cover, including:
  - Broad-leaved / mixed woodland and Coniferous woodland.
  - Boundaries and linear features (hedges, walls, roads).
  - Arable and horticulture, and various grassland types (Improved, Neutral, Calcareous, Acid) and related mixtures.
  - Bracken and Dwarf shrub heath; Fen, marsh and swamp; Bog; Standing water and canals.
  - Montane habitats; Inland rock; Built-up areas and gardens; Coastal habitats ( Supra-littoral and Littoral) including rock and sediment types.
  - Distinctions between inland water, rivers/streams, and various coastal/subtidal classifications.
- Each broad habitat entry includes a description of the vegetation structure and typical management considerations, noting where spectral separations or field knowledge impact accuracy.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaic imagery and cloud-hole patches; multiple overlapping parcels can exist within a 100km tile.
- Artefacts may occur at tile edges; issues include different classifications for the same parcel across tiles, slivers, and boundary fragmentation.
- Guidance to users:
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class using GIS tools; do not dissolve across the entire dataset to preserve parcel-level metadata.
  - Edge merging and clipping: options include clipping to tile edges or merging tiles, but each approach can invalidate certain parcel-level attributes (e.g., SegID continuity, source attributes).
  - For Level 3 data, preserve bhsubvar during dissolves to avoid losing critical Level 3 information.
  - Use selective dissolves or nearest-boundary dissolves to minimize artefacts while retaining data lineage.
  - When merging tiles, first input tile often takes precedence at edges; some edge parcels may appear differently depending on tile order.
- Slivers and very small parcels can be handled by visual removal, dissolving with adjacent same-class parcels, or intelligent dissolving based on boundary length with neighboring parcels.

## Appendix 2: Good practice

- (Not included in excerpt; referenced as a section that provides recommended practices for handling LCM2000 data and workflows.)

## Customisation, production philosophy and data governance

- LCM2000 is designed as a data storage and analysis framework, not just a map; users are encouraged to modify and expand the database for their needs.
- Unique SegID labeling is retained to enable unambiguous communication with the data management team and among users.
- Production philosophy emphasizes preserving information richness; maintain parcel-level metadata to record lineage and processing history.
- When altering data, retain original attributes or copy them to new attributes to preserve provenance.
- Fully document changes to enable traceability and security.

## Further information and limitations

- For data access and methodology details, contact CEH’s Land Cover Map team or visit the LCM homepage.
- References provide methodological context and definitions:
  - Fuller et al. (2002) on the construction of a parcel-based vector map from satellite images.
  - Smith et al. (2001) on Land Cover Map 2000 parcel-based mapping.
  - Jackson (2000) guidance on interpreting the Biodiversity Broad Habitat Classification.
- Accuracy and correspondence notes emphasize that LCM2000 contains inevitable inaccuracies due to data model, scale, resolution, interpretation, and target class definitions; users should interpret differences with these caveats in mind.