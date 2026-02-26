# Dataset documentation

- This document describes Land Cover Map 1990 (LCM1990) data products for the UK, including vector (parcel-based) and raster formats derived from Landsat-5 imagery (30 m resolution).
- LCM1990 maps land cover using 21 Broad Habitat-based classes; it uses an updated spatial framework for compatibility with LCM2015 and to enable long-term change analyses (1990–2015).

## Overview and purpose

- Parcel-based land cover map for the UK, produced by classifying satellite data into 21 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Based on two-date composite imagery; vector polygons reflect real-world boundaries; designed for easy interpretation and compatibility with other geospatial data.
- Includes a stable, archived dataset with rich metadata, uncertainty information, and per-polygon classification details.
- Aims to support diverse mapping needs and enable cross-product comparability with LCM2007 and LCM2015.

## Data structure and products

- Vector data set
  - Polygons with attributes: unique gid, _hist (list of classes with pixel counts), _mode (LCM1990 target class), _purity (percentage of polygon for modal class), _conf (mean per-polygon RF vote confidence 0–100), _stdev (uncertainty), _n (number of pixels), cmp (composite image identifier).
  - Great Britain: ~6.7 million polygons; Northern Ireland: ~0.9 million polygons.
- Raster data sets
  - 25 m raster: 3-band GeoTiff (band 1 = dominant class per polygon; band 2 = mean per-polygon confidence; band 3 = percent of polygon covered by modal class).
  - 1 km raster: derived from the 25 m raster; multiple products available:
    - Dominant cover at 1 km for 21 target classes (1-band).
    - Dominant cover at 1 km for 10 aggregate classes (1-band).
    - Percentage cover at 1 km for 21 target classes (21 bands).
    - Percentage cover at 1 km for 10 aggregate classes (10 bands).
  - Notes: rounding in 1 km percentage products may cause sums to differ from 100; coastal pixels may sum to less than 100 due to mapping extent and MMU considerations.
- Spatial framework and projections
  - Great Britain: British National Grid (BNG, EPSG 27700).
  - Northern Ireland: Irish Grid (TM75 Irish Grid, EPSG 29903).
  - 25 m and 1 km rasters are provided separately for GB and NI due to projection differences.
- Minimum mapping unit
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and linear features < 20 m are dissolved into the surrounding landscape.

## Classes and mapping details

- 21 LCM1990 classes (based on Broad Habitat definitions). Some classes are subdivided for spectral clarity:
  - Built-up Areas and Gardens -> Suburban and Urban.
  - Dwarf Shrub Heath -> Heather and Heather grassland.
  - Littoral Sediment -> Littoral sediment and Saltmarsh (Saltmarsh is a Priority Habitat).
- Classes reflect land cover rather than strictly land use; some land uses (e.g., recreation grass) may resemble other classes spectrally.
- Appendix 2 provides Biodiversity Action Plan Broad Habitat definitions; Appendix 1 contains mapping notes and caveats for individual habitats (e.g., woodland structure, grassland distinctions, water bodies).

## Data access, licensing, and citation

- Access
  - 25 m and 1 km rasters: available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product: available on request under licence from CEH; licence fees may apply for some users.
- Citation and DOIs
  - All LCM1990 products have individual DOIs (GB and NI). See Tables 5 (GB) and 6 (NI) for details.
  - When citing, include authors and year in-text and full DOI in references (example provided in the document).
- Further information and contact
  - Data hub: https://eip.ceh.ac.uk/lcm/lcmdata
  - Spatialdata inquiries: spatialdata@ceh.ac.uk

## Quality assurance and validation

- QA processes verify projections, spatial completeness, polygon modal class presence (vector), metadata alignment, and value ranges (0–100 for 1 km rasters).
- The LCM1990 parcel framework is built on 2007 Ordnance Survey MasterMap data; field boundary changes are infrequent.
- A full validation exercise has been conducted to compare maps against other datasets (e.g., Countryside Survey, National Forest Inventory); results will be published separately.

## Technical details and specifications

- Data formats
  - Vector: polygon features with comprehensive per-polygon attributes.
  - Raster: 25 m and 1 km products; GB and NI provided separately with appropriate coordinate systems.
- Metadata and documentation
  - Rich polygon metadata, including dominant class details and per-pixel classification probabilities.
  - Tables and appendices provide class mappings, color-coding recipes, and composite image information.
- Citing and DOIs
  - DOIs cover vector, 25 m raster, 1 km dominant/percentage cover products, and aggregate classes for GB and NI (Tables 5 and 6).

## Usage notes and caveats for GIS applications

- The 25 m vector and raster products offer detailed spatial information; 1 km products are suitable for UK-scale modelling with other data (e.g., meteorology, species distributions).
- The 0.5 ha MMU and dissolution of small features mean very small patches may be generalized in the final products.
- The dataset is designed for cross-compatibility with LCM2007 and LCM2015 via the shared spatial framework, enabling long-term land cover change analyses (1990–2015).

## Appendices and additional references

- Appendix 1: Class mapping notes and habitat-specific caveats (e.g., woodland types, grassland classification nuances).
- Appendix 2: Summaries of JNCC Broad Habitat definitions used for LCM1990 classes.
- Appendix 3: Standard LCM color mapping recipe for class visualization.
- Appendix 4: Details of composite images used in LCM1990 production.
- Acknowledgement and references to related LCM documentation and validation work.