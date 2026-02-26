# Dataset documentation

- LCM1990 is a parcel-based UK land cover map derived from Landsat-5 imagery (30m resolution) classified into 21 Broad Habitat-based classes. It supports consistent cross-product compatibility with LCM2015 and LCM2007, enabling long-term land cover change analyses (up to 25-year products).
- The dataset is distributed as both vector and raster formats (25m and 1km products), with a focus on rich metadata, per-polygon uncertainty, and explicit class definitions to aid interpretation and reuse.

## Data products and formats

- Vector data set
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland
  - Key attributes: unique geometry identifier (gid), history of class composition (_hist), recommended display class (_mode), polygon purity (_purity), per-polygon classifier confidence (_conf), standard deviation of uncertainty (_stdev), number of pixels in polygon (_n), and data source/composite information (cmp).
- Raster data sets
  - 25m raster: 3-band GeoTIFF (dominant class, per-polygon confidence, polygon area coverage)
  - 1km raster: aggregate and percentage-cover products (dominant and percentage cover for 21 target classes and 10 aggregate classes)
  - GB and NI data provided separately due to different projections
- DOIs and citation
  - All LCM1990 products have DOIs for reproducibility and proper citation (separate DOIs for GB vector, GB 25m raster, GB 1km products, NI vector, NI 25m raster, NI 1km products)

## Data access and licensing

- Access via CEH Environmental Information Platform (eip.ceh.ac.uk)
- Full vector product available on request under licence from CEH; licence fees may apply
- Data documentation and access guidance available at CEH LCM1990 pages
- Licencing considerations accompany potential paywalls/fees for some users

## Spatial framework and compatibility

- GB vector data in British National Grid; NI data in Irish National Grid (TM75 Irish Grid)
- Designed to be directly comparable with LCM2015 and aligned with the LCM2007 framework to enable future multi-time-scale analyses
- Minimum mappable unit: parcels >0.5 ha; features <0.5 ha or lines <20 m dissolved to surrounding landscape

## Data quality, provenance and uncertainty

- Rich metadata for each polygon, including dominant class, pixel-level breakdown, and mean classification probability
- Random Forest classifier provides per-pixel probability, reported as per-polygon mean uncertainty
- Underwent QA checks for projections, completeness, modal class presence, value ranges (0–100 for raster products), and pixel size accuracy
- Validation conducted against external datasets (e.g., Countryside Survey, National Forest Inventory); results documented in a separate publication
- UK CEH Land Cover Maps are produced by trained staff using defined methods and code

## Classification scheme and interpretation

- LCM1990 maps land cover (not strictly land use); some classes may correspond to multiple land-use types and require ancillary interpretation
- 21 target LCM1990 classes mapped from 21 Broad Habitats (JNCC definitions), with some classes subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland)
- Appendix 1 provides detailed mapping notes, training considerations, and common spectral/interpretation caveats for each Broad Habitat
- Appendix 2 summarizes JNCC Broad Habitat definitions used to anchor the LCM classes
- Appendix 3 provides a standard colour-mapping recipe for visualization of LCM1990 classes
- Appendix 4 lists composite images used during the data creation process

## Practical considerations for data leaders

- Discoverability and governance
  - DOIs enable transparent citation and reproducibility; maintain links to both GB and NI products
  - Rich vector metadata supports advanced data discovery and lineage tracking
- Data integration and use
  - Vector product supports detailed attribution per polygon; raster products enable scalable UK-wide analyses and modelling
  - 1km rasters are suitable for large-scale modelling with other environmental datasets
  - Spatial framework compatibility facilitates longitudinal studies (1990–2015 and beyond)
- Access and licensing guardrails
  - Be aware of potential licence fees for the vector product; confirm terms for your institution and use case
  - Use CEH portal for access details and licensing information
- Data quality and transparency
  - Leverage per-polygon uncertainty and histogram (_hist) to assess reliability within analyses
  - Refer to the separate validation publication for methodological context and accuracy benchmarks
- Operational takeaways
  - Use DOIs in publications to ensure reproducibility
  - Retain gid in vector data to preserve unambiguous communication of parcels
  - Consider both 25m detail and 1km summary products depending on reporting granularity and modelling needs

## Projections, coverage, and technical details

- Map projections and coordinate references
  - GB data: British National Grid; NI data: Irish National Grid
- Data extent and structure
  - Core vector product supplemented by 25m and 1km raster products
  - 25m raster provides per-polygon mean confidence and modal class coverage
  - 1km rasters provide dominant and percentage cover across all classes and aggregates
- Metadata and metadata-driven practices
  - Comprehensive polygon attributes, including pixel counts and class proportions, support robust metadata-driven workflows
  - Documentation emphasizes data origin, processing steps, and classification decisions

## How to cite and where to find more information

- Citing pattern example: (Rowland et al., 2020) with full DOI references in the data citation section
- DOIs provided for:
  - GB vector, GB 25m raster, GB 1km percentage and dominant classes (target and aggregate)
  - NI vector, NI 25m raster, NI 1km percentage and dominant classes (target and aggregate)
- Access and help
  - For access specifics and licensing, contact spatialdata@ceh.ac.uk and consult https://eip.ceh.ac.uk/lcm/lcmdata
  - Data portals and user guidance: CEH Environmental Information Platform and CEH LCM1990 pages