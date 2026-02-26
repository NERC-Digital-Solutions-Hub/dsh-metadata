# Dataset documentation

- LCM1990 overview
  - UK parcel-based land cover map created from Landsat-5 (30 m) imagery; classifies into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
  - Designed to be compatible with LCM2007/LCM2015 frameworks to enable long-term change products (25 years).
  - Vector and raster data products available (25 m and 1 km resolutions); GB and Northern Ireland data presented separately due to projections.

- Data structure and products
  - Vector data set
    - Polygons with attached attributes; eight key attributes include: dominant land cover class (text and integer), source image, per-polygon uncertainty, pixel counts per class, and proportion of polygon for the dominant class.
    - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 25 m raster
    - 3-band GeoTIFF: band 1 = dominant class per polygon; band 2 = mean per-polygon confidence; band 3 = percentage of polygon area covered by the modal class.
    - Spatial reference and metadata aligned with GB and NI projections; data sizes and layout detailed in Appendix/Table metadata.
  - 1 km raster
    - Summary products derived from 25 m data: 
      - Dominant cover at 1 km for target classes (21-band, one band)
      - Dominant cover at 1 km for aggregate classes (10-band)
      - Percentage cover at 1 km for target classes (21 bands)
      - Percentage cover at 1 km for aggregate classes (10 bands)
    - Percentage values are integers; sums may not equal exactly 100 due to rounding and coastal edge effects.
  - Spatial framework and resolution details
    - Minimum mappable area > 0.5 ha; polygons smaller than 0.5 ha and linear features < 20 m dissolved into surrounding landscape during production.
    - GB and NI data use distinct coordinate systems: British National Grid for GB; Irish Grid (TM75) for NI.
  - Aggregation and class mapping
    - 21 LCM1990 classes correspond to Broad Habitats; some classes further subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
    - Table 2 provides the mapping from LCM1990 target classes to Broad Habitats and 1 km aggregates.

- Class definitions and labeling
  - 21 classes aligned with JNCC Broad Habitat definitions (as described in Appendices 1–2).
  - A unique geometry ID (gid) labels each parcel in the vector product to enable unambiguous cross-user communication.
  - Polygon-level metadata includes dominant class, per-polygon pixel breakdown, and classifier confidence.

- Uncertainty and quality indicators
  - Random Forest per-pixel probability is included as mean per-polygon confidence (for vector and the 25 m raster).
  - QA checks cover projections, spatial completeness, modal class presence in polygons, value ranges (0–100 for rasters), and pixel size accuracy.
  - Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) is noted; results published separately.

- Data access, licensing, and citation
  - Data are available via the CEH Environmental Information Platform (eip.ceh.ac.uk); full vector product available on request (licence may apply).
  - DOIs are assigned to all LCM1990 products (GB and NI; vector and raster variants; 1 km target and aggregate classes). See Tables 5 and 6 for details.
  - Guidance for citation: include author(s) and date in-text with the full DOI in references (e.g., Rowland et al., 2020; DOI provided in Tables 5/6).
  - More information available at CEH pages and data citation guidelines (eidc.ceh.ac.uk).

- Projections and data formats
  - GB vector and raster data use British National Grid (EPSG 27700); NI data use Irish Grid (TM75, EPSG 29903).
  - Data distributed as uncompressed GeoTIFFs; raster bands are described explicitly (dominant class, confidence, and area coverage).
  - Full vector product access is on request; 25 m and 1 km rasters distributed as GeoTIFFs with defined metadata.

- Further information and contact
  - Primary information and data access: https://eip.ceh.ac.uk/lcm/lcmdata
  - Spatial data inquiries: spatialdata@ceh.ac.uk
  - LCM1990 journal paper forthcoming; dataset documentation includes extensive appendices detailing class definitions and colour mappings.

- Acknowledgement and references
  - Funded by Natural Environment Research Council (UK-SCAPE National Capability).
  - References provided for background on Broad Habitat definitions and previous LCM products (LCM2007, LCM2015, etc.).