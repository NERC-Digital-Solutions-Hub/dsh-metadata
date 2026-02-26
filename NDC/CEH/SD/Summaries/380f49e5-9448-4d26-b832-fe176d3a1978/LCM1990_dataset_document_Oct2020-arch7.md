# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map produced by classifying Landsat-5 imagery into 21 classes, based on UK Biodiversity Action Plan Broad Habitats.
- It was designed to be compatible with other LCM products (notably LCM2015) and uses a consistent spatial framework to enable cross-era analysis (e.g., 25-year change products).
- The documentation covers LCM1990 data products and their use, not other Land Cover Maps.

## Data products and formats
- Vector data set (core product): polygons with attached attributes (dominant class, provenance, uncertainty, per-polygon pixel breakdown, etc.). Contains about 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland. Unique geometry ID (gid) is provided for each parcel and should be retained.
- 25m raster: derived from the vector product; 3-band GeoTIFF (band 1 = dominant class per polygon, band 2 = mean per-polygon confidence from Random Forest, band 3 = percentage of polygon area covered by the dominant class). Separate datasets for GB and NI; 8-bit unsigned, British National Grid (GB) or Irish Grid (NI).
- 1km rasters: produced by aggregating 25m rasters to 1km cells. Products include:
  - Dominant cover at 1km for LCM1990 Target classes (1-band)
  - Dominant cover at 1km for LCM1990 Aggregate classes (1-band)
  - Percentage cover at 1km for LCM1990 Target classes (21 bands)
  - Percentage cover at 1km for LCM1990 Aggregate classes (10 bands)
  - Note: percentages are integers; sums may not equal 100 exactly due to rounding and coastal mapping extents.
- Spatial scope: Great Britain and Northern Ireland have separate datasets due to different projections; GB and NI 25m rasters and 1km rasters are provided with appropriate coordinate systems.

## Spatial framework and scope
- The LCM1990 vector and raster data sets are built on a parcel framework, aligned with the 2007 OS MasterMap derivatives, refined with boundary data to maintain compatibility with other geospatial datasets.
- Minimum mapped area is 0.5 hectares; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape during production.
- Overall aim is to enable easy interpretation and cross-dataset compatibility, including potential for long-term change analyses (e.g., 25-year products).

## Classes and mapping
- LCM1990 maps 21 classes based on UK Broad Habitats (JNCC Jackson 2000). Some broad habitats are subdivided for spectral clarity, including:
  - Built-up Areas and Gardens divided into Urban and Suburban
  - Dwarf Shrub Heath divided into Heather and Heather grassland
  - Littoral Sediment divided into Littoral sediment and Saltmarsh (Priority Habitat)
- Appendix 1 provides detailed class interpretations and caveats for spectral vs. land-use distinctions.
- The dataset includes comprehensive metadata for each polygon, including dominant class, pixel counts per class, and classification probabilities.

## Attributes and uncertainty
- Vector attributes (key ones):
  - gid: unique parcel identifier
  - _hist: list of classes present in the polygon with pixel counts
  - _mode: recommended display class (LCM1990 target class)
  - _purity: percent area of polygon covered by the modal class
  - _conf: mean per-polygon classification confidence (0–100)
  - _stdev: standard deviation of the uncertainty
  - _n: number of pixels in the polygon
  - cmp: composite image number used for the classification
- Uncertainty information:
  - Random Forest classifier provides per-pixel probability; reported as mean per-polygon value in the vector and in the 25m raster (band 2).
- QA and validation:
  - Projections checked, spatial completeness verified, modal class present in polygons, metadata headings consistent, raster value ranges (0–100) checked, pixel sizes verified.
  - Full validation against other datasets (e.g., Countryside Survey, National Forest Inventory) is documented and reported separately.

## Data access and citation
- Access:
  - 25m and 1km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product is available on request under licence from CEH (licence fees may apply for some users).
- Citation and DOIs:
  - All LCM1990 products have individual DOIs (GB and NI). The document provides examples of how to cite, e.g., Land Cover Map 1990 (vector, GB), with full DOI references.
  - DOI-bearing products include GB vector, GB 25m raster, GB 1km percentage/dominant target classes, GB 1km aggregate classes, and equivalent NI products.
- Contact:
  - For access details, licensing, and queries: spatialdata@ceh.ac.uk
  - Data page: https://www.ceh.ac.uk/services/land-cover-map-1990
- Projections and coordinate systems:
  - GB data: British National Grid (EPSG 27700)
  - NI data: Irish Grid (TM75, EPSG 29903)

## Projections and coordinate system
- GB data: British National Grid (27700)
- NI data: TM75 Irish Grid (29903)
- Raster and vector products are provided in respective national grid projections to support accurate spatial analyses.

## Quality assurance and validation
- Methods and code-defined processes ensure consistency with product specifications.
- QA checks include projection verification, spatial completeness, polygon modal class validation, heading consistency, value range checks for rasters, and pixel size verification.
- Validation against independent datasets is described and slated for publication as a separate paper.

## Practical considerations for GIS workflows
- Retain gid in vector products to maintain unambiguous communication about parcels.
- Choose between vector detail and raster simplicity:
  - Use vector for rich metadata and precise polygon delineation.
  - Use 25m raster for analyses that benefit from simpler geometry and reduced file size; 1km rasters are suitable for national-scale modeling with other datasets.
- Expect slight mismatches between 1km sums and 100% due to rounding; coastal areas may show underestimation in some classes.
- If integrating with LCM2015 or other UK land cover maps, be aware of the consistent spatial framework and class definitions designed to maximize comparability.

## Additional information and references
- Data access and more details: https://eip.ceh.ac.uk/lcm/lcmdata
- Related literature and background: Jackson 2000; Morton et al. 2011; Rowland et al. 2020 (change products)
- Appendix 3 and Appendix 4 include standard color mapping and composite image details for classification.