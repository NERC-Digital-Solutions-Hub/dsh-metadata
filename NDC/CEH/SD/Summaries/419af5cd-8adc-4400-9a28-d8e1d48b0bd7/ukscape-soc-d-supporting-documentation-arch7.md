# Soil Organic Carbon Dynamics (SOC-D)

- Five grassland-to-woodland contrasts across England were studied (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest).
- Aims: understand biotic/abiotic controls on soil organic carbon (SOC) dynamics, identify UK regions at SOC risk, and test policies to increase SOC through land management.
- Sampling design: two plots per site (grassland vs woodland), each plot divided into three grids (grassland grids 1–3; woodland grids 4–6); nine sampling locations per plot (total 18 per site) randomly chosen within grids.
- Temporal scope: soil measurements collected 2018–2019; additional measurements (e.g., ANPP, infiltration, earthworms) 2020–2021; ANPP measurements in 2021; vegetation sampling in May–July 2021.
- Spatial references: site coordinates provided (OS grid references and lat/long) to enable GIS mapping; sampling locations linked to a common location ID for data integration.

- Datasets and data structure (four main data groups plus linking files)
  - SOC-D_DATABASE_CONNECTOR.csv: links all datasets via SITE_NAME, LANDUSE, PLOT, GRID, CORE, TRANSITION_DISTANCE, LATERAL_DISTANCE, SLICE, LAB_LAYER, and LOCATION_ID.
  - SOC-D_DATABASE_LOCATIONS.csv: spatial references for locations (LOCATION_ID, GRID_REFERENCE OS grid; X/Y; LAT/LON; coordinates).
  - ANPP and Litter Depth:
    - SOC-D_DATABASE_ANPP.csv: aboveground net primary productivity (ANPP) estimates per LOCATION_ID with model type and site details.
    - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth (cm) as mean of three measurements per grid.
  - Soil physical, chemical, and biological properties (0–1 m; grids 2 and 5 for some measures; depth increments defined):
    - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv: core-level soil metrics (e.g., field water content, bulk density, pH DIW/CaCl2, LOI, total C and N, total P, NO3-N, DOC, CEC, etc.).
    - SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv: subset of soil metrics for grids 2 (grassland) and 5 (woodland), with detailed fractionation and enzyme metrics.
    - SOC-D_DATABASE_SOIL_METRICS_TOP_AND_SUB_SOIL.csv: topsoil vs subsoil metrics (0–15 cm and below 50 cm) including NO3-N, DOC, CEC, various elemental concentrations, enzyme activities, and other soil properties.
  - Soil hydraulic properties and hydraulics:
    - SOC-D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv: unsaturated hydraulic conductivity (Kfs) at specified tensions.
    - HYPROP raw data and HYPROP-derived files (HYPROP_RETENTION_T_PF.csv, HYPROP_CONDUCTIVITY_K_PF.csv, HYPROP_CONDUCTIVITY_K_T.csv): raw and processed HYPROP data for pF and water content and corresponding hydraulic conductivity.
  - Earthworms:
    - SOC-D_DATABASE_EARTHWORMS.csv: earthworm counts by species, fresh biomass, total abundance, and notes per LOCATION_ID.
  - Soil Organic Matter (SOM) density fractionation:
    - Density fractions: LP (light particulate), OP (occluded particulate), MA (mineral-associated), plus DOM; top-level C and N for each fraction.
  - Microbial community and function:
    - Amplicon sequencing (16S rRNA for bacteria; ITS2 for fungi) and metagenomes; derived metrics include OTU abundances, NMDS axes, and fungal/bacterial ratios (Kraken2/bioinformatic outputs).
  - Additional soil metrics (grid 2/5 and top/sub soil aligned with UK national datasets) including C/N ratios, CEC, extractable nutrients, enzyme activities (some sites excluded due to buffer issues); quality control and documentation provided.

- Site and sampling details relevant for GIS
  - Sites and contrasts:
    - Gisburn-1 (grassland x conifer), Gisburn-2 (grassland x broadleaf), Alice Holt (grassland x broadleaf), Wytham Woods (grassland x broadleaf), Kielder Forest (grassland x conifer).
  - Grid layout and boundary:
    - Transition boundary between grids 3 and 4; grids 1–3 on grassland, 4–6 on woodland.
    - Distances to boundary and lateral offsets recorded for each location (Supplement A data).
  - Measurements per location:
    - In 0–5 cm: ANPP, litter depth; in 0–5 cm and 30–35 cm: HYPROP sampling (where possible); earthworms measured in grids 2 (grassland) and 5 (woodland).
    - Deeper soil cores (0–100 cm) collected to 5 depth increments: 0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm (examples vary by site).
  - Core types and collection:
    - Hyprop cores (0–5 cm; 30–35 cm at some sites)
    - National survey style cores (0–15 cm)
    - Split Tube Sampler (0–30 cm)
    - Cobra precision corer (0–100 cm or 30–100 cm)
    - Russian auger (0–50 and 50–100 cm)
  - Data quality and limitations:
    - Some measurements not collected at all sites (e.g., HYPROP at Alice Holt; earthquake of field samples).
    - Enzyme data quality issues at Gisburn (buffer error) led to removal from dataset; microbial CUE and some microbial measurements impacted by sample handling (freeze-thaw effects).
    - Data completeness is described per dataset with NA values where measurements were not made.

- Use and integration for GIS and map-based data products
  - Data are designed for integration into GIS via:
    - Location-level linkage through LOCATION_ID to all co-located measurements across datasets.
    - Spatial coordinates provided in both OS grid and WGS84 lat/long for accurate mapping and projection.
    - Grid-based sampling geometry (Grids 1–6) enabling spatial interpolation and visualization of SOC-related properties across transects from grassland to woodland.
  - Potential map-based products:
    - SOC stock maps by depth increment (0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm) by site and land-use contrast.
    - Soil hydraulic properties maps (Kfs, HYPROP-derived curves) by grid and depth.
    - Fractionated soil organic matter maps (LP/OP/MA/DOC) by grid and site.
    - Enzyme and microbial community indicators (e.g., fungal:bacteria ratios, NMDS axes) at location level for landscape-scale SOC dynamics.
    - Earthworm diversity and biomass distribution across grassland and woodland.

- Data quality indicators and caveats
  - Completeness: common soil measurements complete; less common/expensive measures limited to subsets; NA indicates missing data.
  Data are suitable for cross-site comparisons but with site-specific caveats (e.g., enzyme data removed at Gisburn; microbial data affected by storage/processing).
  Temporal alignment and differences in depth definitions were reconciled where possible, but users should heed depth and grid-specific nuances when aggregating.

- Documentation and access
  - Data are organized with explicit linking files (CONNECTOR and LOCATIONS) to join site, plot, grid, and core information with measurements.
  - Detailed method descriptions, QA steps, and supplementary information (Supplement A–C) support reproducibility and aid GIS data processing and interpretation.

- Acknowledgments and context
  - Part of UK-SCAPE programme; supported by NERC; collaboration with UKCEH and partner sites; multiple datasets align with ELUM, GMEP, UGRASS, and ERAMMP initiatives.