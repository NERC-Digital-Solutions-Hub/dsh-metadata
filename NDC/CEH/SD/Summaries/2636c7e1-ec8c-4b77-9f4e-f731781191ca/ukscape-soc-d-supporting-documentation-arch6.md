# Soil Organic Carbon Dynamics (SOC-D) data description

- Aim and scope
  - Understand biotic and abiotic controls on soil organic carbon (SOC) dynamics, identify UK areas most at risk of SOC loss, and inform policies to increase SOC storage.
  - Test scale- and mechanism-related hypotheses across key UK land-use–soil combinations; develop a flexible, modular process-based SOC model that can be embedded in other soil models.
  - Data comprise co-located aboveground and belowground measurements across five grassland-to-woodland contrasts in England (2018–2021) and include extensive soil physical, chemical, and biological properties, hydrological data, earthworms, and microbial community data.

- Study design and site coverage
  - Five land-use contrasts: Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest.
  - Each contrast includes two plots (grassland vs woodland), each plot divided into three grids (total 6 grids per site). Nine sampling locations per grid, yielding 18 sampling cores per site.
  - Sampling timeline:
    - 2018–2019: soil cores (0–100 cm) and some surface measurements.
    - 2020–2021: additional measurements for infiltration, ANPP, earthworms, and HYPROP where possible.
  - Sampling layout designed to capture distance to the woodland-grassland boundary and lateral distance from grid edges.

- Datasets included
  - Aboveground Net Primary Productivity (ANPP) and litter layer depth (2018–2021)
  - Soil physical, chemical, and biological properties (0–100 cm; up to six depth increments)
  - Soil hydraulic properties: soil water release curves (HYPROP) and unsaturated hydraulic conductivity (K)
  - Earthworm counts and species identification
  - Microbial community data: amplicon sequencing (bacteria 16S, fungi ITS) and shotgun metagenomics
  - Derived microbial and soil metrics (e.g., NMDS axes, gene abundance metrics, community composition ratios)

- Data structure and linking
  - Two key connector/location files to enable cross-dataset linkage:
    - SOC-D_DATABASE_CONNECTOR.csv: 14 fields; site, land-use, plot, grid, core, transition and lateral distances, slice, lab layer, location IDs, sample IDs, and GPS/location details
    - SOC-D_DATABASE_LOCATIONS.csv: 6 fields; location IDs with OS grid references, coordinates, and latitude/longitude
  - Four main data suites with sample IDs connected via the connector:
    - SOC-D_DATABASE_ANPP.csv: ANPP estimates (mean, high, low) linked to location IDs and site metadata
    - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth at each location (mean of three measurements per grid)
    - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv: soil metrics for all depths (0–1 m) across all sites
    - SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv: grid2 (grassland) and grid5 (woodland) soil metrics including fractions, C, N, CEC, and other properties
  - Hydrology datasets:
    - SOC_D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv
    - HYPROP raw data and HYPROP-related files (HYPROP_RETENTION_T_PF.csv, HYPROP_CONDUCTIVITY_K_PF.csv, HYPROP_CONDUCTIVITY_K_T.csv)
  - Earthworms: SOC_D_DATABASE_EARTHWORMS.csv (counts, biomass, species IDs)
  - Field and lab methods documentation supplements (Supplement A–C) with site maps, coring details, and measurement planning
  - Microbial data: sequence reads deposited in ENA (PRJEB66294) with derived metrics (OTU tables, NMDS axes, and functional gene datasets)

- Measurements and methods (highlights)
  - ANPP: predicted from cover-weighted leaf dry matter content (cLDMC) using regression; uncertainty via the posterior distribution from MCMC; model and workflow in RMarkdown
  - Litter depth: measured in three locations per sampling point
  - Soil cores: multi-method approach
    - Hyprop cores for 0–5 cm (and 30–35 cm at some sites) to derive water release curves
    - National survey-style 0–15 cm topsoil cores for compacted soils
    - Split Tube Sampler 0–30 cm for alternative topsoil sampling
    - Deep 0–100 cm cores (mineral soils with Cobra precision corer; peat soils with Russian auger)
  - Infiltration and HYPROP: field mini-disk infiltrometer for unsaturated conductivity; HYPROP for hydraulic properties and pore-size distribution
  - Earthworms: hand-sorting method; species-level counts and biomass
  - Soil properties (0–1 m): standard suite including pH (DIW and CaCl2), EC, bulk density, LOI, total C and N, total P, NO3-N, DOC, CEC, exchangeable cations (Ca, Mg, K, Na)
  - SOM fractionation (density fractionation): dissolved organic carbon (DOC), light fractions (LP), occluded fractions (OP), mineral-associated OM (MA); carbon and nitrogen per fraction
  - Enzyme activities: hydrolytic enzymes (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase) and phenol oxidase; some sites exclude data due to method issues
  - Microbial analyses: DNA extraction from soils; 16S rRNA (bacteria), ITS (fungi) amplicon sequencing; shotgun metagenomics; data processed with DADA2 for OTU/ASV, DIAMOND/SEED for metagenomics, and downstream ordination
  - Data quality and QC: internal standards, replicates, calibration checks, and batch controls described; some data excluded (e.g., Gisburn buffers for enzyme assays) due to methodological issues
  - Data scope and completeness: complete for common metrics (LOI, BD, soil water content, pH, EC); some measurements restricted to select layers or grids (e.g., certain SOC fractions, enzymes, HYPROP) or not collected in some plots; missing values indicated as NA

- Background and program context
  - UK-SCAPE program (started 2018; NE/R016429/1) funded to deliver national-scale data and models for environmental understanding
  - SOC-D aims to test hypotheses on SOC sensitivity to climate and land management, SOC–soil structure–biota feedbacks, useful SOC metrics and models, and UK regional risk mapping
  - Grassland-to-woodland contrasts chosen to explore SOC responses to woodland expansion, a key policy question for net-zero pathways

- Data accessibility and usage notes
  - Primary data hosted as a deposition with explicit linking structure (CONNECTOR and LOCATIONS) plus multiple data files
  - ENA deposition for microbial sequences; derived metrics included to support cross-dataset analyses
  - Site and grid geolocation provided to enable spatial analyses and integration with other UKCEH datasets
  - Documentation supplements (A–C) provide field protocols, coring details, and measurement planning
  - Potential uses: cross-site comparisons of SOC drivers, integration with process-based SOC models, dashboards for policy-relevant SOC risk mapping, and data-driven insights for land-management strategies

- Acknowledgments and references
  - Collaboration with Forest Research; field sites Alice Holt and Kielder Forest; contribution to GIS mapping and data provisioning
  - References cover standard methods for soil carbon work, SOC dynamics literature, and HYPROP/enzyme/microbial analysis protocols

- Supplementary information highlights
  - Supplement A: field-sheets and Google Earth visualization for grassland–woodland contrasts
  - Supplement B: detailed soil coring data by site and corer type
  - Supplement C: measurement rationale, prioritization, and analysis plans for additional soil and ecosystem measurements