# UK Environmental Change Network Vegetation: Baseline (VB)

- Overview
  - One-off vegetation survey to generate a vegetation map and plots for ongoing monitoring; enables GIS-based visualization and spatial analysis; results feed into the ECN Data Centre and Environmental Information Platform.

- Provenance, governance, and access
  - Originator: ECN Data Centre (Centre for Ecology and Hydrology); Owners: UK government departments and agencies funding ECN (e.g., DEFRA, Natural England, NERC).
  - Acknowledgement requested; protocol reference and quality information provided; quality information accompanies the dataset.

- Data structure and storage (GIS implications)
  - Core data stored in an Oracle database with 12 site-specific tables.
  - Site metadata tables: D1VB_xxx (fields like SITECODE, SYEAR, etc.).
  - Plot data tables: D2VB_xxx (fields like SITECODE, PLOTTYPE, SDATE, FEATURES, UNSURVEYED, etc.).
  - Tables are site-specific (xxx = site code) and include metadata on units, descriptions, and reference mappings.
  - Practical GIS join: link site-level metadata to plot data via SITECODE; supports spatial queries and time-series analyses.

- Sampling design (GIS implications)
  - Approximately regular grid aligned to the National Grid with ~400 sample grid positions per site.
  - Up to 100 randomly located infill points for under-represented vegetation types.
  - Each point has a 2 m x 2 m plot centered, oriented N, E, S, W; plots may be permanently marked for long-term monitoring.
  - At each plot: a species list is recorded.
  - Design yields a baseline vegetation map and a set of plots suitable for long-term monitoring.

- Site coverage
  - 12 ECN sites: T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sour Hope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Y Wyddfa – Snowdon, T12 Cairngorms.
  - Each site includes location coordinates and a date range (early 1990s to late 1990s/2000).

- Features, species coding, and data standards
  - Features: coded as presence/absence types (e.g., P, W, S, H, D, F, B, N, X) describing landscape features.
  - Species and plant codes: extensive mappings of species names to codes, including Latin names, cross-references, synonyms, and hierarchical mappings; used in FIELDNAME and VALUE fields to represent plot-level presence/abundance or quality metrics.
  - The dataset contains a detailed, multi-way mapping for species codes with numerous synonyms and cross-references, enabling standardized GIS analyses across sites and time.

- Data quality and usage notes
  - Use accompanying quality information; data quality and transformations are part of data preparation.
  - Early prototype testing and user feedback are recommended for GIS products.
  - Quality codes follow a standard ECN list; unusual events are captured with code 999 and accompanying text.

- Quality codes (context for GIS tagging and filtering)
  - Standard ECN quality codes range from 100 to 999, describing issues from data loss (100) to various sampling and laboratory conditions.
  - 999 indicates an unusual event; associated text explains the circumstances.

- Access, reuse, and downstream use
  - Data support map-based products, spatial analyses, and multi-site time-series visualizations.
  - Appropriate for policy, client, and public-facing GIS visualizations; enables linking site metadata with plot data for spatial queries and temporal analyses.
  - Potential integration with Environmental Information Platform and adherence to metadata standards.