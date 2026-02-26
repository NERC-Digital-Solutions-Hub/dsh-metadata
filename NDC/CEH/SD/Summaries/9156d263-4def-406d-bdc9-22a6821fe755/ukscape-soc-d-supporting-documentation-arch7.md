# Soil Organic Carbon Dynamics (SOC-D) data description

- Purpose and scope
  - Provides co-located aboveground and belowground measurements across five grassland-to-woodland contrasts in England (2018–2021) to understand SOC dynamics and identify where UK soils are at risk or could store more carbon.
  - Aims to test biotic and abiotic controls on SOC stability and develop process-based modelling tools for SOC dynamics.

- Spatial extent and sites
  - Five site locations: Gisburn-1, Gisburn-2 (both in England), Alice Holt (South England), Wytham Woods (South England), and Kielder Forest (North England).
  - Each site comprises a grassland plot and a woodland plot (land-use contrast), subdivided into grids 1–6 with nine sampling locations per plot (18 sampling points per contrast).
  - Contrast boundary lies between grids 3 and 4; transects capture edge effects and confounding factors (e.g., proximity to roads or streams).

- Datasets and data types included
  - Aboveground measurements and productivity
    - Aboveground Net Primary Productivity (ANPP)
    - Litter layer depth
    - Leaf Dry Matter Content (LDMC) used to predict ANPP
  - Soil physical, chemical, and biological properties (0–100 cm, up to six depth increments)
    - Core-derived metrics: bulk density, soil water content, pH (DIW and CaCl2), electrical conductivity (EC), LOI, total carbon and nitrogen, phosphorus, nitrate-N, dissolved organic carbon (DOC)
    - Detailed soil fractions: CEC, exchangeable cations (Ca, Mg, K, Na), and related chemistry
  - Soil physical properties and hydrology
    - Unsaturated hydraulic conductivity (K) from mini-disk infiltrometer
    - Soil water release curves (HYPROP) for 0–5 cm and 30–35 cm depths (where available)
  - Soil texture and structure
    - Particle Size Distribution (PSD) via laser diffraction
    - Texture fractions (clay, silt, sand) and aggregate size distribution (ASD)
  - Soil organic matter (SOM) fractions
    - Density fractionation into LP (light particulate), OP (occluded particulate), MA (mineral-associated), and DOM
    - Concentrations of LP-C, OP-C, MA-C and corresponding N, as well as C:N ratios
  - Enzyme activities (select sites)
    - Phosphatase, beta-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phenol oxidase (with site-specific availability)
  - Microbial community data
    - Amplicon sequencing (16S rRNA, ITS) for bacteria/fungi
    - Shotgun metagenomics with derived metrics (nmds axes, functional gene counts)
    - Fungi:bacteria ratio via taxonomic annotation
  - Earthworms
    - Counts by species, fresh biomass, and total abundance
  - Ancillary connection data
    - SOC-D_DATABASE_CONNECTOR.csv ties sampling data to site/plot/grid/slice/sample IDs
    - SOC-D_DATABASE_LOCATIONS.csv provides location IDs with coordinates (OS grid references and lat/long)

- Data structure and connectivity
  - Datasets are divided into four primary content files plus two linking files:
    - CONNECTOR CSV: links SITE, LANDUSE, GRID, CORE, TRANSITION_DISTANCE, LATERAL_DISTANCE, SLICE, and SAMPLE_ID
    - LOCATIONS CSV: provides LOCATION_ID, grid references, coordinates (OS grid, latitude/longitude)
    - ANPP and LITTER_DEPTH: link via LOCATION_ID to provide ANPP means and litter depth per location
    - COMMON_SOIL_METRICS: contains core soil metrics for all depths and locations (SAMPLE_ID as key)
    - SOIL_METRICS_GRID2_GRID5: contains grid-specific depth data for select metrics
    - HYPROP and HYPROP-related files: hydraulic properties by location and sample
    - EARTHWORMS: earthworm counts and biomass by location
    - Microbial data: amplicon and metagenome derived metrics by location
  - The dataset is designed for join-by-ID workflows in GIS and analytics tools, enabling spatial joins between coordinates and soil/biogeochemical measurements.

