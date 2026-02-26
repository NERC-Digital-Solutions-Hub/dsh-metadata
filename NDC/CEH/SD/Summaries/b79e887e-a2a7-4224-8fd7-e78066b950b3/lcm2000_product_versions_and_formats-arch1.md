# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of UK satellite imagery (primarily Landsat) that updates and extends the Land Cover Map of Great Britain (LCMGB) 1990, covering Northern Ireland for the first time to provide an all-UK dataset.
- Classifies land cover using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, with additional detail for wider user needs.
- Available in both vector and raster formats, with multiple versions offering varying levels of detail and spatial resolutions.

## Product versions and data formats

- Vector data
  - Level 2: Standard detail with 26 LCM2000 Subclasses (most widely used).
  - Level 3: Detailed down to 72 Variant level; higher detail quality varies geographically and may require expert interpretation; available by special arrangement with CEH staff.
  - Standard vector format is ESRI shapefile; ArcGIS users may need the Spatial Analyst extension for advanced analysis.
- Raster data
  - 25 m resolution raster covering 26 Subclasses.
  - 1 km resolution raster summarized from 25 m data with three detail options: Subclass level, Dominant values, and Percentage values; plus 10 Aggregate classes with Dominant and Percentage options.
  - Standard raster format is GeoTiff; Spatial Analyst extension may be required.
- Note: The LCM2000 raster is not directly comparable with LCM1990 due to different construction methods, and is not suitable for estimating change over the 10-year period.

## Dataset coverage and scale

- Compiled on a 100 km tile basis; imagery classified per parcel and added to the corresponding tile.
- Tiles may be merged and some edge parcels straddle tile boundaries; overlaps were removed through erosion and merging to create a single parcel layer per tile.
- LCM2000 supports UK-wide analysis but edge artefacts can occur due to mosaic construction and edge processing.

## Hierarchical nomenclature

- Vector data provides Subclass and Variant detail (Level 2 and Level 3 respectively).
- 26 Subclasses underpin the Broad Habitat framework; Level 3 adds 72 Variant codes for finer differentiation.
- Codes are mapped to descriptive broad habitat categories; the dataset includes alpha and numeric codes (e.g., 1.1 Broad-leaved/mixed woodland; variants like Deciduous, Conifers, etc.).

## Vector polygon attributes

- SegID: Unique label for each land parcel (and per-parcel identity retained for provenance).
- BHSub: Dominant land cover type at Subclass level.
- BHSubVar: Variant-level dominant land cover type (Level 3).
- PerPixList: Top-five spectral subclasses by pixel percentage for each parcel (Level 3 only).
- OpHistory: Processing history descriptor detailing input data, dates, and knowledge-based corrections (KBC) applied.
- TotPixels: Total pixels in the parcel.
- CorePixels: Pixels in the parcel core used for maximum likelihood classification.
- Additional fields and indicators (e.g., quality flags, atlas references) accompany the core attributes.

## OpHistory attribute (process history)

- Encodes input data, scene numbers, sensors, acquisition dates, and processing steps (KBC rules) used in classification.
- Includes a six-field descriptor with a seventh field for other information, such as data gaps, 0-coded “outside normal flowline” classifications, and notes on training data.

## Colour recipes and visualization

- A defined color scheme is provided for 26 Subclasses to aid map visualization and interpretation.
- Colors are specified in terms of Hue, Saturation, Value (HSV) and approximate RGB equivalents for each Subclass.

## Broad Habitat descriptions

- Descriptions cover major habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water and wetlands, Montane habitats, Inland rock, Built-up areas, Coastal/habitat classes).
- Each description clarifies typical vegetation, management implications, and distinctions at subclass level where relevant.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaic assembly of multiple overlapping scenes; 100 km tiles retain overlaps that are then removed by erosion/merging to a single layer.
- Artefacts are rare (generally <0.1% of parcels) but can occur, especially near tile edges.
- Practical guidance for tidying visually:
  - Dissolve boundaries between adjacent parcels of the same class for a cleaner view (without altering the underlying attribute data globally).
  - Use ArcMap legend tools to dissolve edges locally; avoid dissolving across the whole map to preserve parcel-level metadata.

## Appendix 1: Visual and data integrity considerations for edge problems

- Methods to address edge artefacts include clipping to tile edges, using Merge Themes, or Union, with trade-offs in attribute integrity and processing time.
- When dissolving, ensure Level 3 BHSubVar data is preserved to avoid loss of important classification details.
- If merging tiles, precedence of the first input tile affects edge attributes; visible differences may occur where tiles disagree on parcel classification.

## Appendix 2: Good practice

- Encourages user-driven customization and expansion of the database while maintaining data provenance.
- Maintain the SegID for unambiguous communication with data management teams and other users.
- Document changes and preserve original attributes; adopt a lineage-tracking approach before altering data.

## Production philosophy and data integrity

- The production approach retains as much information as possible, creating an information-rich dataset.
- Users are advised to keep parcel-level metadata to record lineage and processing history when modifying data.
- Avoid mischaracterizing differences caused by data model, scale, resolution, or interpretation as inaccuracies; LCM2000 acknowledges inherent uncertainties.

## Additional information and references

- Data and methodology resources available from the Land Cover Map home page and CEH contact points.
- Foundational methodology publications include Fuller et al. (2002) on parcel-based map construction and Smith et al. (2001) on an early parcel-based mapping approach.
- Broad Habitat classification definitions and relationships are documented by Jackson (2000) for alignment with biodiversity classifications.