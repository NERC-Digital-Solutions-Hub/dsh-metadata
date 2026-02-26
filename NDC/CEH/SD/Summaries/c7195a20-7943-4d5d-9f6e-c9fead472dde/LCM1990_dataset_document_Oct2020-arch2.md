# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map with 21 classes, created from Landsat-5 (30 m) two-date composites and aligned with the LCM2007/LCM2015 framework to enable long-term change analysis.
- Provides a range of data products (vector, 25 m raster, 1 km aggregates) to support diverse user needs and maintain compatibility with other LCM products.

## Key data products

- Vector data set (core product)
  - About 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland
  - Each polygon carries rich attributes, including:
    - Unique geometry identifier (gid)
    - _hist: list of classes present in the polygon with pixel counts
    - _mode: recommended LCM1990 target class (1–21)
    - _purity: percentage of polygon covered by the modal class
    - _conf: per-polygon confidence from Random Forest classifier (0–100)
    - _stdev: standard deviation of the uncertainty
    - _n: number of pixels in the polygon
    - cmp: composite image source
- 25 m raster data set
  - 3-band GeoTIFF: band 1 = dominant class per polygon, band 2 = mean per-polygon confidence, band 3 = percentage of polygon area covered by the modal class
  - country-specific grids (GB and NI) with appropriate projections
- 1 km raster data set
  - Aggregated products derived from the 25 m raster:
    - Dominant cover at 1 km for LCM1990 Target classes (21 bands)
    - Dominant cover at 1 km for LCM1990 Aggregate classes (10 bands)
    - Percentage cover at 1 km for Target classes (21 bands)
    - Percentage cover at 1 km for Aggregate classes (10 bands)
  - Rounding can cause sums to deviate from 100%; coastline areas may sum to less than 100% due to mapping extent
- Data formats and projections
  - 25 m and 1 km rasters distributed as uncompressed GeoTIFFs
  - GB uses British National Grid; NI uses Irish Grid (TM75)
  - SW corner pixel anchoring used for coordinate references

## Class structure and mapping

- LCM1990 maps land cover (not strictly land use) using 21 classes based on UK Biodiversity Action Plan Broad Habitats
- Some classes are subdivided for spectral reasons:
  - Built-up Areas and Gardens -> Suburban, Urban
  - Dwarf Shrub Heath -> Heather, Heather grassland
  - Littoral Sediment Broad Habitat -> Littoral sediment, Saltmarsh
- Minimum mapping unit and dissolution
  - Minimum mappable area > 0.5 ha
  - Polygons smaller than 0.5 ha and line features < 20 m dissolved into surrounding landscape
- GID and metadata
  - Each parcel has a unique gid; retaining this attribute is recommended to preserve unambiguous communication
  - Rich polygon metadata includes dominant class details and per-class pixel breakdowns

## Data quality, uncertainty, and validation

- Uncertainty information
  - Random Forest per-pixel probability is provided as per-polygon mean confidence
- Quality Assurance
  - Defined QA checks for projections, spatial completeness, modal class presence (vector), data range checks (raster), and pixel size accuracy
  - Methodology mirrors those used for LCM2007/LCM2015; field boundary changes have limited impact on accuracy
- Validation and references
  - Full validation performed against external datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately
- DOIs and citation
  - Each LCM1990 product has a DOI for precise, repeatable citation
  - Example GB and NI DOIs provided; citation guidance included (author-year in text with full DOI in references)

## Access, licensing, and citation

- Data access
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector product available on request under licence; licensing fees may apply for some users
- DOIs for citation
  - DOIs exist for GB NI vector and raster products and for 1 km dominant/percentage cover products and aggregates
  - Citations should include authors and year (e.g., Rowland et al., 2020) and full DOI in references
- Contact and further information
  - Spatial data queries: spatialdata@ceh.ac.uk
  - More information: CEH eIP LCM1990 data page
- Projections and data structure
  - GB vector/raster: British National Grid; NI vector/raster: Irish Grid
  - Data provided with detailed metadata and standardized classification mappings to enable cross-product comparability across time

## Use cases and suitability for environmental monitoring

- Consistent, standardised outputs suitable for long-term environmental health assessment, policy performance monitoring, and integration with other environmental datasets
- Data can be stored and uploaded to appropriate data portals, enabling broader data discovery and reuse
- The 25-year change potential (1990–2015) is facilitated by adopting the same framework as subsequent LCM versions, supporting trend analyses and policy evaluation

## Summary of relevance for Analysts Monitoring the Environment

- Delivers standardised, trackable environmental datasets with clear provenance (DOIs, metadata, uncertainty measures)
- Supports reproducible analyses through well-documented methods, consistent class definitions, and open access to data formats
- Facilitates data integration by providing both vector and raster representations and aligning with other LCM products for comparability over time
- Addresses challenges of increasing data value and data accessibility by offering rich metadata, QA, and accessible data distribution pathways