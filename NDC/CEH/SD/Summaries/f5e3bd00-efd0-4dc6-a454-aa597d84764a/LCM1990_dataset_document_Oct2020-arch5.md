# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK-wide land cover map (two-date composite, Landsat-5, 30 m) classified into 21 classes aligned with UK Biodiversity Action Plan Broad Habitats. It replaces LCMGB and uses the LCM2007/LCM2015 spatial framework to enable long-term change analysis and compatibility with other LCM products.
- Data products support diverse user needs with a rich metadata and lineage framework to aid governance, reuse, and interoperability.

## Data products and formats

- Vector data product
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Eight key attributes including: dominant class (mode), per-polygon class history (_hist), uncertainty (_conf, _stdev), pixel counts (_n), and source composite (_cmp).
  - Includes a unique geometry identifier (gid) for unambiguous communication.
- Raster data products
  - 25 m raster derived from the vector data (three bands: dominant class, mean confidence, and percentage coverage of modal class).
  - 1 km raster products: dominant cover (for target and aggregate classes) and percentage cover (21 target bands and 10 aggregate bands).
  - Spatial extents and pixel counts provided (GB and NI separately due to different projections).
- File formats and projections
  - Data distributed as uncompressed GeoTIFF rasters.
  - GB: British National Grid; NI: Irish National Grid.
  - Coordinate details and pixel extents specified in the documentation (Table 4 in the source).
- Access and licensing
  - 25 m and 1 km rasters: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product: available on request from CEH (licensing fees may apply).
- DOIs and citation
  - Each LCM1990 product has a DOI. Examples include vector GB, 25 m GB raster, 1 km target/aggregate classes (and their NI counterparts).
  - Guidance to cite DOIs in publications with authors and year; examples provided in the document.
- Example imagery and product relationships
  - Figure-based descriptions compare vector, 25 m raster, and 1 km products.
  - Relationships between LCM1990 classes, aggregate classes, and Broad Habitats summarized in accompanying tables.

## Classification scheme and semantics

- 21 LCM1990 target classes mapped to Broad Habitats (as per Jackson, 2000), with some classes subdivided for spectral clarity (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Appendix 1 provides class-specific mapping notes and caveats, including typical spectral distinctions and potential misclassifications (e.g., Neutral vs Improved Grassland, Calcareous vs Neutral Grassland).
- Appendix 2 summarizes Broad Habitat definitions (from JNCC) to support interpretation and potential data integration.
- Appendix 3 provides standard LCM1990 colour mapping guidelines for visualization.

## Data quality, uncertainty, and validation

- Rich metadata per polygon: dominant class, pixel contributions per class, and mean classification confidence (per-polygon, from Random Forest).
- Per-pixel probability from the Random Forest classifier included in both vector and 25 m raster data.
- QA and validation
  - Projections and spatial completeness checks.
  - Modal class presence in all polygons (vector products).
  - Consistency of headers and data ranges (0-100 for raster percentages).
  - Pixel size verification for raster products.
  - Full validation performed against external datasets (e.g., Countryside Survey, National Forest Inventory) with results to be reported in a separate publication.
- Minimum mappable area
  - >0.5 ha; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into the surrounding landscape during production.
- Data lineage
  - Built on 2007 OS MasterMap-derived parcel framework, with field boundary changes infrequent to limit impact on accuracy.
- Uncertainty handling
  - Per-polygon confidence and standard deviation accompany classification results to inform user decisions.

## Data access, rights, and use

- Access points
  - 25 m and 1 km rasters: CEH Environmental Information Platform.
  - Vector product: available on request; licensing may apply.
- Licensing and fees
  - Some users/applications may incur licensing fees; see CEH access pages for details.
- Data citation and reuse
  - DOIs facilitate transparent, repeatable methods; include authors and date in citations.
  - Example citation format provided in the documentation.

## Data governance and stewardship considerations

- Documentation and metadata richness supports governance, data discovery, and provenance tracking.
- Versioning
  - Documented version history (Version 1.0 released 02/07/2020; Version 1.1 updated DOIs in Tables 5 and 6 on 08/10/2020).
- Data updates and compatibility
  - Spatial framework harmonization with LCM2007 and LCM2015 to enable 25-year change products and cross-product comparability.
  - Clear guidance on aggregation (21 target classes and 10 aggregate classes) to support various analytical needs and interoperability with broader habitat classifications.
- User guidance
  - Guidance on how to interpret land cover vs land use in LCM1990 contexts; cautions regarding potential misclassification of certain habitat types.
  - Recommendations to retain gid for unambiguous communication and dataset development.

## Support and contact

- Further information and data access details
  - https://eip.ceh.ac.uk/lcm/lcmdata
  - Queries: spatialdata@ceh.ac.uk
- Acknowledgement and funding
  - Supported by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE.