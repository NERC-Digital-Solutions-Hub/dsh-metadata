# Dataset documentation

- Overview of LCM1990: a UK parcel-based land cover dataset produced from Landsat-5 imagery (30 m) and mapped to 21 Broad Habitat classes. It uses an updated LCM2015/LCM2007 spatial framework to enable compatibility and long-term change analyses. The dataset is land cover (not land use) and is delivered as vector polygons and raster products at multiple resolutions.

## Data products and structure

- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland
  - Key attributes: unique geometry identifier (gid), dominant class (mode), per-polygon class breakdown (_hist), recommended display class (_mode), uncertainty metrics (_conf, _stdev), polygon pixel count (_n), and source/composite information (_cmp)
  - Rich metadata per polygon, including dominant class and pixel-level breakdown
- 25 m raster
  - 3-band GeoTIFF: band 1 = dominant LCM1990 class, band 2 = mean per-polygon confidence, band 3 = percentage area of polygon covered by the modal class
  - Helps support analyses requiring gridded data with per-pixel confidence
- 1 km raster
  - Aggregated products derived from 25 m data
  - Dominant cover 1 km (target and aggregate classes)
  - Percentage cover 1 km for 21 target classes and 10 aggregate classes
  - Integer values; total may not sum exactly to 100 due to rounding and coast-adjacent areas
- Spatial scope and formats
  - Great Britain and Northern Ireland provided separately to reflect different projections
  - Coordinate systems: Great Britain uses British National Grid; Northern Ireland uses the Irish National Grid
  - Data are distributed as uncompressed GeoTIFFs (25 m and 1 km rasters) and a full vector product available on request

## Standards, metadata, and uncertainty

- Metadata and provenance
  - Rich metadata accompany the vector polygons, including dominant class and per-polygon pixel breakdown
  - Documentation and processing history retained to support reproducibility
- Uncertainty
  - Random Forest per-pixel probability provided as mean per polygon, included in both vector and 25 m raster data
  - Provides a quantitative measure of classification confidence at the polygon level
- Classification detail
  - 21 target classes derived from UK Broad Habitat definitions
  - Some classes are split or hierarchically related (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland)
  - 0.5 ha minimum mapping unit; polygons smaller than 0.5 ha or linears under 20 m are dissolved into surrounding landscape

## Access, licensing, and citation

- Data access
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector product available on request; licensing fees may apply for some users
  - Contact spatialdata@ceh.ac.uk for access guidance
- Citation and DOIs
  - All LCM1990 products have individual DOIs for citation (GB and NI variants)
  - Example citation format provided; DOIs are supplied for each product where available; some DOIs are listed as pending
  - Emphasizes clear, repeatable methods and traceability in publications
- Map projections and data structure
  - GB vector and raster use British National Grid; NI data use TM75 Irish Grid
  - Tables and appendices provide detailed technical parameters and mapping schemes

## Quality assurance and validation

- QA checks
  - Projections, spatial completeness, modal class presence (vector), data headings, value ranges (0–100 for rasters), and pixel sizes
- Validation
  - Full validation against other datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately
- Production practices
  - Based on a parcel framework linked to 2007 OS MasterMap data; field boundary changes are monitored for mapping accuracy

## Practical notes for Data Stewards

- Governance and reuse
  - LCM1990 is a stable, archived dataset with formal DOIs to support reproducibility and data provenance
  - Licences may apply for vector data access; check CEH licensing and contact for terms
- Use considerations
  - LCM1990 maps land cover, not necessarily land use; some classifications may not directly indicate land use (e.g., grass areas may be recreational or pasture)
  - Imperfect separations in complex habitats (e.g., Fen, Marsh and Swamp; Neutral vs Calcareous Grassland) may require aggregation or supplementary data for specific analyses
- Publication and data citation
  - When using in publications, cite the corresponding DOI and include author/date in text and full DOI in references
  - The dataset supports 25-year change analyses, enabling longitudinal studies when combined with later LCM products

## Additional information and contact

- Access and information:
  - CEH Environmental Information Platform: https://eip.ceh.ac.uk/
  - LCM1990 data page: https://www.ceh.ac.uk/services/land-cover-map-1990 or contact spatialdata@ceh.ac.uk
- Acknowledgement and references
  - Supported by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability
  - References provided for the underlying habitat definitions and prior LCM developments

- Appendix highlights (for context)
  - Class definitions and mapping nuances (e.g., how specific Broad Habitats are represented in LCM1990)
  - Color mapping recipes and example composite imagery used during production