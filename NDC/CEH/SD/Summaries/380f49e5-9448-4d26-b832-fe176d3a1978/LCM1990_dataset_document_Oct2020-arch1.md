# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created from Landsat-5 two-date composites at 30m resolution, classified into 21 Broad Habitat-based classes.  
- Purpose: provide a stable, archived data set with rich metadata to support diverse land cover analyses and to enable future compatibility with LCM2007/LCM2015 and long-term change products.

## Background and context

- Classes align with UK Biodiversity Action Plan Broad Habitats (JNCC Jackson 2000).  
- Built to reflect real-world boundaries using an updated LCM2007 spatial framework, enabling compatibility for 25-year change products (with LCM2015 as reference).  
- Spatial framework derived from generalised cartography (OS MasterMap GB, LPS Northern Ireland) and refined with rural boundary data.  
- Minimum mappable unit: polygons >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved into surrounding landscape.  
- Data structure supports both vector (polygons with rich attributes) and raster formats (25m and 1km products).

## Data products and structure

- Core products: LCM1990 vector (parcels) and derived 25m raster; also 1km dominant and percentage cover products (for both 21 target classes and 10 aggregate classes).  
- Vector data: polygons with eight key attributes, including dominant class, per-polygon pixel counts for all classes, uncertainty metrics, and a unique geometry identifier (gid).  
- Uncertainty: per-pixel probability from Random Forest classifier included as mean per-polygon value in both vector and 25m raster.  
- Raster data: available as 25m 3-band raster (band 1 = dominant class per polygon; band 2 = mean polygon confidence; band 3 = percent polygon covered by modal class) and 1km aggregated products derived from 25m data.

## Vector data set details

- Great Britain: ~6.7 million polygons; Northern Ireland: ~0.9 million polygons.  
- Attributes include: land cover class (text and integer), source image, uncertainty information, pixel counts per class, and dominant-class proportion (_mode).  
- GID (Geometry ID) retained to ensure unambiguous communication of parcel data.

## Raster data sets

- 25m raster: 3-band GeoTIFF (GB and NI separate projections: GB uses British National Grid; NI uses TM75 Irish Grid). Band 1 ties to LCM1990 class numbers; Band 2 provides per-polygon RF confidence; Band 3 provides polygon modal class coverage percentage.  
- 1km raster: formed by summarising 25m rasters to give dominant class (1-band) and percentage cover (21-band and 10-band sets). Note: percentage totals may sum to slightly more or less than 100 due to rounding and coastal edge effects.

## Data formats, projections, and access

- File formats: uncompressed GeoTIFFs for raster products; vector data available under license on request from CEH.  
- Coordinate systems: GB = British National Grid; NI = TM75 Irish Grid.  
- Data access: CEH Environmental Information Platform (eip.ceh.ac.uk) for 25m/1km rasters; full vector product available on request (licensing fees may apply).  
- Documentation and DOIs: each LCM1990 product has a Digital Object Identifier (DOI) for precise citation (GB and NI tables provided). Examples include DOIs for GB vector, GB 25m raster, GB 1km percentage/dominant target and aggregate classes, and NI counterparts.

## Quality assurance and validation

- QA checks cover projection correctness, spatial completeness, modal class presence in polygons, data headings, value ranges (0–100 for 1km rasters), and pixel size conformity.  
- Validation activities compare LCM1990 against other datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.  
- The dataset is designed as a stable, archived product with extensive metadata to support reproducibility.

## Access, citations, and references

- All LCM1990 products are citable via DOIs; publications should cite author(s) and date (e.g., Rowland et al., 2020) and include the full DOI in references.  
- Example citation guidance provided for GB and NI products, with detailed tables listing each DOI.  
- Acknowledgement: CEH acknowledges NERC support (National Capability under UK-SCAPE).  
- Further information and contact: CEH Environmental Information Platform and spatialdata@ceh.ac.uk.

## Appendices and additional information

- Appendix 1: Class interpretations and mapping notes for LCM1990 Broad Habitat classes (e.g., Broadleaved Woodland, Coniferous Woodland, Arable and Horticulture, various Grasslands, Wetlands, Built-up Areas, Coastal and Littoral classes).  
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (high-level descriptions for each class).  
- Appendix 3: Standard LCM color-mapping recipes for class visualization.  
- Appendix 4: Composite images used during LCM1990 production (metadata for image pairs and dates).  

## Documentation and sources

- Cited references for methodology and background (e.g., Jackson 2000; Morton et al. 2011; Rowland et al. 2020a, 2020b).  
- Data access and contact details summarized for researchers needing the vector product or DOIs.