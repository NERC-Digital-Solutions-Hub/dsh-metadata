# Dataset Documentation Scottish Pinewoods Survey 1971 (Native Pinewood Survey)

- Purpose and scope
  - Detailed ecological survey defining variation in native Scottish pinewoods to support an integrated conservation strategy.
  - 1971-1972 survey across major native pinewoods in Scotland; 16 randomly assigned 200 m2 plots per wood (27 woods; 26 in 1971, 1 extra in 1972).
  - Aims include standardized data collection, metadata and documentation to enable future discovery and use.

- Geographic coverage
  - 27 Scots pine woods across Scotland, with precise OS grid references provided for each site.
  - Notable sites include Glentanar, Black Wood of Rannoch, Abernethy, Rothiemurchus, Glen Affric, Loch Maree, and Dulnan (surveyed 1972, west of Abernethy).

- Data files and structure (Data Model)
  - Scots_Pine_1971_Sites.csv
    - Site-level point locations (ID, NAME, OSGR, coordinates).
  - SCOTS_PINE_1971_SITE_INFO.csv
    - Descriptions of each site, plot-level data, habitat descriptions, slope, aspect, and survey dates.
  - SCOTS_PINE_1971_TREE_DATA.csv
    - Tree-based data per plot, including DBH, tree type, height, and dead indicators.
  - SCOTS_PINE_1971_GROUND_FLORA.csv
    - Ground flora per plot: vascular plants and bryophytes with cover, growth form, and naming (codes from field manuals).
  - SCOTS_PINE_1971_SOIL_DATA.csv
    - Soil horizon depths, pH, litter/organic layers, and related descriptors per plot.
  - Metadata fields describe plots (1-16 per site; some sites have up to 50 plots), codes, and data sheets used.

- Data collection design and methods
  - Nested quadrat system within each 200 m2 plot:
    - Trees, saplings & shrubs recorded across the plot; vascular plants recorded in progressively larger nested quadrats; bryophytes collected for identification.
  - Data recorded per plot include:
    - Vegetation: species name, DBH, height, dead indicators; bryophytes; % cover; presence/absence of other cover types.
    - Soil: horizon depth descriptions, horizon classifications, pH (top 0–15 cm).
    - Habitat: habitat categories, slope (degrees), aspect (magnetic bearing), site-level habitat descriptions.
  - Standardization and provenance:
    - Methods aligned with Bunce & Shaw (1973) and Bunce & Shaw (1971) Handbook of Field Methods (National Woodland Classification 1971).
    - Vegetation nomenclature aligned with Stace (1997); field handbooks provide precise definitions for categories and classes.

- Original purpose, sampling, and documentation
  - Objective: capture ecological variation beyond pre-1971 knowledge to inform conservation strategy.
  - Sample design: include major native pinewoods identified in literature; 16 randomly assigned plots per wood; additional plots (up to 50) at Abernethy noted.
  - Documentation includes detailed field handbooks, data sheets, and a robust data management effort.

- Data quality, standards, and provenance
  - Consistent data capture across sites using standardized codes and dictionaries.
  - Nomenclature and classifications referenced to established literature (Shaw & Bunce 1971; Stace 1997; Steven & Carlisle 1959).
  - Data management and documentation handled by CEH Lancaster and ITE Merlewood staff; field survey teams documented.
  - Acknowledges additional plots and methodological references; field sheets and code groups are described in the site and data dictionaries.

- Data availability and usage notes for Data Stewards
  - Data are provided as CSV files with explicit field definitions and coding (see the included CSV schemas for site, plot, tree, ground flora, and soil data).
  - OS grid coordinates enable geographic discovery and integration with other spatial datasets.
  - Data include start dates (July–August 1971; some 1972 entries) and site-level descriptions to aid contextual interpretation.
  - Related datasets and publications are listed (e.g., National Woodland Survey 1971; follow-up surveys 1973; later works by Bunce & Shaw).

- References and acknowledgements
  - Key references: Bunce R.G.H. & Shaw M.W. (1971, 1973) on field methods; Stace (1997) plant nomenclature; Steven & Carlisle (1959) native pinewoods.
  - Acknowledgements cover survey management, data management, and field survey teams.