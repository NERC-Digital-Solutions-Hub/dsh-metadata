# Dataset documentation

## Overview
- Landsat-5 based UK Land Cover Map 1990 (LCM1990) is a parcel-based land cover map created by classifying satellite imagery into 21 land cover classes, aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Built to be compatible with LCM2007/LCM2015 frameworks to enable 25-year land cover change analysis.
- Vector product (parcels with detailed attributes) and raster products (25m, 1km) support diverse data applications.

## Data products and structure
- Core products:
  - Vector dataset of polygons (GB and Northern Ireland) with rich attributes.
  - 25m raster derived from the vector data.
  - 1km raster products: dominant cover (target and aggregate classes) and percentage cover (21 target, 10 aggregate classes).
- Spatial details:
  - GB vector: ~6.7 million polygons; NI vector: ~0.9 million polygons.
  - 25m raster: 25 m pixels; 1 km rasters summarize 25m data to provide broader-scale coverage.
- Data formats:
  - Vector: polygon features with attributes (including dominant class, uncertainty, and per-polygon pixel breakdown).
  - 25m raster: 3-band GeoTIFF (band1 dominant class, band2 mean confidence, band3 percent cover).
  - 1km rasters: percentile/percentage cover and dominant class data (aggregated from 25m data).
- Spatial framework and targets:
  - British National Grid for Great Britain; Irish Grid for Northern Ireland.
  - Minimum mappable area > 0.5 ha; features smaller than this are dissolved into surrounding landscape.

## Class structure and mapping
- LCM1990 uses 21 target classes based on Broad Habitats; several classes are split for detail:
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather grassland.
  - Littoral Sediment split into Littoral sediment and Saltmarsh (Priority Habitat).
- Appendix-style guidance links LCM1990 classes to JNCC Broad Habitat definitions to aid interpretation and cross-walks with other datasets.
- The vector attribute _hist provides a list of classes present within a polygon with pixel counts, enabling exploration of mixed-class areas.

## Metadata, uncertainty, and quality
- Rich per-polygon metadata:
  - gid: unique parcel identifier.
  - _hist: list of classes and pixel counts within the polygon.
  - _mode: recommended display class (1–21).
  - _purity: percentage of polygon covered by the modal class.
  - _conf: mean per-polygon confidence from the Random Forest classifier (0–100).
  - _stdev: standard deviation of the uncertainty.
  - _n: number of pixels in the polygon.
  - cmp: composite image source indicator.
- Uncertainty information:
  - Random Forest per-pixel probability is included as mean per-polygon confidence and in the 25m raster band 2.
- DOIs:
  - Each LCM1990 product has its own DOI to facilitate citation and reproducibility (separate DOIs for GB vector, GB 25m raster, GB 1km target/aggregate, NI equivalents). See Tables 5 and 6 in the document for details.
- Documentation and references:
  - DOI citation guidance and examples provided; full DOI citations included in references section.
  - Provisions for colour mapping and standard classifications provided in Appendix 3.

## Access, licensing, and citation
- Data access:
  - 25m and 1km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH (licence may apply).
- Licensing:
  - Some users may incur licence fees; Dundation details available via CEH data access pages.
- Citation guidance:
  - Use the dataset DOIs with author/date; example format provided (e.g., Rowland et al., 2020).
  - Include full DOI citation in references; see “Citing LCM1990 (DOIs)” section for example references and URLs.

## Technical specifications and data access details
- Projections:
  - Great Britain: British National Grid; Northern Ireland: Irish Grid (TM75).
- Data extents and grid characteristics (selected):
  - Great Britain 25m and 1km rasters have defined grid dimensions and extents; NI rasters have corresponding dimensions with Irish Grid coordinates.
- Data access points:
  - CEH Environmental Information Platform for 25m/1km rasters.
  - CEH spatialdata contact for the vector product and access details.
- Versioning:
  - Dataset documentation Version 1.1 (updated 8/10/2020) with DOI updates in Tables 5 & 6.

## Quality assurance and validation
- QA checks include:
  - Correct projections and spatial completeness.
  - Polygons containing a modal class (vector products).
  - Consistency of headings with dataset documentation.
  - Value ranges 0–100 for raster percentage products.
  - Correct pixel sizes for raster products.
- Validation:
  - Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results prepared for a separate publication.

## Usage notes and considerations
- Data interpretation:
  - LCM1990 maps land cover (not always directly equal to land use); some land-use inferences may be ambiguous from remote sensing alone.
- Data granularity:
  - Vector provides detailed metadata but larger file sizes and processing overhead; 25m raster offers a balance between detail and performance; 1km rasters are suitable for national-scale modelling with other data (e.g., meteorology, species distributions).
- Class aggregation:
  - Aggregated classes for 1km rasters help when full 21-class resolution is unnecessary; some users may aggregate grassland classes due to spectral similarities noted in the documentation.

## Practical notes for data support
- When addressing “the ask,” consider whether a distribution of land cover across the UK (1km rasters) or detailed polygon-level classifications (vector) better meets needs.
- For reproducibility and transparency, cite the appropriate DOI for the chosen data product and reference the accompanying documentation and validation materials.
- Leverage _hist and _conf attributes in the vector to assess mixed-class areas and per-polygon classification confidence.
- Consult Appendix materials for class definitions and mapping nuances to ensure correct interpretation in analyses and dashboards.

## Contact and additional information
- Access and further information:
  - CEH Environmental Information Platform: https://eip.ceh.ac.uk/
  - LCM1990 data information page: https://www.ceh.ac.uk/services/land-cover-map-1990 or contact spatialdata@ceh.ac.uk
- Acknowledgement:
  - Supported by NERC award NE/R016429/1 (UK-SCAPE programme, National Capability).