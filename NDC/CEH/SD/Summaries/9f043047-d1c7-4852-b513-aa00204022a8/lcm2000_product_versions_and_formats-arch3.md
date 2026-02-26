# LCM2000 specification

- A UK-wide parcel-based land cover map derived mainly from Landsat satellite imagery, upgrading the Land Cover Map of Great Britain (LCMGB) 1990 and extending coverage to Northern Ireland for an all-UK dataset.
- Classified with a hierarchical nomenclature aligned to the Joint Nature Conservation Committee (JNCC) Broad Habitats, enabling detailed habitat representation and broader applicability.
- Available in both vector and raster formats, with multiple product versions offering different detail levels and spatial resolutions.

## Data content and formats

- Formats and versions:
  - Vector data: polygons (land parcels) with per-parcel attributes.
    - Level 2: 26 Subclasses (most widely used).
    - Level 3: up to 72 Variant level; higher detail available by special arrangement.
    - Standard vector format: ESRI Shapefile.
  - Raster data (derived from vector):
    - 25 m resolution: 26 Subclasses.
    - 1 km resolution: Subclass level (26 Subclasses) and Aggregate level (10 simplified aggregates) with Dominant and Percentage values.
  - Note: Raster data are not directly comparable with LCM1990 due to different production methods.
- Accessibility: data are provided with extensive metadata and are suitable for use in GIS environments (ArcGIS with Spatial Analyst, etc.).

## Dataset coverage and structure

- Coverage: UK-wide, produced on a 100 km tile basis; parcels are classified per tile and then mosaicked into a single all-UK dataset.
- Edge handling: parcels crossing tile edges retained in both adjoining tiles; artefacts from edge merging may occur but are minimal (<0.1% of parcels) and manageable by users.
- Unique labeling: each parcel has a SegID for unambiguous provenance and traceability.

## Hierarchical nomenclature and classes

- Subclass and Variant levels provide a detailed classification aligned with Broad Habitats.
- A comprehensive code table maps Subclass and Variant codes (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable crops, Various grassland types, Urban/built-up areas, coastal/shoreline habitats, etc.).
- Contextual information may be used to separate classes where possible, but some distinctions may not be up to date due to imaging timing and changing land cover.

## Vector polygon attributes

- SegID: unique parcel identifier.
- BHSub: dominant land cover type at the subclass level (Level 2).
- BHSubVar: dominant land cover type at the variant level (Level 3).
- PerPixList: per-pixel mix by percentage (Level 3 only).
- OpHistory: processing history details (image date(s), KBC steps, etc.) for the parcel.
- TotPixels / CorePixels: pixel counts for the parcel and its core area used for classification.
- BHSub and BHSubVar fields provide essential lineage and classification detail for monitoring and reproducibility.

## OpHistory attribute details

- The OpHistory (PHD) records contain six fields describing input data and the stages of classification, knowledge-based correction (KBC), and final compilation.
- Includes scene number, sensor (e.g., TM, IRS), acquisition dates, cloud-hole patches, and flags indicating processing specifics (e.g., haze, training data, etc.).
- A separate key explains the meaning of each field, including how to interpret scene numbers, sensor types, and cloud-cover handling.

## Colour recipes and Broad Habitat descriptions

- Colour coding tables map each Subclass to display colors (Hue, Saturation, Value; or RGB equivalents) for intuitive visualization.
- Broad Habitat descriptions provide concise definitions for major habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water/streams, Montane habitats, Inland bare ground, Built-up areas, Coastal habitats, etc.).
- The broad habitat framework supports policy monitoring and communication of habitat distribution changes.

## Data quality, limitations, and caveats

- Change over time: LCM2000 raster is not directly comparable to LCM1990 due to differing construction methods; not suitable for inferring 10-year changes without careful methodological alignment.
- Accuracy and updates: contextual information may aid class separation, but some details may be out of date relative to imaging times; accuracy varies by region and habitat type.
- Edge artefacts and slivers: edge overlaps between tiles can create artefacts; guidance is provided for visual tidying, clipping, dissolving, and preserving important parcel-level metadata.
- Data model considerations: users should distinguish between data model differences, scale, resolution, and interpretation when discussing accuracy; LCM2000 emphasizes preserving as much information as possible and maintaining parcel-level lineage.

## Production philosophy, customization, and governance

- Customisation: LCM2000 is designed as a data storage and analysis framework; users are encouraged to modify and expand their version while retaining parcel-level metadata and provenance.
- Unique labeling: SegID should be retained to maintain traceability and communication with data management teams.
- Production philosophy: maximize information retention; when altering data, maintain lineage and keep original attributes in new fields or separate attributes.
- Documentation: thorough documentation of changes is essential for data management and user feedback.
- Data governance and openness: while metadata and provenance are emphasized, the document acknowledges the importance of transparent data handling and the potential need to preserve open data principles in dissemination.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaic construction and cloud-hole patching; multiple layers of parcels may exist within a 100 km tile.
- Artefacts are rare and generally minor; users can visually tidy boundaries between adjacent parcels of the same class using GIS tools (e.g., dissolving boundaries in ArcMap) without altering source attributes.
- Methods for dealing with edge artefacts:
  - Clip data to tile edges or merge tiles, with awareness that clipping dissolves parcel-level attributes and may affect data provenance.
  - Use union or dissolve cautiously, as some attributes may be invalidated for edge parcels.
  - For Level 3 data, preserve bhSubVar during dissolving to avoid losing key 3-level information.
  - If merging tiles, selection tools can speed up edge dissolution.
- Priority in tile merging: first input tile often takes precedence for edge parcels; differences between tiles may occur where classifications diverge.

## Appendix 2: Good practice

- (Not fully included in the provided text; the document indicates an additional appendix focusing on best practices.)

## Further information and references

- Contact: Land Cover Map team at CEH Wallingford (spatialdata@ceh.ac.uk; +44 1491 838800) and the LCM data page (www.ceh.ac.uk/data/lcm).
- Key publications:
  - Fuller et al. 2002; The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images.
  - Smith et al. 2001; Land Cover Map 2000: a parcel-based map from satellite images.
  - Jackson 2000; JNCC Guidance on the interpretation of the Biodiversity Broad Habitat Classification (terrestrial and freshwater types).
- Broad Habitat classification reference and detailed descriptions are provided to support interpretation and integration into monitoring frameworks.