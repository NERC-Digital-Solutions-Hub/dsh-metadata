# LAND COVER MAP 2007 DATASET DOCUMENTATION

- UK-wide parcel-based land cover classification (LCM2007) using 23 Broad Habitat-based classes derived from 20–30 m satellite imagery.
- Provides a range of data products (vector and raster) to support varied applications; not a land-use map.
- Built to upgrade LCM2000 with improved spatial framework (OSMM and Landsat-era data) and richer metadata; guidance recommends consulting the Final Report for full methodology and limitations.

## Data content and structure

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes (including Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Unique Parcel_ID per polygon; BHSub provides Broad Habitat sub-class descriptions; FieldCode offers mapping codes (not QA’d for strict use).
  - 23 LCM2007 classes tied to Broad Habitats; supports communication via a standard internal coding (INTCODE) and accompanying metadata.
- Raster Data Sets
  - 25 m and 1 km products derived from the vector dataset; GB and NI provided separately due to different projections.
  - 25 m raster uses 23 LCM2007 classes; 1 km raster products include dominant and percentage cover for both LCM2007 classes and their Aggregate classes (for broader analyses).
  - Data specifications include pixel counts, extents, coordinates, projections, and datums (GB: OSGB36; NI: Ireland 1965; GB/NI projections differ – see Table metadata).
- Map Projection and Coordinate System
  - GB data: British National Grid (Transverse Mercator, OSGB36).
  - Northern Ireland data: Irish National Grid (Transverse Mercator, Ireland 1965), with NI moving toward ITM in future GIS workflows.
- Minimum Mapping Unit
  - Parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape during production.
- Data Size
  - Vector (100 km x 100 km shapefile): GB ~ 4.13 GB; NI ~ 433 MB.
  - Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB.
  - 1 km raster products: smaller files (e.g., 21 MB to 49 KB for various products).

## Classification and metadata

- 23 LCM2007 classes are based on UK Broad Habitats; some classes are subdivided to reflect spectral distinctions (e.g., Built-up Areas subdivided into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment split into Littoral sediment and Saltmarsh).
- Broad Habitat Sub-classes (BHSub) exist for descriptive purposes, not all are as reliable as the primary LCM2007 class; ProbList provides the top five spectral class probabilities per polygon.
- Knowledge-Based Enhancements (KBE) describe processing history and adjustments (e.g., soil correction, altitude correction, urban masks).
- Validation and accuracy
  - Ground reference data enabled validation against 9127 polygons; average accuracy ~83%.
  - Accuracy is an average; local discrepancies may occur; users should validate sub-class usage where precision is critical.
  - Caution: some grassland mis-classifications (Neutral/Calcareous grasslands vs. Improved grassland) noted; recommended aggregation or user validation for grassland sub-classes.
- Appendices (reference material)
  - Appendix 1: LCM2007 class descriptions (definition notes for each Broad Habitat).
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping guidance).
  - Appendix 3: Colour mapping recipe for display (RGB values assigned per LCM2007 class).

## Data access and licensing

- 1 km raster data sets accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; online application process available.
- Licence fees may apply for some users and applications.

## Quality, limitations, and governance

- LCM2007 maps land cover (not necessarily land use); interpretation should consider that some land cover signatures do not uniquely determine land use.
- The MMU and segmentation approach may affect small features; 0.5 ha threshold reduces noise and improves reliability at larger scales.
- Sub-class level analysis requires independent validation; Broad Habitat generalizations are more robust than Broad Habitat sub-classes.
- The documentation advises consulting Morton et al. (2011) Final Report for a comprehensive methodology, limitations, and accuracy discussion; cross-reference with Jackson (2000) for Broad Habitat definitions.

## Practical considerations for data leaders

- LCM2007 provides rich, well-documented land-cover assets suitable for integration into national data systems, policy analysis, and environmental reporting.
- The dataset’s size, structure, and licensing imply planning for storage, processing capacity, and access controls; retaining Parcel_ID enhances traceability and communication among users.
- Given scattered data origins, cross-referencing with other datasets (e.g., ground references, other land cover maps) is recommended, especially when working with grassland and montane/sub-class analyses.
- For broad-scale modelling or UK-wide analyses, 1 km raster products offer an efficient summary with suitable accuracy; for detailed mapping, vector and 25 m rasters provide higher thematic detail with richer metadata.
- Users should plan validation steps, especially when relying on sub-classes or ProbList-derived classifications.

## References and further information

- Morton, D. et al. (2011). Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on interpretation of the Biodiversity Broad Habitat Classification (terrestrial and freshwater types).

- Note: This document also provides detailed mappings between LCM2007 classes and Broad Habitats (Appendix 2) and color mappings (Appendix 3) for display and interpretation.