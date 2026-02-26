# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview and aims
- Land Cover Map 2007 (LCM2007) provides a range of map-based data products to describe UK land cover, based on 23 classes derived from Broad Habitats.
- Created from 20–30 m satellite imagery; parcel-based vector polygons refined with OS cartography.
- Maps land cover (not strictly land use) and uses a 0.5 ha minimum mappable unit (parcels smaller than this are dissolved).
- Supersedes LCM2000; intended for GIS use and compatibility with other datasets. Final, detailed methodology and limitations are in Morton et al. (2011).

## Data structure and classes
- 23 LCM2007 classes aligned to UK Broad Habitats; some classes subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Each parcel (polygon) has a unique Parcel_ID and 10 attributes, including BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (display class), KBE history, ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct history.
- Sub-class information (BHSub) is provided mainly for supporting probability data and user validation; broad QA is for the main LCM2007 classes.

## Data formats: Vector and Raster
- Vector Data Set: polygons with attributes; ~8.6 million GB polygons and ~0.9 million NI polygons; 10 attributes per polygon. Rich metadata and provenance (KBE, processing history, spectral classification, etc.).
- Raster Data Sets:
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately; data type Unsigned 8-bit.
  - 1 km raster: derived by summarising 25 m data to provide dominant class, percentage cover for both LCM2007 classes and Aggregate (broad) classes.
- Raster products are designed for broader-scale analyses; vector provides detailed polygon-level information and metadata.

## Spatial extent and resolution
- UK-wide: Great Britain and Northern Ireland treated separately due to different projections.
- Projections: GB vector/raster in British National Grid; NI vector/raster in Irish National Grid (with NI transitioning to ITM over time).

## Validation and quality
- Ground reference validation: 9,127 polygons used to assess thematic accuracy; average accuracy around 83%.
- Local discrepancies may occur; Broad Habitat sub-classes and some field codes are not QA-validated to the same standard as the main LCM2007 classes.
- KBE and ProbList provide additional information but require user validation for subclass-level use.

## Data access and licensing
- 1 km raster data sets accessible via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence from CEH; online application at ceh.ac.uk/data or via spatialdata@ceh.ac.uk.
- License fees may apply depending on user type and application.

## File sizes and data footprint
- Vector (100 km x 100 km shapefile example):
  - GB: ~4.13 GB
  - NI: ~0.43 GB
- Raster 25 m:
  - GB: ~1.36 GB
  - NI: ~46 MB
- 1 km raster products are comparatively small (19 KB to ~49 MB depending on product).

## Use recommendations and cautions
- LCM2007 is complex; consult the Final Report (Morton et al., 2011) for production methodology, metadata, and inherent limitations.
- LCM2017 classes are thematically rich but Broad Habitat sub-classes may not be as robust as main classes; users should validate if using sub-class level data.
- The dataset supports GIS-friendly workflows due to polygonal objects and detailed metadata, but the vector dataset is large and may be unwieldy for some applications; raster products offer lighter-weight alternatives with less attribute information.
- Consider aggregating classes (via the provided Aggregate scheme) for 1 km analyses if needed.

## Appendix highlights

- Appendix 1: LCM2007 Classes
  - Descriptions of each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural grassland, Montane Habitats, Inland Rock, Saltwater, Freshwater, Urban/Suburban, etc.), including key characteristics and mapping constraints.

- Appendix 2: Relationship between Broad Habitats, LCM2007 classes and Broad Habitat sub-classes
  - Mapping between Broad Habitats, LCM2007 class numbers, and sub-classes (FieldCode) to aid interpretation and cross-walking to other classifications.

- Appendix 3: Colour mapping (LCM2007 colour recipe)
  - Standard RGB color mappings for each LCM2007 class and class numbers, used in the Final Report for visualization.

## Further information
- Additional details and validation context: Morton et al. 2011 Final Report for LCM2007.
- Broad Habitat interpretation guidance: Jackson 2000, JNCC Report 307.
- Acknowledgements note data sources (Landsat, SPOT, AWIFS, OS, soils, elevation, etc.) and licensing.