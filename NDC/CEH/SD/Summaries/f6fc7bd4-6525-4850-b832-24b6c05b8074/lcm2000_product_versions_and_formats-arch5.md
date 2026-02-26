# LCM2000 specification

## Introduction
- LCM2000 is a parcel-based thematic land-cover classification for the entire United Kingdom, updating the Land Cover Map of Great Britain (LCMGB) 1990.
- Derived mainly from Landsat satellite imagery, with additional data sources, covering all of the UK including Northern Ireland.
- Classified with a hierarchical nomenclature aligned to the JNCC Broad Habitats.
- Available in both vector and raster formats, with several versions offering different detail levels and resolutions.
- Not directly comparable to the LCM1990 dataset due to differing production methods.

## LCM2000 specification
- Maps land cover; includes a minimum mappable parcel size of >0.5 ha; smaller parcels are dissolved into surrounding areas.
- Features a hierarchical class structure: Target and Subclasses aimed at Broad Habitats, with additional Variant levels where provided (not always with the same accuracy).
- Vector data is provided as polygons ( parcels ) with attached attributes; raster data is derived from the vector database and provided at 25 m and 1 km resolutions.

## Product versions overview
- Vector data formats:
  - Level 2: standard detail with 26 LCM2000 Subclasses (most widely used).
  - Level 3: detailed down to 72 Variant level; higher uncertainty in some areas; available by special arrangement with CEH.
  - Standard vector format is ESRI shapefile; ArcGIS may require Spatial Analyst for advanced analysis.
- Raster data formats (derived from vector):
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: Subclass level (26 Subclasses) with Dominant values and Percentage values, plus Aggregate class level (10 simplified aggregates) with Dominant and Percentage values.
- Raster data are GeoTIFF files; ArcGIS Spatial Analyst may be required for analysis.
- Important caveat: the LCM2000 raster dataset is not directly comparable with the LCM1990 dataset.

## Dataset coverage
- Compiled on a 100 km tile basis; classifications are added to corresponding tiles.
- Consists of all UK land areas, including Northern Ireland; some tiles are merged for construction efficiency.
- Edge overlaps between tiles are common and require careful handling.

## Hierarchical nomenclature
- Vector data offer both Subclass and Variant detail; Subclass and Variant codes are provided (e.g., broad-leaved/mixed, coniferous woodland, arable crops, etc.).
- Table 2 lists the mapping codes for Subclass and Level 3 Variants.
- Contextual information may be used to distinguish classes where possible, but accuracy varies by area and timing of imagery.

## Vector polygon attributes
- Each parcel has a set of attributes, including:
  - SegID: unique parcel identifier (includes 100 km square and segment number).
  - BHSub: dominant land cover subclass code.
  - BHSubVar: dominant land cover variant (Level 3) when available.
  - PerPixList: per-pixel breakdown of top spectral subclasses (Level 3 only).
  - OpHistory: processing history details (image dates, KBC rules, etc.).
  - TotPixels and CorePixels: pixel counts for the parcel and its core area.
- SegID is recommended to be retained to preserve provenance and communication with the data management team.

## OpHistory Attribute
- The OpHistory (PHD) on each parcel records input scene, sensor, acquisition dates, and steps of the classification and knowledge-based corrections (KBC), plus a sixth field for other information.
- Includes details such as which image date and sensor contributed to the parcel’s classification and any patching or reclassification steps.

## Colour recipes for LCM2000 mapping
- The dataset provides color specifications for display of each Subclass (Table 5), aiding consistent visualization in GIS.
- Examples include colors for broad-leaved/mixed woodland, coniferous woodland, arable crops, improved grassland, and urban/built-up areas.

## LCM2000 Broad Habitat descriptions
- Table 6 outlines descriptions for 16 Broad Habitat groups (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved/Neutral/Calcareous/ Acid grassland; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water; Montane habitats; Inland bare ground; Built-up areas; Coastal habitats).
- Each category includes notes on interpretation, spectral distinctions, and potential ambiguities.

## Further Information
- For data access and methodology, contact CEH Spatial Data / Land Cover Map team (spatialdata@ceh.ac.uk; phone numbers provided).
- References for methodology and classifications:
  - Fuller et al. 2002; Smith et al. 2001/2002; Jackson 2000 (JNCC Broad Habitat guidance).

## Appendix 1: Dealing with edge overlap problems
- Edge overlaps arise from mosaicked, overlapping imagery used to create 100 km tiles; overlaps are removed by erosion and merging to produce a single parcel layer.
- Parcels straddling tile edges may be retained in adjacent tiles; edge artefacts (~<0.1% of parcels) are possible.
- Artefacts can include boundary differences, slivers, and varying classifications at tile edges.
- Visual or programmatic approaches to mitigate edge artefacts:
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class using GIS legend tools.
  - Clipping to tile edges or merging tiles (uses Geoprocessing wizard, Merge Themes); note that editing attributes post-merge can invalidate source metadata.
  - Use Union to retain both tile attributes (with caution to attribute validity).
  - For Level 3 data, ensure Level 3 bhsubvar information is preserved during dissolves.
  - Prioritize the first input tile during merges; some edge parcels may differ between tiles, affecting outcomes.
  - When parcels share the longest boundary with similar classes, intelligent dissolving can reduce edge artefacts without destroying attribute data.

## Appendix 2: Good practice
- (Not detailed in the excerpt; generally emphasizes maintaining provenance, documentation, and respecting data lineage when editing or combining datasets.)
- Unique SegID labeling should be retained to support clear communication with data management and other users.
- Production philosophy stresses preserving information; when altering data, maintain lineage in new attributes or copies.