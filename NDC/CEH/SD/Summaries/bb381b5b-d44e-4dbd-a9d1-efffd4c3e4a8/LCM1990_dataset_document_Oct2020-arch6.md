# Dataset documentation

- LCM1990 is a parcel-based UK land cover map with 21 classes, created from Landsat-5 two-date composites at 30 m resolution.
- It uses an updated LCM2007 spatial framework and mirrors methods from LCM2015 to enable long-term land cover change analyses (e.g., 25-year product).

## Data products and structure

- Vector data set
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Key attributes include gid (unique parcel id), hist (class composition within the polygon), mode (recommended dominant LCM1990 class), purity, conf (mean per-polygon classifier confidence), stdev, n (pixel count), and cmp (composite image source).
  - Provides detailed metadata for each polygon.

- Raster data sets
  - 25 m raster: 3-band output per polygon – band 1 is dominant class, band 2 is mean confidence, band 3 is percentage of polygon covered by the dominant class.
  - 1 km rasters: aggregate products (dominant cover per 1 km) and percentage cover per class (21 target classes and 10 aggregate classes). Percentage values are integers and may not sum exactly to 100 due to rounding and coastal edge effects.
  - The 25 m and 1 km rasters are produced for Great Britain and Northern Ireland in separate coordinate systems.

- Data formats and access
  - Core product is the vector dataset; the 25 m raster is derived from the vector; 1 km rasters summarize the 25 m data.
  - Vector and raster products are distributed in GeoTIFF-compatible formats; GB and NI datasets use respective national projections.
  - Access channels include the CEH Environmental Information Platform (eip.ceh.ac.uk) and data-licensing arrangements; full vector product available on request (licensing fees may apply).

## Class structure and interpretation

- 21 LCM1990 target classes align with UK Broad Habitats (JNCC Jackson 2000). Some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- LCM1990 maps land cover (not strictly land use); certain land uses may be ambiguous from spectral data alone (e.g., recreation grass vs. grazed grassland).
- Minimum mappable area is >0.5 ha; polygons smaller than 0.5 ha or linear features shorter than 20 m are dissolved into surrounding landscape.

## Uncertainty and quality

- Uncertainty is quantified via Random Forest per-pixel probabilities, summarized per polygon in the vector (and in the 25 m raster as the mean confidence in band 2).
- A comprehensive QA process checks projections, spatial completeness, modal class presence in polygons, data range (0–100 for raster products), and pixel sizes.
- Validation has been conducted against other datasets (Countryside Survey, National Forest Inventory) with results to be detailed in a separate publication.

## Metadata and citation

- Each LCM1990 product has a Digital Object Identifier (DOI) for citation, enabling transparent methods and reproducibility.
- Guidance provided for including author/date and DOI in references (e.g., Rowland et al., 2020).
- Example DOIs cover: GB vector, GB 25 m raster v2, GB 1 km percentage/dominant/aggregate products, and NI equivalents.

## Projections and data access details

- Projections:
  - Great Britain vector and 25 m/1 km rasters: British National Grid (OSGB 27700).
  - Northern Ireland 25 m/1 km rasters: TM75 Irish Grid (EPSG 29903).
- Data access points:
  - CEH Environmental Information Platform: https://eip.ceh.ac.uk/
  - Full vector product available on request from CEH (licensing may apply).
- Licensing: Some users may incur license fees; consider license terms for redistribution and reuse.

## Documentation and support resources

- Appendix 1: Detailed notes on LCM1990 class interpretations and mapping considerations (e.g., woodland types, grassland confusion, and spectral vs. field distinctions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (context for class mapping).
- Appendix 3: Standard LCM color mapping recipe for visualization.
- Appendix 4: Composite image metadata used during LCM1990 production.
- Map projections, data structure, and accuracy assessments are described to support data integration with other datasets and time-series analyses.

## Data citation and contact

- DOIs provided for GB and NI products across vector, 25 m, 1 km target/dominant/aggregate rasters.
- Data queries and access details: spatialdata@ceh.ac.uk and CEH’s LCM data page: https://eip.ceh.ac.uk/lcm/lcmdata