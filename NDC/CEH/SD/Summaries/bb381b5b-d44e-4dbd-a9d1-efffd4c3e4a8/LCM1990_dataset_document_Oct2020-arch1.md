# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created by classifying Landsat-5 satellite imagery (30 m resolution) into 21 classes.
- Based on UK Biodiversity Action Plan Broad Habitat definitions; aims to be compatible with LCM2007 and LCM2015 to enable long-term change analyses.
- Delivered as multiple data products: vector and raster formats, with both GB and Northern Ireland coverage.
- Includes rich metadata, per-polygon uncertainty measures, and a robust quality assurance process.

## Data products and formats
- Vector data set
  - Polygons with attached atributos: dominant class, source image, per-polygon pixel breakdown, uncertainty metrics, and a unique geometry identifier (gid).
  - Coverage: ~6.7 million polygons for Great Britain and ~0.9 million for Northern Ireland.
- 25 m raster
  - 3-band GeoTIFF: band 1 = dominant LCM1990 class per polygon, band 2 = mean per-polygon confidence (Random Forest), band 3 = percentage of polygon area covered by the modal class.
  - Used to derive 1 km products.
- 1 km raster
  - Dominant cover products for both target (21) and aggregate (10) classes (1 band each).
  - Percentage cover products for both target (21 bands) and aggregate (10 bands) classes (1 km resolution; values are integers and may not sum exactly to 100 due to rounding and coastal areas).
  - Note: 1 km data are calculated from the 25 m raster data.
- Class relationship
  - Aggregate classes: 10; Target classes: 21; mappings described in accompanying tables to relate LCM1990 classes to Broad Habitats and higher-level aggregates.
- Spatial framework and comparability
  - Spatial framework aligned with LCM2015 methods to enable cross-version comparability and 25-year change analyses (1990–2015 context).

## Class details and mapping
- LCM1990 maps 21 classes based on Broad Habitats; some broad habitats are further subdivided by spectral signatures (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories subdivided into Saltmarsh vs. Littoral Sediment, etc.).
- Appendix notes provide detailed rationale for class definitions, field-site considerations, and potential misclassifications (e.g., grassland confusion between Improved, Neutral, and Calcareous Grasslands).

## Metadata and uncertainty
- Each polygon includes:
  - Dominant class and a breakdown of pixel counts per class within the polygon.
  - Per-polygon confidence (based on Random Forest voting) and standard deviation of uncertainty.
  - The histogram of class votes (_hist) and the recommended display class (_mode).
- Uncertainty information is available in both vector attributes and the 25 m raster's band 2.

## Data access and licensing
- Access via the CEH Environmental Information Platform (EIP): https://eip.ceh.ac.uk/
- The full vector product is available on request under licence from CEH; some applications may incur licence fees.
- Contact: spatialdata@ceh.ac.uk for access details and licensing.

## Map projections and coordinate systems
- Great Britain: British National Grid (EPSG 27700).
- Northern Ireland: Irish Grid (EPSG 29903).
- All products are provided in their respective national grid projections; 25 m and 1 km rasters are distributed as uncompressed GeoTIFFs.

## Quality assurance and validation
- QA checks ensure correct projections, spatial completeness, modal class presence in polygons, data headings, value ranges (0–100 for rasters), and pixel sizes.
- A full validation exercise compared LCM1990 with other datasets (e.g., Countryside Survey, National Forest Inventory) and is described in a separate publication.

## Citing LCM1990 (DOIs)
- All LCM1990 products have individual DOIs to facilitate reproducible citation.
- Examples include:
  - GB vector (vector, GB)
  - GB 25 m raster (GB 25m raster)
  - GB 1 km percentage cover target classes (GB 1km % target)
  - GB 1 km dominant cover target classes (GB 1km dom. target)
  - GB 1 km percentage cover aggregate classes (GB 1km % aggregate)
  - GB 1 km dominant cover aggregate classes (GB 1km dom. aggregate)
  - NI vector, NI 25 m raster, NI 1 km target/aggregate products
- Use the provided DOIs in citations, e.g., “Rowland et al., 2020” with the full DOI in references.

## Appendix context (highlights)
- Appendix 1: Guidance on how LCM1990 maps Broad Habitat classes, including caveats about spectral interpretation and field verification needs.
- Appendix 2: Summaries of Broad Habitat definitions used for classification (JNCC Jackson definitions).
- Appendix 3: Standard LCM color-mapping recipes for class visualization.
- Appendix 4: Composite images metadata used during LCM1990 creation.

## Contact and further information
- Data access and licensing details: spatialdata@ceh.ac.uk; https://www.ceh.ac.uk/services/land-cover-map-1990
- Additional information and data discovery: https://eip.ceh.ac.uk/lcm/lcmdata
- Acknowledgement: Supported by NERC award NE/R016429/1 as part of the UK-SCAPE programme.