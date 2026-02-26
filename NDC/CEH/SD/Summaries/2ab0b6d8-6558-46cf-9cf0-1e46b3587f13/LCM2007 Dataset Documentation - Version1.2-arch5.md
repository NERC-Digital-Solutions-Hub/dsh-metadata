# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK-wide Land Cover Map 2007 (LCM2007) provides a range of data products to support diverse user needs, building on the Final Report by Morton et al. (2011).
- Distinguishes land cover (not land use) using 23 Broad Habitat-based classes derived from satellite imagery (20–30 m) and enhanced with high-quality cartography.
- Available in vector (polygons with rich metadata) and raster formats (25 m and 1 km), for Great Britain and Northern Ireland (separate datasets).

## Data Content and Structure
- Classification and classes
  - Parcel-based classification using 23 classes aligned to UK Broad Habitats; some Broad Habitats are split into sub-classes (e.g., Built-up Areas, Dwarf Shrub Heath, Littoral Sediment).
  - Classes are validated at the 23-class thematic level; Broad Habitat sub-classes receive supplementary information but may require user validation.
- Data formats and products
  - Vector: polygons with 10 attributes each (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels). Contains ~8.6M polygons GB and ~0.9M NI.
  - Raster: 25 m and 1 km products derived from the vector data; 1 km products include Dominant and Percentage cover for both 23 classes and Aggregate classes.
- Attributes and data provenance
  - Parcel_ID uniquely identifies each polygon and links to source imagery.
  - KBE (Knowledge-Based Enhancements) record processing history; ProbList lists top spectral class candidates.
  - INTCODE is the display-ready class (1–23) used in standard tools (.lyr file available).
- Spatial specifics
  - Vector and 25 m rasters for GB and NI; projections are GB National Grid (OSGB) and Irish National Grid, respectively; NI moving toward ITM (GIS tools should reproject if needed).
  - Minimum mappable unit is >0.5 ha; parcels <0.5 ha or lines <20 m were dissolved during production.

## Data Quality, Validation, and Limitations
- Validation
  - Ground-reference validation against polygons shows an average accuracy of 83% at the thematic level (23 classes), acknowledging possible local discrepancies.
- Change mapping
  - Not well suited for change detection due to class and spatial structure differences across LCM1990/2000/2007 and typical spectral classification errors (~20%).
- Metadata and interpretation
  - Rich metadata per polygon; caution advised when using Broad Habitat sub-classes since QA-level validation primarily covers LCM2007 classes.
  - LCM maps land cover, not land use; cautious interpretation when inferring use (e.g., arable crops vs. grazing land).
- Grassland classifications
  - Noted misclassifications between Neutral/Calcareous Grassland and Improved Grassland; guidance to aggregate classes as needed for certain analyses.

## Licensing, Access, and Distribution
- Access
  - 1 km raster products available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under license from CEH (licensing fees may apply).
- Documentation and references
  - Final Report: Morton et al., 2011.
  - Broad Habitat classification guidance: Jackson, 2000.
- Updates and provenance
  - Appendix 4 lists product updates (Version 1.2, May 2014): includes new OS tiles (Fair Isle, Stranraer), addition of water class in 1 km dominant/aggregate products.

## Spatial Coverage and Projections
- Geographic scope: Great Britain and Northern Ireland; GB and NI datasets are provided separately with corresponding projections.
- Map projections
  - GB: British National Grid (OSGB36)
  - NI: Irish National Grid (and transitioning to ITM for NI)
- Data scales and resolutions
  - 23-class vector; 25 m raster; 1 km raster (aggregate and target/dominant class products)

## Practical Guidance for Data Stewards
- Data governance and stewardship
  - Maintain Parcel_ID for unambiguous data lineage and traceability across datasets and updates.
  - Use the vector’s rich metadata for data provenance, processing history (KBE), and QA decisions; leverage ProbList for spectral class validation guidance.
- Product selection and usage
  - Choose data products to balance detail versus manageability (vector for detailed analysis with metadata; 25 m raster for boundary-aligned analyses; 1 km rasters for national-scale modeling).
  - Be mindful of the 0.5 ha MMU and potential misclassifications in grassland and sub-classes; consider aggregation when appropriate.
- Data quality management
  - Validate Broad Habitat sub-classes if they are critical to your analysis; rely on 23-class QA for core results.
  - Recognize change-detection limitations; integrate ground-truth or supplementary datasets when evaluating temporal dynamics.
- Licensing and access planning
  - Plan for licensing fees and access lead times for full vector and 25 m raster products; utilize 1 km rasters via CEH gateway for faster access.
- Documentation and governance workflows
  - Reference Morton et al. (2011) and Jackson (2000) for methodological and classification rationale.
  - Track updates (Appendix 4) to maintain alignment with latest product versions and tile coverage.

## Appendices and Supporting Information Highlights
- Appendix 1: LCM2007 class definitions and broad habitat descriptions (with caveats and interpretation notes).
- Appendix 2: Mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode guidance).
- Appendix 3: Color mapping for LCM2007 classes (including an ArcGIS .lyr file).
- Appendix 4: List of product updates (Version 1.2, 2014) including new tiles and added water class.

## Version History and Acknowledgements
- Version history: 1.0 (July 2011); 1.2 (May 2012/May 2014 updates).
- Acknowledgements: data sources from Landsat, SPOT, AWIFS, Ordnance Survey, and other datasets; CEH and Countryside Survey partnership.