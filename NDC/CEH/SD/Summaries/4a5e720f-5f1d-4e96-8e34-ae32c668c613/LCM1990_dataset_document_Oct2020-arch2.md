# Dataset documentation

- Overview
  - Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map that classifies satellite imagery into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
  - Built from two-date Landsat-5 composites (30 m) and aligned with the LCM2007/2015 spatial framework to enable long-term change analysis (25-year perspective).
  - Produces both vector (polygons with rich metadata) and raster products suitable for diverse environmental monitoring and policy evaluation.

- Data products and structure
  - Vector data set
    - Polygons with attached attributes; each parcel has a unique geometry identifier (gid).
    - Eight key attributes (including dominant class, source image, uncertainty, per-polygon pixel counts, and confidence).
    - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Raster data sets
    - 25 m raster (three bands: dominant class per polygon, mean per-polygon confidence, and percentage of polygon covered by the modal class).
    - 1 km raster products: dominant cover (target and aggregate classes) and percentage cover (21 target bands and 10 aggregate bands).
    - Separate datasets for Great Britain (GB) and Northern Ireland (NI); coordinate systems align to GB National Grid and Irish Grid respectively.
  - Class structure
    - 21 target LCM1990 classes, based on Broad Habitats; several groups have sub-classes (e.g., Built-up Areas subdivided into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral and Supralittoral divisions).
    - LCM1990 maps land cover (not always equivalent to land use), with caveats (e.g., arable vs. use in recreation areas).
  - Data formats and resolution
    - 25 m and 1 km rasters; vector polygons with detailed metadata; DOIs provided for citation.
    - Minimum mapping unit is >0.5 ha; polygons smaller than 0.5 ha or linear features under 20 m are dissolved into surrounding landscape.

- Data access and citation
  - Access
    - 25 m and 1 km rasters: CEH Environmental Information Platform (eip.ceh.ac.uk).
    - Full vector product available on request under license from CEH (fees may apply).
  - Citation and DOIs
    - Each LCM1990 product has a DOI (GB vector, GB 25 m, GB 1 km target and aggregate classes, NI vector, NI rasters, etc.).
    - Publications should cite the authors, date, and DOI (e.g., Rowland et al., 2020) and list the full DOI in references.
  - Data projections
    - GB vector/raster: British National Grid (EPSG 27700); NI vector/raster: Irish Grid (EPSG 29903).

- Quality assurance and validation
  - QA checks ensure correct projections, spatial completeness, presence of a modal class in polygons (vector), consistency of headings, and value ranges (0–100 for rasters).
  - The dataset uses a robust parcel framework based on 2007 Ordnance Survey MasterMap data; field boundary changes are limited.
  - A full validation exercise compared LCM1990 to datasets like Countryside Survey and National Forest Inventory; results form a separate publication.

- Usage notes and considerations
  - The vector product includes a gid for unambiguous communication; retaining gid is recommended for developments.
  - Per-polygon uncertainty is provided via Random Forest-based probability (mean per polygon) and is also reflected in the 25 m raster.
  - 1 km products may not sum exactly to 100 due to rounding; coastal areas may have mapping extent nuances.
  - The dataset provides both detailed (vector) and processing-friendly (raster) formats to support modeling, monitoring, and integration with other data (e.g., meteorological, species distribution).

- Appendices and related information
  - Appendix 1: Class mapping notes and cautions for certain Broad Habitats (e.g., woodland, grasslands, bog/sedge, marine/coastal habitats) and guidance on aggregation.
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (detailed descriptions of each of the 21 Broad Habitats).
  - Appendix 3: Standard LCM colour mapping recipe for class visualization.
  - Appendix 4: Composite images used in LCM1990 data production (metadata on image paths, rows, dates).
  - Acknowledgements and references to supporting reports and related LCM documentation.

- Further information
  - Additional details and access information available at CEH CEH eIP pages; spatialdata@ceh.ac.uk for queries.
  - LCM1990 journal paper in preparation; related datasets include LCM change products (1990–2015) for GB and NI.