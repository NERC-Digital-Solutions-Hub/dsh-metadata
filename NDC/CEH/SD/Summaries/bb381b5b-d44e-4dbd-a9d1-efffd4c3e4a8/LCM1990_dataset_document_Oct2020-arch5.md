# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map produced from two-date Landsat-5 data (30 m) and classified into 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Designed to be compatible with LCM2007 and LCM2015 frameworks to enable 25-year land cover change analyses.
- Vector and raster data formats, with DOIs assigned for stable, citable references; data are archived and suitable for long-term use.
- Data are governed and distributed by CEH, with access via the CEH Environmental Information Platform; licensing may apply.

## Data products and structure
- Core products:
  - Vector dataset: polygons with rich per-polygon metadata; 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Raster datasets: 25 m raster (GB and NI) and 1 km aggregated products derived from the 25 m data.
- Class structure:
  - 21 LCM1990 target classes mapped to Broad Habitat definitions.
  - Aggregates: 10 broad habitat aggregates used for 1 km products; 21-band and 10-band 1 km percentage/dominant products.
  - Some classes are subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).
- Data relationships:
  - 25 m raster produced from the vector data; 1 km products derived by aggregating 25 m data (dominant cover, percentage cover).
  - 1 km data sums may deviate from 100% due to rounding and coastal areas.
- Key attributes (vector):
  - gid: unique parcel identifier.
  - hist: list of classes present in polygon with pixel counts.
  - mode: recommended LCM1990 target class (1–21).
  - purity: percent coverage of modal class.
  - conf: mean per-polygon classifier confidence (0–100).
  - stdev: uncertainty standard deviation.
  - n: number of pixels in polygon.
  - cmp: composite image number used for classification.
- Output formats and metadata:
  - 25 m raster: three-band GeoTIFF (band 1: dominant class, band 2: mean confidence, band 3: percentage cover).
  - Projections: GB data in British National Grid; NI data in Irish National Grid (TM75) for rasters; vector data aligned accordingly.
  - DOIs provided for all GB and NI products; recommended to cite DOIs in publications.

## Metadata, uncertainty, and quality
- Rich polygon-level metadata enables traceability to processing steps and pixel-level composition.
- Uncertainty is quantified via Random Forest per-pixel probabilities included as mean polygon values (vector and 25 m raster) and in 1 km products.
- Quality assurance:
  - Projections, spatial completeness, modal class existence in polygons, header consistency, value ranges (0–100 for rasters), and pixel size checks.
  - Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately.

## Access, licensing, and citation
- Access:
  - 25 m and 1 km raster data available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request; licenses may apply.
- Citation and DOIs:
  - All LCM1990 products have DOIs for Great Britain and Northern Ireland; use author/date format in text and include full DOI in references.
  - Example citation format provided in the documentation to ensure reproducibility.

## Data governance and stewardship implications
- Data governance:
  - Datasets are archived with DOIs and stable identifiers to support reproducible research and governance needs.
  - Clear licensing and access arrangements help manage proprietary or restricted-use cases.
- Practical guidance for data stewards:
  - Retain gid in vector products to preserve unambiguous communication about parcels.
  - Prefer DOIs for data citation to support tracking of usage and provenance.
  - Be mindful of differences between 25 m and 1 km products, especially rounding effects on 1 km percentage sums.
  - Align use with Broad Habitat definitions and the LCM1990 to LCM2007/LCM2015 framework for consistency in longitudinal analyses.

## Appendix and additional information (highlights)
- Appendix 1–4 provide detailed class definitions, colour mappings, and composite image metadata; Appendix 2 covers Broad Habitat definitions aligned with JNCC classifications.
- The dataset supports 25-year land cover change analyses and cross-compatibility with newer LCM products to facilitate longitudinal studies.

## Access and contact
- Data access inquiries (full vector product, licensing) and further information:
  - CEH Environmental Information Platform: https://eip.ceh.ac.uk/
  - Spatialdata for LCM1990: spatialdata@ceh.ac.uk
  - CEH LCM1990 information: https://www.ceh.ac.uk/services/land-cover-map-1990
  - Land Cover Map 1990 data page: https://eip.ceh.ac.uk/lcm/lcmdata

## References
- Jackson, 2000; Morton et al., 2011; Rowland et al., 2020 (GB and NI) and related DOIs for primary products.