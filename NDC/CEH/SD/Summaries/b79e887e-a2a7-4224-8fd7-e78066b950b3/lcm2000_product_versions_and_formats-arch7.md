# LCM2000 specification

## Introduction
- LCM2000 is a parcel-based thematic land cover map for all of the United Kingdom, built from satellite imagery (mostly Landsat) with enhancements from ancillary data.
- Available in both vector (parcel-based polygons) and raster formats, with multiple versions at different detail levels and spatial resolutions.
- Classified using a hierarchical nomenclature aligned to the JNCC Broad Habitats, covering broad habitat types and providing additional subclass and variant detail where possible.
- Note: raster data are not directly comparable with LCM1990 due to different construction methods; the dataset is not suitable for straightforward ten-year change estimation.

## Product versions overview
- Vector data formats
  - Level 2: standard detail with 26 LCM2000 Subclasses (most widely used).
  - Level 3: up to 72 Variant levels (more detailed; quality varies by area; special arrangement with CEH required).
  - Standard vector format is ESRI shapefile (ArcGIS users may need Spatial Analyst for advanced analysis).
- Raster data formats
  - 25 m resolution raster with 26 Subclasses.
  - 1 km resolution raster derived from the 25 m data, with two detail levels:
    - Subclass level (26 Subclasses).
    - Aggregate level (10 simplified Aggregates).
  - For 1 km data: Dominant values and Percentage values per pixel at Subclass and Aggregate levels.
  - Standard raster format is GeoTIFF (Spatial Analyst may be required in ArcGIS).
- Coverage: all UK, including Northern Ireland; 100 km tile-based organization; edge handling requires attention during use.

## Dataset coverage
- Data compiled on a 100 km tile basis; land parcels are classified per parcel and added to the corresponding tile.
- Tiles may be merged at edges to create a single layer; some edge parcels are retained in adjacent tiles.
- Overlaps and edge artefacts can arise from mosaic construction and cloud-hole patching; these artefacts are typically small (<0.1% of parcels) but may require user tidying.

## Hierarchical nomenclature
- Vector data provides both Subclass (Level 2) and Variant (Level 3) detail.
- Subclass codes map to 26 Broad Habitat types; Variant codes provide finer detail (Level 3).
- The documentation includes a mapping table (codes and descriptions) illustrating the relationship between Subclass and Variant levels.

## Vector polygon attributes
- Each land parcel (SegID) carries a suite of attributes:
  - BHSub: dominant land cover type (Level 2) as a hierarchical code.
  - BHSubVar: dominant land cover type (Level 3) as a hierarchical code (Variant).
  - PerPixList: list by pixel percentages of the top five spectral subclasses (Level 3 only).
  - OpHistory: processing history details (image dates, KBC rules, etc.).
  - TotPixels: total pixels in the parcel.
  - CorePixels: pixels within the core area used for maximum likelihood classification.
  - Other attributes include masks and codes for quality and provenance.
- SegID is a unique parcel identifier and is recommended to be retained for traceability.

## OpHistory Attribute
- The processing history descriptor (PHD) on each parcel records input data and stages of classification, knowledge-based corrections (KBC), and final compilation.
- Six fields exist (Scene, Sensor, Acquisition Dates, Cloud-Hole patches, spectral probabilities, KBC rule counts, etc.), plus a seventh field for additional information.
- The OpHistory provides provenance and allows reconstruction of the production steps for each parcel.

## Colour recipes for LCM2000 mapping
- Colour schemes are provided for display of the 26 Subclasses (and related levels) to support map readability.
- Each Subclass has a defined hue, saturation, value and approximated RGB equivalents to aid consistent visualisation in GIS.

## LCM2000 Broad Habitat descriptions
- The Broad Habitat classification includes 26 main habitat groups, with definitions such as:
  - Broad-leaved/mixed woodland and coniferous woodland.
  - Boundaries and linear features.
  - Arable and horticulture, including cereals and various crops.
  - Various grassland types (improved, neutral, calcareous, acid).
  - Bracken and dwarf shrub heath.
  - Fen, marsh and swamp; bog.
  - Standing water, rivers/streams.
  - Montane habitats and inland rock.
  - Built-up areas and gardens.
  - Coastal habitats (supra-littoral and littoral rock/sediment) and inshore sublittoral categories.
- Each description provides guidance on how the habitat type is defined and differentiated in the classification.

## Appendix 1: Dealing with edge overlap problems
- Edge overlaps arise because multiple source images and cloud-hole patches contribute to each 100 km tile.
- Artefacts may include:
  - Differences in parcel classification at tile edges.
  - Slivers or very small parcels from erosion/merging processes.
  - Boundary discontinuities when merging tiles.
- Visual and GIS-based remedies:
  - Visual tidying by dissolving boundaries between adjacent parcels of the same class (preferred over dissolving across the whole dataset to preserve parcel-level attributes).
  - Clipping or merging tiles can affect parcel-level attributes; be aware that dissolved attributes may no longer reflect original data.
  - For Level 3 data, preserve bhsubvar during dissolves to avoid losing important Level 3 information.
  - Use selection tools to isolate edge areas before dissolving to optimize performance.
- Priority and artefacts:
  - When merging tiles, the first input tile often takes precedence for edge parcels (but differences can occur if classifications differ).

## Appendix 2: Good practice
- See Appendix 2 for recommended practices (data handling, documentation, and maintenance guidelines) to preserve data integrity and lineage.

## Customisation and production philosophy
- Production philosophy emphasizes retaining as much information as possible; parcel-level metadata should document lineage and processing history.
- The dataset is an information-rich framework intended for modification and expansion by users.
- Unique SegID labeling provides unambiguous reference to the original data and management team communications.
- Documenting changes and maintaining provenance support robust data management and reuse.

## Production notes: Accuracy and correspondence
- LCM2000 acknowledges inherent inaccuracies due to data models, scale, resolution, interpretation, and class definitions.
- Users should distinguish between true data inaccuracies and differences arising from methodological choices when comparing to other datasets.

## Further Information
- For data access and inquiries: CEH Land Cover Map contact details (spatialdata@ceh.ac.uk; phone numbers provided).
- Methodology references:
  - Fuller et al. 2002 and Smith et al. 2001 papers describing parcel-based map construction from satellite imagery.
  - Jackson 2000 guidance on Broad Habitat interpretation.
- For detailed Broad Habitat definitions and mappings, consult the provided tables and external references.