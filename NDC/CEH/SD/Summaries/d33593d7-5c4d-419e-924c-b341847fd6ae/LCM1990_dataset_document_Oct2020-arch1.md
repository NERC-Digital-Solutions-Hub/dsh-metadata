# Dataset documentation

## Introduction
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map classified into 21 classes, based on UK Biodiversity Action Plan Broad Habitats.
- Created from two-date Landsat-5 composites (30 m) and aligned with the LCM2007 framework to maximize compatibility with later maps.
- Provides data products to support diverse LCM user needs; this document covers LCM1990 data products only.

## Background
- LCM1990 maps land cover, not strictly land use; some distinctions (e.g., arable crop vs. actual land use) may be ambiguous from remote sensing alone.
- Built to enable a 25-year land cover change product (1990–2015) alongside LCM2015, using a consistent spatial framework derived from Ordnance Survey MasterMap and other base data.
- Data are structured as polygons with real-world boundaries to improve interpretability and compatibility with other datasets.
- A minimum mappable area of >0.5 ha; polygons smaller than 0.5 ha or very short linear features are dissolved into surrounding landscape.

## LCM1990: Data products overview
LCM1990 provides vector and raster data products at multiple resolutions, with extensive metadata and uncertainty information. The products are distributed with DOIs for citation.

### Vector data set
- Great Britain: ~6.7 million polygons; Northern Ireland: ~0.9 million polygons.
- Each polygon carries a rich set of attributes:
  - gid: Unique parcel identifier (geometry id).
  - hist: List of classes present in the polygon with pixel counts.
  - mode: Recommended dominant LCM1990 class (1–21).
  - purity: Percentage of the polygon covered by the modal class.
  - conf: Mean classifier confidence per polygon (0–100).
  - stdev: Standard deviation of the uncertainty.
  - n: Number of pixels in the polygon.
  - cmp: Composite image source used for classification.
- 21 target classes map to Broad Habitat definitions; several classes are subdivided for spectral reasons (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).

### Raster data sets
LCM1990 raster data are derived from the vector dataset to support applications that prefer gridded formats.

#### 25m raster
- 3-band 25 m raster:
  - Band 1: Dominant LCM1990 class per polygon (1–21).
  - Band 2: Mean per-polygon confidence (from Random Forest voting).
  - Band 3: Percentage of the polygon area covered by the modal class.
- Separate rasters for Great Britain and Northern Ireland; coordinates and metadata detailed in the data specification.

#### 1km raster
- Created by aggregating 25m rasters to 1 km squares, providing:
  - Dominant cover at 1 km for LCM1990 Target classes (1-band).
  - Dominant cover at 1 km for LCM1990 Aggregate classes (1-band).
  - Percentage cover at 1 km for Target classes (21 bands).
  - Percentage cover at 1 km for Aggregate classes (10 bands).
- Percentage values are integers; sums may deviate slightly from 100 due to rounding and coastal areas.
- Great Britain and Northern Ireland data are provided separately due to projection differences.

### Class mapping and relationships
- Table 2 in the document defines the mapping between LCM1990 classes, Broad Habitats, and Aggregate/Target classifications used in the raster products.
- Aggregates condense the 21 classes into 10 (GB) or other usable groupings for 1 km products.

## Citing LCM1990 (DOIs)
- Each LCM1990 product (vector, 25 m, 1 km target/aggregate, etc.) has an individual DOI for citation.
- Examples provided for GB and NI products; DOIs enable transparent, repeatable methods and usage tracking.
- When citing, include author/date in-text and full DOI in references.

## Map projection
- GB vector and 25 m rasters: British National Grid (EPSG 27700).
- NI vector and 25 m rasters: Irish National Grid (EPSG 29903 or TM75 Irish Grid for larger-scale products).

## Data access
- 25 m and 1 km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector product: available under licence on request from CEH (spatialdata@ceh.ac.uk); licence fees may apply for some users/applications.

## Quality Assurance
- Data are produced under defined methods with QA checks for projection accuracy, spatial completeness, polygon modal class, value ranges (0–100 for rasters), and pixel size consistency.
- LCM1990 follows the 2007 MasterMap-based parcel framework; field boundary changes are infrequent, limiting impact on overall accuracy.
- A full validation exercise comparing LCM1990 with other datasets (Countryside Survey, National Forest Inventory, etc.) has been conducted; results are reported in a separate publication.

## Further Information
- Additional data and documentation are available at the CEH LCM data portal: https://eip.ceh.ac.uk/lcm/lcmdata
- Queries can be directed to spatialdata@ceh.ac.uk.
- The LCM1990 journal paper is in preparation and will contain further information.

## Acknowledgement
- Supported by the Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.

## References
- Jackson (2000); Morton et al. (2011); Rowland et al. (2020a, 2020b) and related CEH datasets and reports.
- Data citations provided in Tables 5 and 6 of the document for GB and NI products.

## Appendices
- Appendix 1: Comments on LCM1990 class mappings and Broad Habitat interpretations.
- Appendix 2: Biodiversity Action Plan Broad Habitats (JNCC classifications).
- Appendix 3: Standard LCM1990 colour mapping recipe for visual display.
- Appendix 4: Composite images used in LCM1990 production (metadata for image sources and dates).