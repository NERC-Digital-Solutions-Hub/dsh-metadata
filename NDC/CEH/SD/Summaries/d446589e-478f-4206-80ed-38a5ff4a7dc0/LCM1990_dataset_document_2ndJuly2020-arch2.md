# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created from Landsat-5 imagery (30 m) classified into 21 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Built to be compatible with the LCM2015 framework to enable 25-year land cover change analysis (Rowland et al., 2020a; 2020b).
- The dataset is a stable, archived product with Digital Object Identifiers (DOIs) for citation.
- LCM1990 maps land cover (not strictly land use) and uses a polygon-based (vector) framework with accompanying 25 m raster and 1 km products.
- Minimum mappable area is >0.5 ha; parcels <0.5 ha and linear features <20 m are dissolved into surrounding landscape.

## Data products and formats
- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Eight key attributes per polygon, including dominant class, source image, uncertainty, pixel counts per class, and modal class proportion.
  - Unique geometry identifier (gid) retained for unambiguous communication.
- Raster data sets
  - 25 m raster derived from the vector data (three bands: dominant class, mean per-polygon confidence, and percent area of modal class).
  - 1 km raster products created by aggregating 25 m data to provide dominant and percentage cover for both target (21) and aggregate (10) classes.
  - Separate data sets for Great Britain and Northern Ireland due to different projections.
- Classes and aggregation
  - 21 LCM1990 target classes based on Broad Habitats; some Broad Habitats are split into sub-classes (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
  - 1 km products include both target (21) and aggregate (10) classifications; percentage cover products are integer-valued.
- Metadata and uncertainty
  - Rich polygon metadata; per-polygon breakdown of class pixels and mean classification probability.
  - Uncertainty information from Random Forest classifier; per-polygon mean probability included in vector and 25 m raster (Band 2).

## Data access and licensing
- Access via the CEH Environmental Information Platform (EIP): https://eip.ceh.ac.uk/
- 25 m raster and 1 km raster products: available via EIP.
- Full vector product: available on request under licence from CEH (licence fees may apply).
- Data are provided in multiple formats (GeoTiff rasters; vector with detailed attributes) and coordinate systems:
  - GB: British National Grid (EPSG 27700)
  - NI: Irish Grid (TM75) (EPSG 29903)

## Citing and DOIs
- All LCM1990 products have individual DOIs; DOIs should be cited to ensure reproducibility.
- Example citations provided for GB and NI products (vectors and rasters) with full references in accompanying documentation.
- Guidance: include author(s) and date in text and the full DOI citation in references (e.g., Rowland et al., 2020).

## Quality assurance and validation
- UK CEH Land Cover Maps produced with defined methods and QA checks:
  - Projections correctness and spatial completeness.
  - Modal class presence in all polygons (vector) and value ranges (0–100 for raster products).
  - Verification against alternative datasets (e.g., Countryside Survey, National Forest Inventory) and a core validation point set.
- A full validation exercise has been conducted; results to be published separately.

## Methods and compatibility
- Produced using methods aligned with LCM2015 to maximise cross-product compatibility.
- Data are designed to support comparison over time and integration with other geospatial datasets.
- LCM1990 maps land cover, not land use; some land-use inferences may be limited (e.g., recreation grass vs. grazed grass).

## Use considerations and practical tips
- The gid attribute should be retained for traceability and communication between users.
- When using 1 km products, note that percentage sums may not add exactly to 100 due to rounding and coastal edge effects.
- The 25 m raster’s Band 2 (confidence) and Band 3 (percent cover) enable assessment of classification certainty and spatial extent of each class within a polygon.
- For applications needing detailed boundary information, use the vector data; for wide-area modelling, the 1 km rasters are typically preferred.

## Additional information
- Further information and data access: https://eip.ceh.ac.uk/lcm/lcmdata
- Contact: spatialdata@ceh.ac.uk
- Related literature and background: Jackson (2000); Morton et al. (2011); Rowland et al. (2020a, 2020b)
- Acknowledgement: NERC UK-SCAPE programme and CEH support.