- Data coverage and completeness
  - Complete for core, common soil measurements (e.g., LOI, BD, pH, EC, bulk density, soil water content).
  - Some less common or expensive measurements were limited to specific layers or sites (e.g., certain SOC fractions, enzyme activities, explicit texture data, HYPROP at some sites).
  For missing values, NA is used.
  - ANPP and LDMC-based predictions follow regression models; uncertainties reflected via 95% credible intervals from MCMC parameter samples.
  - Temporal coverage: field sampling primarily in 2018–2019 for core data, with ANPP and vegetation measurements up to 2021.

- Data quality and provenance
  - Samples processed in UKCEH labs with QA/QC protocols; internal standards and replicated samples used for many chemical analyses.
  - Standardised methods aligned with UK national soil datasets (Countryside Survey, GMEP, ERAMMP) and European LUCAS framework where applicable.
  - Metadata includes field sheet information, sampling matrices, and site-specific notes for soil cores and grid-level sampling.

- Access, formats, and where to find data
  - Data are available as CSV files described above, with accompanying supplemental documents (field sheets, Supplement A–C) and project metadata.
  - Raw microbial sequences deposited in ENA under project PRJEB66294; derived metrics provided in the soil-metrics files.
  - Project context and supplementary resources:
    - UK-SCAPE programme (funding and project context)
    - ELUM, GMEP, UGRASS, ERAMMP project pages
  - File naming and structure are designed to allow programmatic linking of location and sample IDs to datasets for GIS workflows.

- How to use these data in GIS and map-based analyses
  - Core workflow
    - Use SOC-D_DATABASE_LOCATIONS.csv to map locations (latitude/longitude and OS grid references).
    - Join ANPP and litter data via SOC-D_DATABASE_ANPP.csv and SOC-D_DATABASE_LITTER_DEPTH.csv to location plots.
    - Use SOC-D_DATABASE_COMMON_SOIL_METRICS.csv and SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv to attach soil properties to each location and depth.
    - Connect to HYPROP and hydraulic conductivity data (SOC-D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv, HYPROP-related files) for hydrological context.
    - Link earthworm data (SOC-D_DATABASE_EARTHWORMS.csv) and microbial data (amplicon/metagenome metrics) by LOCATION_ID.
  - GIS considerations
    - Coordinate system: use OSGB36 for grid references or convert to WGS84/ decimal degrees as needed for mapping and web GIS.
    - Depth dimension: incorporate depth slices (0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm) to create 3D or layered maps of soil properties.
    - Grid structure: reflect the five site contrasts and six grids per plot to visualize edge effects and gradients from grassland to woodland.
  - Visualization and analysis ideas
    - Map SOC stocks and carbon fractions by depth and by land-use contrast to identify SOC-rich/at-risk zones.
    - Compare ANPP and LDMC-derived productivity with soil carbon metrics across sites to explore biotic controls.
    - Overlay hydraulic properties with SOC fractions to study hydrological controls on SOC dynamics.
    - Integrate earthworm biomass and microbial community indicators to assess biological mediation of SOC persistence.
  - Data quality awareness
    - Note site-specific data availability (e.g., some measurements missing at Gisburn or Alice Holt) and interpret results with site-level context.
    - Use provided uncertainties (e.g., ANPP prediction intervals, QA for chemical measurements) in any modelling or risk assessment.

- Related outputs and references
  - Project basis and background: SOC-D aims to test the role of biotic and abiotic controls on SOC, with emphases on deep SOC pools and interactions with soil structure and biology.
  - Supplementary materials include field maps, core depth data, and site-specific notes to support spatial interpretation and reproducibility.

- Quick facts for GIS users at a glance
  - Five grassland-to-woodland contrasts across England: Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest
  - Depth coverage up to 100 cm; up to six depth increments
  - Datasets cover ANPP, litter depth, soil chemistry, hydraulic properties, texture/structure, SOM fractions, enzymes, microbial data, and earthworms
  - Two main connector/location files enable robust joins to all measurement datasets
  - ENA sequencing data available under PRJEB66294;-derived metrics provided in soil metrics files

- Credits and provenance
  - UKCEH and collaborators; supported by the UK-SCAPE programme (NE/R016429/1)
  - Acknowledgments to Forest Research and sampling sites (Alice Holt, Gisburn, Wytham Woods, Kielder Forest)

- Contact and further information
  - For access and data usage inquiries, refer to the SOC-D project pages and UKCEH/JISC data repositories associated with ELUM, GMEP, UGRASS, and ERAMMP collaborations.