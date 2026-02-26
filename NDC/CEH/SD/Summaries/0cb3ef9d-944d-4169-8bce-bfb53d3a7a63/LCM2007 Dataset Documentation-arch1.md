# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification with 23 classes based on UK Broad Habitats.
- Created from summer–winter satellite composites with 20–30 m pixels; builds on LCM2000 using OS-based generalised cartography and image segmentation to align with real-world objects (fields, woodland blocks).
- Maps land cover (not strictly land use) and uses a minimum mappable area of >0.5 ha; parcels smaller than 0.5 ha or linear features under 20 m are dissolved into the surrounding landscape.
- Validated against ground reference data with an average thematic accuracy of 83% across 9,127 polygons; local discrepancies can occur.

## Data products and formats

- Vector Data Set
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 10 polygon attributes per feature, including:
    - Parcel_ID: Unique parcel identifier (includes source image reference).
    - BH: Broad Habitat (dominant class).
    - BHSub: Broad Habitat sub-class (describes FieldCode).
    - FieldCode: Short descriptor used in LCM2007 construction.
    - INTCODE: Integer code for display (1–23, the validated LCM2007 class).
    - KBE: Knowledge-Based Enhancement history.
    - ProbList: Top five spectral-class probabilities for the polygon.
    - CorePixels and TotPixels: Pixel counts used for classification.
    - Construct: Derivation history (OSMM, segmentation, etc.).
  - Broad Habitat sub-classes (BHSub) provide additional detail but are not guaranteed to have QA validation at the sub-class level.
  - Parcel_ID should be retained for unambiguous communication.

- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; direct relation to vector classes via a defined mapping.
  - 1 km raster: Aggregated products derived from 25 m raster (dominant class, and percentage cover for both 23 classes and Aggregate classes).
  - Two regional raster sets: Great Britain and Northern Ireland, each with separate projections and extents (GB uses British National Grid; NI uses Irish National Grid).
  - Data metadata in Tables 2 and 3 describes class relationships and raster grid specifications (width, height, extent, pixel size, data type, projection, and datum).

- Data access and licensing
  - 1 km raster data: available via the CEH Information Gateway.
  - Full vector product and 25 m raster product: available under licence on request from CEH (online data application or direct contact); licensing fees may apply for some users/applications.

## Product overview and use cases

- Product family supports diverse applications; vector data is the most feature-rich but larger in size due to per-polygon metadata; 25 m rasters provide detailed land cover without polygon boundaries, suitable for some processing needs; 1 km rasters are convenient for national-scale modelling and integration with other data (e.g., meteorological or species distribution data).
- Example datasets illustrate the level of detail across vector, 25 m raster, and 1 km raster products.
- 1 km rasters offer dominant and percentage cover for 23 classes and aggregates, aiding broad-scale analyses.

## Classification, classes, and mapping

- LCM2007 uses 23 classes aligned with Broad Habitats; some Broad Habitats are divided into sub-classes to capture spectral variations (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and other coastal classes).
- Appendix 1 provides detailed descriptions for each of the 23 LCM2007 classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Saltwater, Freshwater, Urban, Suburban, Supra-littoral Rock, Littoral Rock, Littoral Sediment, Saltmarsh, etc.).
- Appendix 2 documents the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (how 23 classes map to Broad Habitats and FieldCodes).
- Appendix 3 provides standard LCM2007 colour mappings used in the Final Report for display purposes.

## Validation, accuracy, and caveats

- Ground reference validation involved 9,127 polygons; average accuracy around 83%, acknowledging regional and class-based variability.
- Local discrepancies may occur; Broad Habitat sub-classes and FieldCodes are provided for additional detail but require independent validation for sub-class use.
- Some grassland distinctions (e.g., Neutral/Calcareous/Acid Grassland) were challenging when compared with ground-truth data and Countryside Survey maps; users requiring precise sub-class distinctions should consult Morton et al. 2011 for methodological details.
- Montane Habitat mapping is altitude-based; caution is advised when interpreting Montane Habitats relative to vegetation-based Broad Habitat definitions.

## Technical details and limitations

- Data scale and unit
  - Vector: ~10 million polygons; high file sizes; rich metadata per polygon.
  - Raster: 25 m and 1 km resolutions; suitable for different modelling and visualization needs.
- Spatial coverage and projection
  - GB data: British National Grid (OSGB36); NI data: Irish National Grid; NI is transitioning towards ITM for future compatibility.
- Minimum mappable unit and feature dissolution
  - Features smaller than 0.5 ha or linears under 20 m are dissolved, which may affect the visibility of small features.
- Metadata and QA
  - Rich polygon metadata including KBE history, processing lineage, and ProbList; QA focuses on the primary 23 LCM2007 classes rather than Broad Habitat subclasses.

## Data sizing and access details

- Vector (Shapefile, 100 km x 100 km blocks example)
  - GB: ~4.13 GB; NI: ~0.43 GB
- Raster 25 m
  - GB: ~1.36 GB; NI: ~46 MB
- Raster 1 km
  - Range: ~21 MB to ~49 KB depending on product
- Access
  - 1 km rasters via CEH gateway
  - Full vector and 25 m rasters on request; licence may apply

## Colour mapping and presentation

- Appendix 3 provides the colour mapping for 23 LCM2007 classes (for display in maps and reports), detailing specific RGB values per class.

## Acknowledgements and copyright

- Acknowledges data sources from Landsat, SPOT, AWIFS, and Ordnance Survey datasets; CEH and Countryside Survey Partnership contributions.
- Copyright notices apply; CEH manages licensing and dissemination for data products.

## Key references

- Morton et al., 2011. Final Report for LCM2007 – the new UK Land Cover Map.
- Jackson, 2000. Guidance on the interpretation of the Biodiversity Broad Habitat Classification.

- For more information and detailed methodology, consult the Final Report (Morton et al., 2011) and related appendices in the LCM2007 documentation.