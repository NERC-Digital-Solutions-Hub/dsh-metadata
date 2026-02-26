# Land Cover Map 2007 (LCM2007)

- Overview
  - LCM2007 is available in multiple formats to suit different user needs, with UK coverage.
  - Formats include vector data (detailed) and raster data (simplified for broad use).
  - Vector data uses ESRI Shapefile format; raster data is provided as GeoTiff.
  - Raster products include one 25 x 25 m per-pixel classification (most likely Broad Habitat) and four freely available 1 x 1 km rasters that summarize the 25 x 25 m data.
  - Detailed metadata and specific attribute/class information are described in the Land Cover Map 2007 Dataset Documentation.

- Data formats and scales
  - Vector data
    - Most detailed product: each polygon represents a land cover parcel with attributes and metadata on derivation.
    - Minimum mappable unit: 0.5 hectares.
    - Supply format: ESRI Shapefile.
  - Raster data
    - Five raster products in total.
    - 25 m x 25 m raster: per-pixel Broad Habitat classification.
    - Four 1 km x 1 km rasters: summarize the 25 m x 25 m data.
    - Supply format: GeoTiff.
    - Coverage: UK.

- Documentation and metadata
  - Comprehensive metadata is available in the Land Cover Map 2007 Dataset Documentation.
  - Tables in the documentation include:
    - Table 1: Description of the attributes of the LCM2007 vector dataset.
    - Table 2: Habitats, LCM2007 classes, and Broad Habitat sub-classes.
    - Table 3: Metadata information for the LCM2007 raster datasets.

- Access and governance implications for data leaders
  - Raster products are freely available; vector data is provided in Shapefile format, enabling broad reuse and integration.
  - The availability of both high-granularity (0.5 ha vector) and aggregated (1 km raster) formats supports flexible data strategy and cross-domain usage.
  - Rich metadata and explicit attribute/class tables facilitate data suitability assessments, quality checks, and integration with other datasets.
  - Documentation supports discoverability and standardization efforts across teams and potentially across networks.

- Practical considerations for use
  - Choose format based on required resolution and analysis needs:
    - High-detail analyses may use vector data (0.5 ha minimum mapping unit).
    - Broad-scale analyses may use the 25 m x 25 m raster or the 1 km rasters for efficiency.
  - Ensure alignment with existing GIS workflows by using the provided Shapefile and GeoTiff formats.
  - Leverage the classification and metadata tables to understand habitat classes and data lineage.

- Next steps for data leaders
  - Refer to the Land Cover Map 2007 Dataset Documentation for detailed attribute, class, and metadata information.
  - Assess how the two data representations (vector vs. raster) fit current data architecture and stakeholder needs.
  - Plan integration with other datasets and establish governance around data discovery, quality, and updates based on the documentation.