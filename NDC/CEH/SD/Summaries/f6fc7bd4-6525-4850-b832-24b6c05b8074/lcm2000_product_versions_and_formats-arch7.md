# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map of the United Kingdom, produced from satellite imagery (primarily Landsat) and covering the entire UK including Northern Ireland.
- The dataset is produced in both vector and raster formats, with multiple detail levels and resolutions; it is aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats classification.
- Data are UK-wide, parcel-based, and designed to support map-based data products for GIS analysis and visualization.

## Product formats and versions

- Vector data
  - Standard format: ESRI shapefile (polygons representing land parcels) with attached attributes.
  - Level 2: 26 Subclasses (most widely used).
  - Level 3: up to 72 Variant codes (more detailed; availability requires special arrangement and additional user support).
- Raster data (GeoTIFF)
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: Summary at two detail levels:
    - Subclass level: 26 Subclasses.
    - Aggregate level: 10 Aggregates (plus Dominant and Percentage values per pixel for Subclass and Aggregate levels).
- Raster data are not directly comparable with the earlier LCM1990 dataset due to different construction methods and are not suitable for estimating 10-year change.
- Notes: ArcGIS users may need the Spatial Analyst extension for advanced analysis.

## Dataset coverage and nomenclature

- Coverage: All-UK, including Northern Ireland; compiled on a 100 km tile basis.
- Classification hierarchy: Target classes and Subclasses configured to emphasize Broad Habitats (as defined by Biodiversity Action Plans) and extended for broader use; Variant levels provide additional detail where available.
- Subclass and Variant codes exist for detailed labeling; Variant level details depend on imagery and dominant land cover at imaging time.
- A unique SegID is assigned to each parcel to enable unambiguous data management and communication with the data team.

## Vector polygon attributes

- SegID: Unique identifier for each parcel (combines 100 km tile reference and segment number).
- BHSub: Dominant land cover type at the Subclass level (Level 2).
- BHSubVar: Variant of the dominant land cover type (Level 3, when present).
- PerPixList: Top five per-pixel spectral subclass percentages within the parcel (Level 3 only).
- OpHistory: Processing history; includes image dates and knowledge-based correction steps (KBC) used.
- TotPixels: Total pixels in the parcel.
- CorePixels: Pixels within the core area used for maximum likelihood classification.
- Other metadata may accompany parcels to document provenance and processing steps.

## OpHistory attribute

- The OpHistory (processing history descriptor) contains:
  - Scene number, sensor type, image acquisition dates.
  - Spectral probability information and probability aggregation flags.
  - Phase 1 and Phase 2 KBC rules applied.
  - Additional status flags for edge conditions, training data, and other processing notes.
- This metadata supports traceability of input data and classification decisions.

## Colour and visualization

- LCM2000 provides color recipes for mapping the 26 Subclasses to display colors, enabling consistent and interpretable map visualizations.
- Each Subclass has a defined Hue, Saturation, Value (HSV) and an approximate RGB equivalent to aid rendering in GIS software.

## Broad Habitat descriptions (class framework)

- The LCM2000 methodology uses Broad Habitat classifications that cover themes such as:
  - Broad-leaved/mixed woodland and coniferous woodland
  - Arable and horticulture; Improved grassland; Neutral grassland; Calcareous, acid and other grasslands
  - Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water and canals
  - Montane habitats; Inland rock; Built-up areas and gardens
  - Coastal habitats including supra-littoral and littoral zones
  - Inland water bodies and other landscape types
- Broad Habitats are meant to reflect the main habitat types across the UK and are described in accompanying definitions (e.g., Table 6).

## Edge overlaps and artefacts (Appendix 1)

- Edge overlap issues arise because the dataset combines multiple overlapping images across 100 km tiles and uses cloud-hole patching from alternative dates.
- Artefacts are rare (typically <0.1% of parcels) but can occur at tile edges due to differing source imagery and processing along tile boundaries.
- Recommended user approaches:
  - Visual tidy-up by dissolving boundaries between adjacent parcels of the same class (without altering underlying attribute data).
  - Clip or dissolve strategies may be used to manage edge artifacts, but care must be taken to preserve parcel-level metadata.
  - When merging tiles, the first input tile often has precedence for edge parcels; Level 3 data require using bhsubvar during dissolves to avoid losing important information.
  - Use selective dissolving (e.g., only edge areas) to minimize impact on attribute information.
- Slivers and very small parcels can be removed or dissolved into neighboring parcels with similar classes, or dissolved by the longest shared boundary when appropriate.

## Customisation and production philosophy

- LCM2000 is designed as an information-rich data framework, not just a map.
- Users are encouraged to modify and extend the dataset, while preserving parcel-level meta-data and provenance to maintain traceability.
- Retaining the SegID and other provenance attributes supports communication with data management teams and other users.
- Documentation of changes is emphasized to support data security and effective feedback loops.

## Accuracy and interpretation notes

- Users should distinguish between true inaccuracy and differences arising from data model, scale, resolution, interpretation, or definitions of target classes.
- LCM2000 acknowledges inherent inaccuracies; users should consider the data’s nature and the classification framework when applying it to analysis tasks.

## Further Information and references

- For more information, see the Land Cover Map homepage and the CEH contact details.
- Key literature includes Fuller et al. (2002) on the construction of parcel-based vector maps from satellite images, and related conference papers (2001/2002).
- For Broad Habitat classification details, see Jackson (2000) and JNCC guidance documents.