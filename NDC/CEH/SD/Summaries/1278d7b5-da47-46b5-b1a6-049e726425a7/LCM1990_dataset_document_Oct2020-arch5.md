# Dataset documentation

- Purpose and scope
  - Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map provided as a range of data products to support diverse user needs.
  - Built to be compatible with other LCM products (e.g., LCM2015) and to enable a 25-year land cover change product; uses a consistent spatial framework and polygon boundaries for interpretability and interoperability.
  - Classes are based on the UK Biodiversity Action Plan Broad Habitat definitions and derived from Landsat-5 imagery (30 m).

- Data lineage and framework
  - Generated from two-date composite satellite imagery; framework derived from Ordnance Survey MasterMap-like sources for GB and Northern Ireland equivalents; updated to align with LCM2015 methods.
  - Aims to maximize interoperability across LCM versions and support long-term change analysis (1990–2015 context in related work).

- Data products and structure
  - Vector data set (core product)
    - Polygons with attributes: unique geometry identifier (gid), class label, per-polygon histogram of class composition, mode (dominant class), purity, confidence, standard deviation, pixel count, and composite image source.
    - GB: ~6.7 million polygons; NI: ~0.9 million polygons.
  - Raster data sets
    - 25 m raster: three-band product (band 1 = dominant class per polygon; band 2 = mean per-polygon confidence; band 3 = percentage of polygon area covered by dominant class).
    - 1 km raster: derived aggregates
      - Dominant 1 km per target and aggregate classes (1 band each)
      - Percentage cover at 1 km for all 21 target classes (and 10 aggregate classes; multiple bands)
    - 25 m and 1 km rasters are provided separately for Great Britain and Northern Ireland due to different projections.
  - Class structure
    - 21 LCM1990 target classes; 10 aggregate classes for raster products to support various application needs.
    - Some classes have subdivisions (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).

- Metadata and uncertainty
  - Rich metadata at polygon level; includes dominant class, distribution of pixel-level classifications, and classification probability (from Random Forest).
  - Per-polygon uncertainty measures included (conf, stdev) and per-polygon pixel counts.
  - Uncertainty is also represented in the raster products (mean confidence per polygon).

- Data quality and validation
  - QA checks cover projections, spatial completeness, modal class presence in polygons, documentation consistency, value ranges (0–100 for rasters), and pixel size accuracy.
  - Validation performed against external data sources (Countryside Survey, National Forest Inventory, validation points); results to be reported in a separate publication.
  - The dataset is a stable, archived product with DOIs to support citation and reproducibility.

- Data access and licensing
  - Access via the CEH Environmental Information Platform (eip.ceh.ac.uk); 25 m and 1 km rasters are available online; full vector product on request.
  - Licence fees may apply for some users/applications; contact spatialdata@ceh.ac.uk for details.
  - Projections: GB vector and GB rasters use British National Grid; NI vector and rasters use TM75 Irish Grid.

- Citing and DOIs
  - Each LCM1990 product has a DOI to enable precise citation (GB vector, GB 25 m raster, GB 1 km targets/aggregates, NI vector, NI 25 m raster, NI 1 km targets/aggregates).
  - Example citation format: (Author et al., Year) with the DOI listed in references; see provided tables for exact DOIs per product and region.

- Practical notes for use
  - The vector product provides rich attribute data suitable for detailed analysis and communication, but larger file sizes may be unwieldy; the 25 m raster offers a simpler, metadata-light alternative with the same land cover detail.
  - For 1 km products, be aware that percentage sums may not exactly equal 100 due to rounding, and coastal areas may show slightly lower totals due to mapping extents.
  - The gid (geometry identifier) in vector data is recommended to be retained for traceability and unambiguous communication across datasets and analyses.

- Access points and further information
  - Data overview and access: CEH Environmental Information Platform and CEH Land Cover Map 1990 information page.
  - Additional documentation and contact: spatialdata@ceh.ac.uk; link to dataset-specific pages for more details, citations, and support.

- Context and references
  - LCM1990 aligns with Broad Habitat definitions (JNCC Jackson 2000) and prior LCM products (LCM2007, LCM2015) to support cross-version analyses.
  - Appendix content and colour-mapping recipes are provided to assist users in visualizing and communicating classes consistently.
  - Acknowledgement of support and references to related methodological reports and validation studies.