# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map produced from two-date Landsat-5 imagery (30 m resolution) classifying into 21 broad habitats.
- Built to support a range of LCM applications and to align with later products (LCM2007/LCM2015) for long-term change analysis.
- Vector and raster data products are provided, with metadata-rich attributes and uncertainty estimates to aid data governance and quality assessment.

## Data products and structure

- Vector data set
  - ~6.7 million parcels for Great Britain and ~0.9 million for Northern Ireland.
  - Key attributes per parcel: gid (unique parcel identifier), hist (list of classes within the polygon with pixel counts), mode (dominant LCM1990 class, 1–21), purity, conf (mean per-polygon classifier confidence, 0–100), stdev (uncertainty), n (number of pixels in polygon), cmp (composite image used).
  - Purpose: detailed, attribution-rich representation of land cover with per-polygon uncertainty and composition data.

- Raster data sets
  - 25 m raster: 3-band GeoTIFF
    - Band 1: dominant LCM1990 class per polygon
    - Band 2: mean per-polygon confidence (classifier votes)
    - Band 3: percentage of polygon area covered by the modal class
  - 1 km raster: aggregate products
    - Dominant cover at 1 km for LCM1990 Target classes (1 band)
    - Dominant cover at 1 km for LCM1990 Aggregate classes (1 band)
    - Percentage cover at 1 km for LCM1990 Target classes (21 bands)
    - Percentage cover at 1 km for LCM1990 Aggregate classes (10 bands)
  - Spatial context: separate datasets for Great Britain and Northern Ireland due to differing projections.
  - Note: 1 km products are derived by aggregating the 25 m raster data.

- Class structure and aggregation
  - LCM1990 uses 21 target classes linked to UK Broad Habitats; a core set of 10 aggregate classes used for 1 km products.
  - Some broad habitats are further divided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).

## Data access, formats, and citation

- Access
  - 25 m and 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence from CEH (licence fees may apply for some users/applications).

- Data formats and projections
  - Vector: polygon features with rich attributes (including hist and conf) in a vector dataset.
  - Rasters: uncompressed GeoTIFFs.
  - Projections:
    - Great Britain: British National Grid (OSGB 27700)
    - Northern Ireland: Irish Grid (TM75)
  - Minimum mapping unit and DM considerations
    - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and linear features < 20 m are dissolved into surrounding landscape.

- Citing the data (DOIs)
  - Each LCM1990 product has an individual DOI (GB vector, GB 25 m raster, GB 1 km target/dominant/aggregate products, NI equivalents).
  - Example citation formats provided (Rowland et al., 2020; DOIs given for each product).

## Quality assurance, validation, and limitations

- Quality assurance
  - Defined QA checks for projections, spatial completeness, modal class presence (vector), metadata consistency, value ranges (raster 0–100), and pixel size correctness.
  - Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) with results pending publication.

- Uncertainty and accuracy
  - Per-polygon uncertainty captured as mean classifier confidence and standard deviation; per-pixel probability output from the Random Forest classifier used in the polygon-level attribution.
  - Landsat-based spectral interpretation means some habitat classes can be spectrally similar and misclassified; complementarities with ancillary data can improve accuracy.

- Interpretive guidance
  - LCM1990 maps land cover (not always directly translatable to land use).
  - Some grassland classes can be spectrally similar (e.g., Neutral vs Improved Grassland); users may aggregate classes if appropriate.

- Classification framework and compatibility
  - Spatial framework and class definitions aligned with LCM2015 methods to support cross-temporal analyses (e.g., 25-year UK land cover change products).

## Governance, stewardship, and maintenance

- Versioning and updates
  - Version 1.1 (updates include DOI updates in Tables 5 & 6; published 8 October 2020).
  - Vector products archived with DOIs to support reproducibility and traceability.

- Metadata richness
  - Rich metadata for each polygon, including dominant class, per-class pixel breakdown, and classification probability per polygon.
  - Detailed documentation and mapping appendices to aid interpretation (Appendix 1–4 and Appendix 2 on Broad Habitats).

- Access and contact
  - CEH Environmental Information Platform for raster data; spatialdata@ceh.ac.uk for queries.
  - Further information and dataset documentation available on CEH’s LCM1990 pages and data citation resources.

## Practical considerations for Data Leaders

- Holistic data system view
  - LCM1990 provides both detailed (vector) and scalable (raster) representations, enabling analyses at parcel, landscape, and national scales.
- User needs and co-ownership
  - Rich metadata and uncertainty metrics support collaborative data product development and transparent data stewardship.
- Discoverability and interoperability
  - DOIs, well-defined projections, and explicit 1 km aggregation facilitate reproducibility and integration with other UK land cover and environmental datasets.
- Data gaps and barriers
  - Access to full vector products may require licensing; some data (e.g., coastal and marine-adjacent areas) may be influenced by cartographic framework and MMU constraints.
- Standards and metadata discipline
  - Strong emphasis on metadata, documentation, and standardized color mapping (Appendix 3) to ensure consistent interpretation across teams and external partners.