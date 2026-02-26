# Land Cover Map 2007 Dataset Documentation

- A structured collection of UK land cover data products (LCM2007) to support diverse data exploration and insight generation.
- Produces parcel-based land cover classifications using 23 Broad Habitat-based classes from 20–30 m imagery.
- Available in vector and raster formats, with detailed metadata and multiple product levels to suit different applications.
- Emphasizes careful use: consult the Final Report for comprehensive methodologies and limitations; LCM2007 data are distinct from LCM2000/1990 products.

## Introduction and Background

- LCM2007 maps land cover (not land use) across Great Britain and Northern Ireland using 23 classes derived from Broad Habitats.
- Built from summer–winter composite imagery at 20–30 m resolution; improves on LCM2000 via a more spatially precise framework (OSMM-based) and segmentation.
- Minimum mapping unit: parcels >0.5 ha; smaller features dissolved into surrounding landscape.
- Classes sometimes subdivided into sub-classes (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Validation: ground reference data against 9,127 polygons yielded an average accuracy of 83%, with expected local variation.

## LCM2007 Product Overview

- Provides a range of data formats and thematic/spatial resolutions to meet various needs.
- Vector data: polygons with rich attribute information per parcel.
- Raster data: 25 m and 1 km products derived from the vector data; allow different scales and applications.
- 25 m and 1 km products exist separately for GB and NI, accommodating different projections and sampling grids.
- Classes are aligned to Broad Habitats (per Jackson 2000) with some scale-based subdivisions to improve spectral separability.

## Example Data Sets

- Vector data: 8.6 million polygons for GB and 0.9 million for NI.
- 25 m raster: full 23-class raster derived from vector data, with detailed polygon-related metadata not present in raster form.
- 1 km raster: aggregated products (dominant class, percentage cover) for UK-wide modeling and broader analyses.
- Trade-offs:
  - Vector: rich metadata, larger files, more complex processing.
  - 25 m raster: similar detail without polygon boundaries or metadata overhead.
  - 1 km raster: suitable for national-scale modeling and integration with other datasets (e.g., meteorology, species distributions).

## Vector Data Set

- Each parcel (polygon) carries 10 attributes (Table 1):
  - Parcel_ID: unique identifier (includes source image, e.g., 11853977:c20).
  - BH: Broad Habitat (dominant class at Broad Habitat level).
  - BHSub: Broad Habitat sub-class (text description from FieldCode).
  - FieldCode: short code for sub-class details; not QA-validated for standalone use.
  - INTCODE: integer LCM2007 class (1–23) recommended for display; QA-validated.
  - KBE: Knowledge-based enhancements history (processing trace).
  - ProbList: top five spectral-class probabilities (spectral variants).
  - CorePixels: number of core pixels used for maximum likelihood classification.
  - Construct: data-source/origin and segmentation history (OSMM, OSMM:SEG, OSMM:AGC:SEG).
  - TotPixels: total pixels in the polygon.
- Special notes:
  - BHSub provides extra detail but may be less reliable; users should validate if using sub-classes.
  - ProbList provides the likelihoods of spectral matches; use as guidance rather than definitive classification.
  - Parcel_ID enables unambiguous cross-referencing between users.

## Raster Data Sets

- 25 m rasters: 23 LCM2007 classes; GB and NI provided separately with different projections.
- 1 km rasters: derived by summarizing 25 m data to compute dominant and percentage cover per 1 km pixel; offers both 1 km dominant and 1 km percentage products for classes and aggregates.
- Metadata and layout:
  - GB 25 m: 28,000 columns × 52,000 rows; NI 25 m: 7,800 × 6,200 (examples from Table 3).
  - 1 km GB: 700 × 1,300; NI: 200 × 1,300 (examples from Table 3).
  - Pixel size: 25 m (25 m rasters) or 1000 m (1 km rasters).
  - Data types: unsigned 8-bit.
  - Projections: GB in British National Grid; NI in Irish National Grid (with NI transitioning to ITM in progress).
- Applications:
  - 25 m rasters align with detailed land-cover mapping.
  - 1 km rasters facilitate national-scale analyses and integration with other large-scale datasets.

## Map Projection and Data Access

- Map projections:
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (Ireland 1965), with a plan to migrate NI data to ITM.
- Data access:
  - 1 km raster data: CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector product and 25 m raster product: available on request under licence from CEH; application via CEH data portal or via spatialdata@ceh.ac.uk.
- Licensing and cost:
  - Some users/applications may incur licence fees; access may require contractual arrangements.

## Data Quality, Use and Documentation

- Rich metadata available for vector polygons, including source images, processing steps, KBE history, and ProbList.
- Validation: average 83% accuracy against ground reference polygons; individual accuracy may vary locally.
- Important cautions:
  - LCM2007 maps land cover, not necessarily land use; interpretation of sub-classes requires validation.
  - Broad Habitat sub-classes (BHSub) are included mainly for interpretative and probability context; use with validation if employing at sub-class level.
  - Some grassland classifications (Neutral/Calcareous) can be mis-classified as Improved Grassland; consult Morton et al. 2011 for detailed guidance.
- Documentation and references:
  - Final Report for LCM2007 (Morton et al., 2011) for method, QA, and limitations.
  - Broad Habitat guidance (Jackson, 2000) for understanding class definitions and relationships.
- MMU and data processing:
  - MMU of 0.5 ha ensures relatively robust mapping; smaller features are generalized.
  - Detailed rules for class splits (e.g., Heather vs Heather grassland) reflect spectral and habitat considerations.

## Appendices

- Appendix 1: LCM2007 Classes – detailed brief reviews of each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various grassland types, Fen/Marsh/Swamp, Bog, Montane, Inland Rock, Saltwater, Freshwater, Urban/Suburban, Littoral and coastal classes, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (maps table linking Broad Habitat groupings to LCM2007 class numbers and sub-classes).
- Appendix 3: LCM2007 colour mapping recipe – standard color assignments for each LCM2007 class (for visualization in GIS).
- Acknowledgements: data sources and partners; notes on imagery and cartographic data used; copyright and licensing statements.

## Further Information

- Morton et al. (2011) Final Report for LCM2007 – the comprehensive reference for methodology, QA, and limitations.
- Jackson (2000) Guidance on Broad Habitat Classification – definitions and relationships to other classifications.
- Countryside Survey network and CEH data portals for access and additional documentation.