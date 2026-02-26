# Dataset documentation

- Land Cover Map 1990 (LCM1990) is documented as a complex data product suite designed to support diverse monitoring needs and to enable scrutiny of policy and decisions.
- The document provides an in-depth guide to LCM1990 data products, their generation, structure, formats, and usage considerations.

## Purpose and scope

- LCM1990 provides parcel-based land cover data for the UK, classified into 21 classes aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Aims to support monitoring, comparability across time, and integration with other geospatial datasets for environmental health assessments and policy evaluation.

## Data products and structure

- Vector data set (core product)
  - Polygons with rich attributes per parcel, including dominant class, per-polygon class breakdown, confidence metrics, and metadata.
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Key attributes include gid (unique parcel identifier), _hist (list of classes present and pixel counts), _mode (dominant class code 1–21), _purity (percent area of modal class), _conf (mean classifier confidence 0–100), _stdev (uncertainty), _n (number of pixels), cmp (composite image source).
- Raster data sets
  - 25m raster: derived from the vector data; three bands (dominant class per polygon, per-polygon mean confidence, polygon modal coverage percentage). Used for detailed analyses and compatible with 25m resolution modelling.
  - 1km raster products: aggregate percentage cover and dominant class per 1km pixel, derived from the 25m raster. Includes:
    - 1km dominant cover for LCM1990 Target classes (1 band)
    - 1km dominant cover for LCM1990 Aggregate classes (1 band)
    - 1km percentage cover for Target classes (21 bands)
    - 1km percentage cover for Aggregate classes (10 bands)
  - Great Britain and Northern Ireland datasets are provided separately to accommodate different projections (British National Grid for GB; TM75 Irish Grid for NI).
- Spatial framework and compatibility
  - LCM1990 uses a polygon-based framework compatible with LCM2015, enabling long-term change analysis (e.g., 25-year change product).
  - Class mapping and labels follow the Broad Habitat framework; some classes are subdivided based on spectral signatures (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).

## Class taxonomy and mapping details

- 21 target LCM1990 classes derived from UK Broad Habitats (as per Jackson et al., 2000), with occasional refinements:
  - Example splits include Urban vs Suburban; Heather vs Heather grassland; Saltmarsh vs Littoral sediment within Littoral Sediment Broad Habitat.
- LCM1990 maps land cover (not strictly land use); some land-use distinctions may not be inferable from spectral data alone (e.g., recreation grass vs grazing land).
- MMU and mapping rules
  - Minimum mappable area: >0.5 ha.
  - Parcs smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscapes during production.
- Metadata richness
  - Each polygon includes extensive metadata describing processing, class composition, and per-polygon uncertainty.
- Uncertainty information
  - Per-pixel classifier probability from Random Forest is provided as mean per-polygon uncertainty in vector and in 25m raster.
- Color mapping (Appendix 3)
  - Standardized color mappings for each class to support visualization and rapid interpretation.

## Data access, citation, and governance

- Access
  - 25m and 1km raster datasets available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH; licensing may apply.
- Citation and DOIs
  - All LCM1990 products have individual DOIs; citations should include author, date, and DOI.
  - Examples provided for GB and NI vector and raster products (DOIs listed in the document).
  - Guidance available at the CEH citing-data resource.
- Projections
  - GB vector and raster data: British National Grid (EPSG: 27700).
  - NI: Irish National Grid (TM75 Irish Grid, EPSG: 29903).
- Quality assurance
  - Defined QA checks for projections, spatial completeness, modal class presence in polygons, value ranges, and pixel size consistency.
  - Validation performed against external datasets (Countryside Survey, National Forest Inventory) with results to be published separately.
- Versioning and lineage
  - LCM1990 is archived with DOIs for traceability; data lineage and processing steps are documented to support reproducibility.

## Data context for monitoring frameworks

- Rich metadata and uncertainty metrics support transparency and data governance for monitoring programs.
- Public data sharing is addressed with explicit data provenance (gid, hist, conf, etc.), facilitating audit trails and comparability over time.
- Availability of both detailed (vector) and scalable (1km/25m raster) products supports multi-scale monitoring and integration with other environmental datasets (e.g., meteorological, biodiversity, and species distribution data).
- The dataset supports long-term change analyses (e.g., 1990–2015) by using a common spatial framework and consistent class definitions across LCM versions.

## Practical considerations for use

- When using the data for policy monitoring, consider the MMU, potential misclassifications between spectrally similar classes, and the need for ancillary data to refine land-use interpretations.
- For computational workflows, the vector product offers rich attribute fields at the cost of larger file sizes; the 25m raster provides a lighter, grid-based alternative with per-polygon uncertainty embedded in the data.
- Ensure proper citation of DOIs and acknowledgement of CEH/NERC support when publishing analyses derived from LCM1990 data.