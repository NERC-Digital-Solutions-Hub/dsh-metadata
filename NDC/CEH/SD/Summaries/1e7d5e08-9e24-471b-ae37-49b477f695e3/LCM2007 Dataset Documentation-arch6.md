# Land Cover Map 2007 Dataset Documentation

- UK parcel-based land cover classification using 23 Broad Habitat-based classes, derived from 20–30 m satellite imagery.
- Builds on LCM2000 with improved spatial framework (OSMM/large-scale vector data) and segmentation for object-based mapping.
- Maps land cover (not land use) with a minimum mappable unit of 0.5 ha; small parcels (<0.5 ha) dissolved into surrounding landscape.

## Data and Product Overview

- Data formats and resolutions:
  - Vector data set: polygons with 10 attributes, 8.6 million polygons GB, 0.9 million polygons NI.
  - Raster data sets: 25 m and 1 km products for GB and NI (separate projections).
- Data products are designed to support diverse applications; final report Morton et al. 2011 provides comprehensive methodology.
- Vector product attributes (Table 1 highlights):
  - Parcel_ID: unique polygon identifier including source image.
  - BH: Broad Habitat (dominant class at Broad Habitat level).
  - BHSub: Broad Habitat sub-class (descriptive FieldCode).
  - INTCODE: 1–23 LCM2007 class number (recommended display class; QA-validated).
  - KBE: Knowledge-Based Enhancements applied to the polygon.
  - ProbList: top 5 spectral-class probabilities for the polygon.
  - CorePixels/TotPixels: pixel counts for classification.
  - Construct: data-source and segmentation history (OSMM-based, segmentation variants).
  - Additional fields: FieldCode, Description, etc.
- Raster products:
  - 25 m: full 23-class raster grid.
  - 1 km: aggregates for UK-scale analyses (dominant class, percentage cover for both 23 classes and Aggregate classes).
- Class structure:
  - 23 LCM2007 classes anchored to UK Broad Habitats (with some subdivisions, e.g., Urban vs Suburban, Heather vs Heather grassland, Littoral/Saline splits).
  - Appendices detail relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides standard colour mapping.

## Class Taxonomy and Interpretation

- Broad Habitats cover major UK land cover types (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved/Uneven Grassland, Semi-natural Grassland, Montane Habitats, Inland Rock, Saltwater, Freshwater, Littoral and Coastal, Built-up Areas and Gardens, etc.).
- Some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Important notes:
  - LCM2007 maps land cover (spectral/reflectance-based) rather than precise land use; interpretation should consider context (e.g., arable land vs. actual use).
  - Broad Habitat subclasses (BHSub) provide additional information but are not as rigorously QA-validated as the main LCM2007 classes; users should validate at subclass level if used.
  - Ground-truth validation shows average accuracy ~83% across 9,127 polygons; local discrepancies may occur.
  - Certain classes (e.g., Fen/Marsh/Swamp, Bog, Montane habitats) can be spectrally challenging; cross-check with metadata and Final Report if used for fine-grained analyses.

## Data Access and Licensing

- 1 km raster data (dominant/percentage cover) available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under license from CEH (licence fees may apply).
- File size guidance:
  - Vector (GB 100 km × 100 km shapefile): ~4.13 GB; NI shapefile ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB–49 KB (varies by product).
- Projections:
  - GB: British National Grid (OSGB 1936).
  - NI: Irish National Grid (moving toward Ireland Transverse Mercator, ITM).
- Data access contact: spatialdata@ceh.ac.uk; CEH data portal at www.ceh.ac.uk/data.

## Metadata, Validation, and Quality

- Rich metadata per vector polygon, including processing history (KBE), original imagery, and spectral class likelihood.
- QA and validation:
  - Class-level QA with a 9127-polygon ground reference dataset; overall average accuracy ~83%.
  - Sub-class level metadata (BHSub and FieldCode) recommended to be used with caution unless validated by users.
- Practical guidance:
  - Retain Parcel_ID attribute for unambiguous communication and provenance.
  - Use the INTCODE for display and QA-supported classification; cross-reference with Table 2/Appendix for crosswalks if needed.
  - For analysis requiring detailed spectral class information, consult ProbList and perform user validation on sub-classes.

## Usage Guidance and Recommendations

- Suitable for a wide range of GIS applications requiring 23-class land cover detail at ~20–30 m resolution; can be aggregated to 1 km for UK-scale modelling.
- Vector data provides rich attribute metadata per polygon but larger file sizes; 25 m raster offers a lighter-weight alternative with less metadata.
- Because LCM2007 is a complex product, recommended practice includes:
  - Familiarising with production methodology, metadata, and limitations as described in the Final Report (Morton et al., 2011).
  - Consulting Appendix 1–3 for class definitions, crosswalks to Broad Habitats, and standard colour mappings.
  - Cross-validating Broad Habitat subclasses if used for specific ecological or management decisions.
- Acknowledgements reflect diverse data sources (Landsat, SPOT, AWIFS, OS MasterMap, etc.), and usage should respect licensing terms.

## Appendices and Supporting Information

- Appendix 1: Detailed LCM2007 class descriptions and notes on each Broad Habitat type.
- Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
- Appendix 3: Standard LCM2007 colour mapping (class number to RGB values).
- References:
  - Morton et al. 2011: Final Report for LCM2007 – the new UK Land Cover Map.
  - Jackson 2000: Guidance on Broad Habitat classification definitions.

## Acknowledgements

- Data sources include Landsat-TM5, SPOT, AWIFS, cartographic data from Ordnance Survey and others; CEH collaboration with Countryside Survey Partnership.