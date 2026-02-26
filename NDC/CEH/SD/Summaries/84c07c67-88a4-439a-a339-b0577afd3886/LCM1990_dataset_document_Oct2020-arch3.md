# Dataset documentation

- Land Cover Map 1990 (LCM1990) is presented as a range of data products to support diverse requirements of the LCM user community, with a focus on providing stable, parcel-based land cover information for the UK derived from Landsat-5 30m imagery.
- The dataset aims to be compatible with later LCM products (LCM2007, LCM2015) to enable long-term change analyses (e.g., a 25-year land cover change product).
- LCM1990 is designed for easy interpretation and interoperability with other geospatial datasets, reflecting real-world boundaries through polygon-based mapping.

- Purpose for monitoring and policy:
  - Enables scrutiny and evaluation of environmental health and land cover changes.
  - Supports policy decisions and future planning by providing structured, harmonised land cover information.

- Core characteristics:
  - 21 land cover classes based on UK Biodiversity Action Plan Broad Habitats (spectrally defined classes).
  - Output formats include vector (polygon) data and raster products (25m and 1km resolutions) for broad-scale analyses and modelling.
  - Spatial framework and class definitions are aligned with LCM2015 methods to facilitate comparability over time.

- Data provenance and structure:
  - Vector data: parcel-based polygons with rich per-polygon metadata, including dominant class, class breakdown, and per-polygon confidence.
  - Raster data: 25m resolution raster (GB and NI) with three bands (dominant class, mean purity/confidence, and percentage cover for the polygon’s modal class); 1km rasters summarize 25m data to dominant and percentage cover for both target and aggregate classes.
  - The vector dataset contains millions of polygons (GB ~6.7M, NI ~0.9M).
  - The core product is the LCM1990 vector dataset; 25m raster is derived from it; 1km products are created by aggregating the 25m data.

- Metadata and uncertainty:
  - Each polygon contains a rich set of attributes, including dominant class, source image, per-polygon pixel counts by class, and a mean classification confidence (Random Forest).
  - Uncertainty is quantified per polygon and per-pixel in the raster products, enabling assessment of data reliability in analyses.
  - A per-polygon history of class composition (_hist) lists all classes present and their pixel counts; the modal class (_mode) is recommended for display.

- Data quality and validation:
  - CEH implements defined QA checks for projections, spatial completeness, modal class presence in polygons, value ranges (0–100 for rasters), and pixel size accuracy.
  - A full validation exercise was conducted against multiple reference datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.

- Spatial coverage and limitations:
  - British National Grid (GB) for Great Britain; Irish Grid (NI) for Northern Ireland; maps land cover (not strictly land use) and uses a minimum mappable area of >0.5 ha.
  - Parcels smaller than 0.5 ha or linear features under 20 m are dissolved into surrounding areas.
  - Coastal and marine areas are limited by the digital cartography; land and tidal areas are included, but some coastal features may be underrepresented.
  - Some classes can be spectrally confounded (e.g., certain grasslands vs. improved grassland; neutral vs. calcareous grassland), and users may need ancillary data or field validation for finer distinctions.
  - The dataset distinguishes between “land cover” and “land use” in places; not all land use can be inferred from land cover alone.

- Access and licensing:
  - Data are available via the CEH Environmental Information Platform (eip.ceh.ac.uk); full vector product available on request (licensing may apply).
  - DOIs are provided for all LCM1990 products to facilitate citation and reproducibility (separate DOIs for GB vector, GB 25m raster, GB 1km targets and aggregates, NI vector, NI rasters, etc.).
  - Licences and access conditions may incur fees for some users and applications.

- Data products and their relationships:
  - Vector: 6.7 million polygons (GB) and 0.9 million (NI); key attributes include class, source image, uncertainty, per-class pixel counts, and dominance metrics.
  - 25m raster: three bands (dominant class, per-polygon confidence, percentage cover); enables efficient analysis with both detail and manageable file sizes.
  - 1km rasters: aggregate percentage cover for target and aggregate classes; dominant cover per 1km pixel; used for national-scale modelling with other datasets (e.g., meteorology, species distribution).
  - Aggregates: defined 10 aggregate classes for 1km products to support applications requiring fewer classes.

- Citing and use in publications:
  - Each LCM1990 product has a DOI; citations should include authors and year in text and full DOI in references.
  - Examples provided for GB and NI vector and raster products; data citation practices are encouraged to support transparency and reproducibility.

- Documentation and support:
  - Documentation includes detailed class definitions, color mappings, and methodological notes (Appendices describing Broad Habitat definitions, color recipes, and composite image usage).
  - Acknowledgement of support and references to foundational Methodology (e.g., Jackson 2000 Broad Habitats, Morton et al. 2011 LCM2007, Rowland et al. 2020 for change products).

- Practical implications for monitoring frameworks:
  - Facilitates monitoring of environmental health indicators through stable, well-documented land cover data with explicit metadata and uncertainty estimates.
  - Supports governance needs for data quality, provenance, and reproducibility via DOIs, robust QA, and clear data lineage.
  - Provides scalable data products (vector and multi-resolution rasters) suitable for local to national policy evaluation and scenario modelling.