# Dataset documentation

- The document describes Land Cover Map 1990 (LCM1990), a UK parcel-based land cover dataset created from Landsat-5 imagery (30 m) classified into 21 Broad Habitat-based classes, designed to support diverse user requirements and to be compatible with later LCM versions for long-term change analyses.
- LCM1990 replaces earlier LCM versions and follows an updated LCM2007 spatial framework to maximize compatibility with LCM2015 for multi-decadal change products.

- Data products and formats
  - Vector data set
    - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland
    - Eight key attributes per polygon, including: dominant class, source image, per-polygon confidence, histogram of class composition, polygon area (n), and a unique geometry identifier (gid)
    - Rich metadata per polygon, including dominant class, per-class pixel breakdown, and per-polygon classification confidence
  - Raster data sets
    - 25 m raster (three-band): band 1 = dominant LCM1990 class per polygon; band 2 = per-polygon Mean RF confidence; band 3 = percentage cover of the polygon by the modal class
    - 1 km raster products: dominant cover and percentage cover for both target (21 classes) and aggregate (10 classes) schemes
    - Separate GB and NI rasters to accommodate different projections
  - Data coverage and scale
    - Minimum mappable area > 0.5 ha; polygons smaller than 0.5 ha and linear features < 20 m were dissolved
    - 1 km products derived by aggregating 25 m raster data
  - Projections and coordinates
    - GB vector/raster: British National Grid
    - NI vector/raster: Irish National Grid (TM75)
    - Detailed extents and pixel grids defined in the metadata tables

- Class structure and labeling
  - 21 LCM1990 target classes derived from UK Broad Habitat classifications; several classes subdivided where spectral signatures allow finer resolution (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland)
  - Each polygon has a unique gid for unambiguous communication; gid should be retained in derivative work

- Data quality, uncertainty, and validation
  - Uncertainty information included: per-pixel probability from the Random Forest classifier, summarized as per-polygon mean confidence (and per-polygon stdev)
  - QA checks cover projections, spatial completeness, modal class presence in polygons (vector), value ranges (0–100 for raster), and pixel size accuracy
  - Full validation against external datasets and validation points; results planned for a separate publication
  - Metadata-rich design mirrors prior LCM products (LCM2007, LCM2000, LCM2015) to ensure traceability and comparability

- Citing and data provenance
  - All LCM1990 products have DOIs; explicit citations are recommended for replication and traceability
  - Example citation formats provided, with DOIs for GB vector, GB 25 m raster, GB 1 km targets/aggregates, and NI products; further DOIs are pending for some 1 km products
  - Data provenance and lineage are maintained through documented processing steps and the consistent use of the LCM framework

- Access, licensing, and governance
  - Data access through the CEH Environmental Information Platform (EIP)
  - Full vector product available on request; licensing fees may apply for some uses
  - Spatial data contact: spatialdata@ceh.ac.uk; additional information at the LCM1990 CEH page
  - Data licensing and DOIs support reproducibility and formal citation in publications

- Map structure and documentation context
  - LCM1990 is designed as a stable, archived data set with a rich metadata and documentation framework to support discovery, reuse, and interoperability
  - The dataset’s structure aligns with LCM2015 methods to enable a 25-year land cover change product (1990–2015) and facilitate cross-version comparisons
  - Appendix content (not reproduced here) includes detailed class definitions, color mappings, and composite image notes used during production

- Practical considerations for data stewards
  - Maintain gid across derivatives to preserve unambiguous communication
  - Preserve the rich metadata and uncertainty fields to support downstream quality assessment
  - Respect data access controls and license terms; properly cite DOIs in publications
  - Document any updates or reprocessing clearly, noting versioning (Version 1.0) and source imagery dates
  - Ensure alignment with UK CEH data governance standards and cross-compatibility with LCM2007/2015 baselines for integrative analyses

- Contact and additional information
  - Data access and licensing details: https://www.ceh.ac.uk/services/land-cover-map-1990
  - Data request and spatialdata inquiries: spatialdata@ceh.ac.uk
  - CEH EIP page for LCM1990 data: https://eip.ceh.ac.uk/lcm/lcmdata
  - Acknowledgement: supported by NERC and the UK-SCAPE programme; references to methodological documents and DOIs provided within the full dataset documentation