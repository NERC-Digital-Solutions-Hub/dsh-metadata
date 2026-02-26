# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A parcel-based UK land cover classification (LCM2007) using 23 classes aligned to UK Broad Habitats, based on summer–winter satellite imagery at 20–30 m resolution.
- Produces map-like data products (vector and raster) for GIS use; designed to support diverse users (policy, clients, public) with rich metadata and QA.
- Not a land-use map; land cover is mapped, which may not always reveal land use (e.g., arable land vs. grass used for recreation).

## Key Features and Aims for GIS Practitioners

- 23 LCM2007 classes derived from Broad Habitats; some classes have sub-classes (e.g., Built-up Areas subdivided into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Minimum mappable unit is >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding areas.
- Polygon-based vector dataset with rich attributes; designed for clear communication and compatibility with GIS workflows.
- Validation against ground reference data yielded an average accuracy of ~83% across 9127 polygons; local discrepancies may occur.

## Data Products and Structure

- Vector Data Set
  - ~8.6 million polygons for Great Britain; ~0.9 million for Northern Ireland.
  - 10 attributes per polygon, including:
    - Parcel_ID: unique identifier with source image reference.
    - BH: Dominant Broad Habitat (LCM2007 class level).
    - BHSub: Broad Habitat sub-class (detailed FieldCode).
    - FieldCode: short description of Broad Habitat sub-class.
    - INTCODE: integer LCM2007 class number (1–23) recommended for display and QA-validated.
    - KBE: Knowledge-Based Enhancement history (processing history and changes).
    - ProbList: top 5 spectral class probabilities for the polygon.
    - CorePixels / TotPixels: pixel counts used in classification.
    - Construct: polygon construction method (OSMM-based segmentation, etc.).
  - Sub-classes (BHSub) present mainly for information and QA; not all have equal accuracy.
  - Relationships and mappings to Broad Habitats and LCM2007 classes provided in appendices.

- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; derived from the vector dataset.
  - 1 km raster: aggregated products derived from 25 m data:
    - Dominant cover at 1 km for LCM2007 classes.
    - Dominant cover at 1 km for Aggregate classes.
    - Percentage cover at 1 km for LCM2007 classes.
    - Percentage cover at 1 km for Aggregate classes.
  - Separate data sets for Great Britain and Northern Ireland due to different projections.

## Spatial and Thematic Details

- Projections and coordinate systems
  - Great Britain: British National Grid (OSGB 1936) with Transverse Mercator projection.
  - Northern Ireland: Irish National Grid (in NI) with Irish Transverse Mercator as NI migrates to ITM.
- Resolution and data structure
  - 20–30 m pixel imagery underpinning classifications; 25 m raster products are common outputs.
  - 0.5 ha minimum mapping unit leads to dissolution of smaller parcels.
- Data formats and example datasets
  - Vector: detailed polygon features with attached metadata.
  - 25 m raster: same land cover detail without polygon boundaries or extensive metadata (easier processing for some apps).
  - 1 km rasters: UK-wide summaries suitable for large-scale modelling (e.g., meteorology, species distribution).

## Access, Licensing, and Documentation

- Data access
  - 1 km raster datasets available via the CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector product and 25 m raster product available on request under licence from CEH (online application at ceh.ac.uk/data; contact spatialdata@ceh.ac.uk).
  - Licence fees may apply for some users and applications.
- Documentation and sources
  - Final Report for LCM2007 (Morton et al., 2011) provides comprehensive methodology and validation details.
  - Broad Habitat classification guidance and relationships provided in appendices (Appendix 2; Appendix 1 lists the LCM2007 classes).
  - Colour mapping for visualization provided in Appendix 3 (RGB values per class).

## Data Specifications and Size

- Vector data
  - GB: ~4.13 GB (100 km x 100 km shapefile example)
  - NI: ~433 MB
- Raster data (geotiff format)
  - 25 m (GB): ~1.36 GB
  - 25 m (NI): ~46 MB
  - 1 km products: 21 MB to 49 KB depending on product
- Summary: large data volumes; efficient data management and selective use recommended for GIS workflows.

## Practical Considerations for GIS Specialists

- The dataset provides a high thematic resolution (23 classes) with rich attribute data; use vector for detailed analysis and metadata tracking, or raster for scalable, compute-friendly processing.
- Maintain Parcel_ID for unambiguous communication and traceability across projects.
- Be mindful that Broad Habitat sub-classes (BHSub) are supplementary and may require independent validation due to variable accuracy.
- Data reflects land cover, not purely land use; infer usage with caution and validate against local context or additional data.
- For Northern Ireland, be aware of projection and datum differences; plan reprojection as needed to ITM for NI-specific analyses.

## Appendices and Colour Mapping

- Appendix 1: LCM2007 classes with brief descriptions per Broad Habitat.
- Appendix 2: Detailed mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Standard colour mapping (RGB) for visualizing LCM2007 classes.

## Further Information and References

- Morton, D. et al. (2011). Final Report for LCM2007 - the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on Broad Habitat Classification definitions (JNCC Report 307).
- Data and contact: CEH data portals and spatialdata@ceh.ac.uk.