# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map of the United Kingdom, updating and upgrading the 1990 map (LCMGB) and providing all-UK coverage including Northern Ireland.
- It is derived from satellite imagery (primarily Landsat) and integrates ancillary datasets; produced in both vector and raster formats with multiple versions at different detail levels and resolutions.
- The classification aligns to the Joint Nature Conservation Committee (JNCC) Broad Habitats hierarchy, with additional detail where possible, to support a range of users.

## Data formats and detail levels

- Vector data (parcels with attributes)
  - Level 2: standard level with 26 LCM2000 Subclasses (most widely used).
  - Level 3: down to 72 Variant level (special arrangement with CEH; requires more user support).
  - Standard vector format is ESRI shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.
  - Minimum mappable parcel size: > 0.5 ha; parcels ≤ 0.5 ha are dissolved into surrounding landscape during production.
- Raster data (derived from vector)
  - 25 m resolution raster with 26 Subclasses.
  - 1 km resolution raster with Subclass level and two summary options: Dominant values and Percentage values.
  - Aggregated raster formats include 10 Aggregate classes (from the 26 Subclasses) with Dominant and Percentage options.
  - GeoTIFF format; ArcGIS Spatial Analyst may be required.
  - Note: Raster data are not directly comparable with the 1990 dataset and should not be used to estimate change over the 10-year period.

## Dataset coverage and geography

- Data compiled on a 100 km tile basis; imagery classified per parcel and then assigned to the appropriate 100 km tile.
- Some tiles were merged to simplify construction; edge overlap between tiles is retained for parcels that straddle tile boundaries.

## Nomenclature and attributes

- Hierarchical codes map to Subclass and, where available, Variant levels; a comprehensive mapping table exists (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable crops, Urban, etc.).
- Vector parcels carry a set of attributes:
  - SegID: unique parcel identifier (stable for communications with data managers).
  - BHSub: dominant land cover type (Level 2 code).
  - BHSubVar: dominant land cover type (Level 3 Variant code).
  - PerPixList: top five spectral subclasses per pixel within the parcel (present in Level 3).
  - OpHistory: processing history for the parcel (image dates, KBC rules, etc.).
  - TotPixels: total pixels in the parcel; CorePixels: pixels in the core area used for classification.
- OpHistory (process history descriptor, PHD) provides a structured record of input data and classification steps, including scene number, sensor, acquisition dates, and KBC rule usage.

## Processing history and provenance

- The PHD comprises fields detailing scene, sensor (e.g., TM, IRS), acquisition dates, cloud-hole patching status, and knowledge-based corrections (KBC).
- A detailed Table of scenes, sensors, and acquisition dates accompanies the dataset to support reproducibility and auditability.
- The design emphasizes retaining and documenting lineage and metadata for each parcel.

## Colour mapping and habitat descriptions

- Colour recipes are defined for display of the 26 Subclasses to aid interpretation and visualization (example hues and RGB equivalents provided for key classes).
- Broad Habitat descriptions (Table 6) give summaries for major habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland bare ground, Built-up areas, Coastal habitats).

## Data quality, edge artefacts, and remediation

- Edge overlap problems arise from mosaic imagery and cloud-hole patching across 100 km tiles, producing artefacts at tile edges.
- Artefacts are infrequent (typically < 0.1% of parcels) and may be mitigated by:
  - Visual tidying: dissolving boundaries between adjacent parcels of the same class (via GIS legend tools) without changing parcel attributes.
  - Data processing interventions: clipping to tile edges, merging tiles, or dissolving boundaries; each option has implications for parcel-level metadata.
  - For Level 3 data, preserving bhsubvar during dissolves to avoid losing key classification detail.
  - Selecting edge areas before dissolving to speed up processing and minimize unintended attribute loss.
- When tiles are merged, first input tile may take precedence for edge parcels; differences between tiles may affect edge parcels in some cases.
- Slivers and very small parcels (< minimum mappable unit) may remain; recommended remedies include visual removal, dissolving with adjacent parcels of the same class, or intelligent dissolution based on shared boundaries.
- Users should consider the impact of edge remediation on the integrity of parcel-level meta-data and keep a record of changes.

## Production philosophy, customization, and governance

- Production philosophy: retain as much information as possible; store parcel-level meta-data to document lineage and processing history.
- Customization: the dataset is intended as a storage and analysis framework; users are encouraged to modify and expand their version while preserving a record of original attributes.
- Unique labeling: each parcel has a SegID; recommended to retain this label to maintain unambiguous communications with data managers and other users.
- Documentation of changes is essential for data management and feedback loops to the data management team.
- Accuracy: acknowledge inevitable data-model, scale, resolution, interpretation, and target-class differences; LCM2000 is not a simple one-to-one mapping and may not meet all user expectations.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps occur due to mosaic imagery and cloud-hole filling; steps to resolve include erosion/merge to a single parcel layer.
- Edge parcels may exist in multiple tiles; artefacts can include differences in parcel classification and attribute values.
- Visual cleanup and GIS operations (clip, union, dissolve) are described, with cautions about loss of parcel-level metadata and complexity when using Level 3 attributes.
- Precedence and potential attribute mismatch are discussed; strategies to minimize impact include targeted dissolves and selective edge-area processing.

## Appendix 2: Good practice

- The document references additional guidance on good practice, encouraging preservation of metadata and careful management of lineage, though detailed content is not included here.

## Further information and references

- Land Cover Map home page: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk; +44 (0)1491 692315
- Key references:
  - Fuller et al. 2002; "The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images." Cartographic Journal.
  - Smith et al. 2001; "Land Cover Map 2000: a parcel-based map from satellite images." Remote Sensing Society proceedings.
  - Jackson 2000; JNCC Report No. 307: guidance on Broad Habitat classification.