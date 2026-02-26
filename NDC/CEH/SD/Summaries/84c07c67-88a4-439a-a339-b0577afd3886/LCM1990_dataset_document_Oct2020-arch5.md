# Dataset documentation

## Overview and purpose
- LCM1990 is a UK parcel-based land cover map produced by classifying Landsat-5 data into 21 classes, aligned with the UK Broad Habitat framework.
- It replaces the previous LCMGB and uses the LCM2007 spatial framework for compatibility with LCM2015 and to enable long-term change products.
- The dataset supports a range of applications and aims to provide accessible, well-documented land cover information with rich metadata and uncertainty information.

## Data products and structure
- Core products and data formats:
  - Vector data: polygons with extensive attributes; 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 25m raster: derived from the vector; three bands (dominant class, mean per-polygon confidence, percentage cover of the modal class).
  - 1km rasters: aggregate products derived from 25m data; include dominant cover and percentage cover for both 21 target classes and 10 aggregate classes.
- Data sets by region and resolution:
  - Great Britain and Northern Ireland are provided separately (different projections and coordinate systems).
  - Minimum mapping unit: parcels >0.5 ha; linear features <20 m dissolved into surrounding landscape.
- Class structure:
  - 21 LCM1990 classes mapped to Broad Habitats (with some sub-classes for certain habitats).

## Vector and raster details
- Vector data attributes (key fields):
  - gid: unique parcel identifier
  - hist: list of classes present in the polygon with pixel counts
  - mode: recommended display class (LCM1990 target class 1–21)
  - purity: percentage of the polygon covered by the modal class
  - conf: mean per-polygon confidence from the Random Forest classifier
  - stdev: standard deviation of the uncertainty
  - n: number of pixels in the polygon
  - cmp: composite image index used for classification
- 25m raster product:
  - Band 1: dominant LCM1990 class per polygon
  - Band 2: mean per-polygon confidence
  - Band 3: percentage of the polygon area covered by the dominant class
- 1km raster products:
  - Dominant cover at 1km (21-target and 10-aggregate classes)
  - Percentage cover at 1km for each class (21-target and 10-aggregate)
  - Note: percentage values are integer; sums may not always equal 100 due to rounding and coastal area considerations.
- Spatial framework and comparability:
  - Vector framework based on 2007 Ordnance Survey MasterMap for Great Britain; NI uses TM75 Irish Grid for projection.
  - Compatibility with LCM2015 framework to support 25-year change analyses (Rowland et al. references).

## Classes, metadata, and uncertainties
- 21 LCM1990 classes (with some subdivisions):
  - Examples: Built-up Areas and Gardens (split into Urban and Suburban), Dwarf Shrub Heath (split into Heather and Heather grassland), Littoral Sediment (split into Saltmarsh and Littoral sediment).
- Metadata and uncertainty:
  - Rich polygon metadata including dominant class, per-polygon class breakdown, and mean classification probability (uncertainty).
  - Per-polygon gid retained for unambiguous communication among users.
- DOIs and citation:
  - Each LCM1990 product has a DOI; guidance provided for citing vector, 25m raster, and 1km products (GB and NI) to support reproducibility.

## Data access, licensing, and contact
- Data access:
  - 25m and 1km raster data sets available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH; license fees may apply.
- Licensing and contact:
  - Licence details and access procedures available at ceh.ac.uk data pages; for access inquiries: spatialdata@ceh.ac.uk.
- Citations and references:
  - Example DOI citations provided; see Tables 5 and 6 in the document for the full list of DOIs per product and region.
  - Data citation guidance emphasizes including author and date in-text and full DOI in references.

## Quality assurance and validation
- QA checks implemented to ensure data quality:
  - Projections, spatial completeness, and modal class checks for vector data.
  - Headings consistency and value range checks (0–100 for rasters).
  - Pixel size verification for all rasters.
- Validation:
  - Full validation against independent datasets (e.g., Countryside Survey, National Forest Inventory) is described and results to be published separately.
- Production and provenance:
  - LCM1990 uses a documented parcel framework derived from stable map sources; field boundary changes are infrequent, limiting impact on mapping accuracy.

## Practical notes and usage considerations
- Data structure and size:
  - Large vector dataset with millions of polygons; raster products provide lighter-weight options for some applications.
- Temporal and compatibility context:
  - Designed to enable long-term change analyses (1990–2015 era comparisons) and cross-version compatibility with LCM2007/LCM2015.
- Color mapping and appendices:
  - Appendix 3 provides standard color mappings for visual display of classes.
  - Appendices 1–4 offer detailed mapping notes, composite image information, and supplemental methodological details.

## Appendices and additional information
- Appendix 1: Notes on how LCM1990 classes map to Broad Habitat definitions and classification caveats.
- Appendix 2: Overview of Biodiversity Action Plan Broad Habitats (JNCC Jackson 2000 definitions).
- Appendix 3: Standard color mapping recipes for LCM1990 classes.
- Appendix 4: Composite images used during LCM1990 production.

## Acknowledgements and references
- Acknowledgement of NERC CEH support and project details (UK-SCAPE/National Capability).
- Key references for background, methodology, and related products (e.g., Jackson 2000; Morton et al. 2011; Rowland et al. 2020).