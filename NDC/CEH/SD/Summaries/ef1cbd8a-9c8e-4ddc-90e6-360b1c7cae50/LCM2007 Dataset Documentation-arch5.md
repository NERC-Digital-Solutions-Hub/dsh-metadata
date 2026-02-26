# Land Cover Map 2007 Dataset Documentation

## Overview

- UK-wide parcel-based land cover dataset using 23 classes aligned with UK Broad Habitats.
- Provides multiple data products (vector and raster) at different thematic/spatial resolutions to support diverse applications.
- Emphasizes metadata richness, provenance, processing history, and quality assurance to aid governance and reuse.
- Data derived from satellite imagery (20–30 m pixels) and integrated with generalised OS mapping frameworks for improved GIS compatibility.

## Data Content and Structure

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Unique Parcel_ID per polygon; supports communication via a stable identifier.
  - Broad Habitat (BH) and Broad Habitat sub-class (BHSub) are included; FieldCode provides training/validation detail but is not QA-validated.
  - KBE (Knowledge-Based Enhancement) histories documented; ProbList lists top 5 spectral class candidates.
  - Designed for high thematic resolution (23 classes) with some subdivisions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).

- Raster Data Sets
  - 25 m and 1 km products derived from the vector data.
  - Separate data sets for Great Britain and Northern Ireland due to different projections.
  - 1 km rasters provide dominant class and percentage cover for 23 LCM2007 classes and corresponding aggregates.

- Data Products and Access
  - 1 km raster data sets accessible via the CEH Information Gateway.
  - Full vector product and 25 m raster product available under licence on request from CEH.
  - Licensing fees may apply; contact details provided for access.

## Classes and Classification

- LCM2007 uses 23 classes based on Broad Habitats; some classes have sub-classes (Appendix 1 and Appendix 2 describe relationships and mappings).
- In some Broad Habitats, sub-classes offer additional detail but may have lower accuracy or consistency than the primary LCM2007 class.
- The colour mapping (Appendix 3) provides a standard palette for display purposes in QA and visualization.

## Methodology and Quality

- Production method combines satellite imagery with segmentation informed by OS MasterMap and other cartographic data to create polygons representing real-world objects.
- Land cover (not land use) mapping; minimum mappable unit > 0.5 ha; parcels smaller than 0.5 ha are dissolved into surrounding areas.
- Validation: ground reference data used to compare LCM2007 against spatially and thematically matched polygons (9127 polygons), achieving an average accuracy of 83%.
- Accuracy varies locally; users should perform their own validation for sub-classes and for analyses requiring high certainty.
- Knowledge-Based Enhancements (KBE) applied to refine classifications (e.g., soil corrections, altitude adjustments, urban masks).

## Data Details and Documentation

- Appendix 1: LCM2007 Classes – brief descriptions and field interpretations for each class (e.g., Broadleaved woodland, Arable and Horticulture, Improved Grassland, Semi-natural Grassland, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping table and field codes to LCM2007 classes).
- Appendix 3: Colour mapping recipe used in the Final Report (Morton et al., 2011) for standard visualization of classes.
- Data provenance highlights include Landsat-TM5, SPOT, IRS-LISS3 imagery, and various cartographic sources; acknowledgments to contributing data producers and licensees.

## Spatial and File Size Details

- Vector data (shapefile, 100 km x 100 km blocks):
  - GB: ~4.13 GB; NI: ~433 MB.
- Raster data (geotiff):
  - 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km products: 21 MB to 49 KB (depending on product type).
- Projections:
  - Great Britain: British National Grid (OSGB36).
  - Northern Ireland: Irish National Grid (Ireland 1965; moving to ITM in NI).
- Data volumes are large; storage planning should account for both vector and raster formats and the associated metadata.

## Access, Licensing, and Use Guidance

- Data access pathways:
  - 1 km raster data: CEH Information Gateway.
  - Full vector and 25 m raster data: available under licence on request from CEH.
- Licensing considerations may apply to certain users and applications; licensing contacts provided.
- Users are advised to consult the Final Report for full methodological detail and limitations (Morton et al., 2011) to ensure appropriate use and interpretation.
- Suitable governance and stewardship practices include maintaining Parcel_ID, metadata, and provenance to facilitate traceability, reproducibility, and data sharing.

## Practical Considerations for Data Stewards

- High governance value:
  - Rich metadata and processing history enable reproducibility and auditability.
  - Clear data provenance and labeling (Parcel_ID) support unambiguous data communication.
- Update and interoperability:
  - Multiple data products support different workflows; plan for updates and versioning.
  - Vector and raster products offer trade-offs between detail (vector) and processing efficiency (raster).
- Access and licensing management:
  - Centralize licensing information; track user permissions and usage rights.
  - Ensure alignment with OS, CEH, and partner data licenses and acknowledge data sources as required.
- Validation and risk management:
  - Encourage users to validate Broad Habitat subclasses and sub-class interpretations for their specific analyses.
  - Document limitations related to MMU, spectral similarity among classes, and changes over time due to land cover dynamics.

## Further Information

- Morton, D. et al. (2011). Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- For a detailed description of Broad Habitat classifications and class relationships, refer to Appendices and the Final Report.