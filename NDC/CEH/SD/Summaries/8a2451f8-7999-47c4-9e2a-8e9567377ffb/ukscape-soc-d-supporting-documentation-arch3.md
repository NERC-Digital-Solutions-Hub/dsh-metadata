# Soil Organic Carbon Dynamics (SOC-D) data description

- Overview
  - Data from the SOC-D project, part of UK-SCAPE, collected 2018–2021 across five grassland-to-woodland contrasts in England to understand soil organic carbon (SOC) dynamics.
  - Aims: identify environmental health measures to scrutinise policy, assess SOC controls under climate/land management changes, identify UK areas at risk of SOC loss, and support future decision-making with a modular process-based SOC model.
  - Key questions: sensitivity of SOC to climate/management; links between SOC, soil structure, chemistry, and biota; which metrics and models best reflect SOC dynamics; and locations in the UK most at risk or suitable for SOC protection/storage.

- Study design and sites
  - Five grassland-to-woodland contrasts: Gisburn-1, Gisburn-2 (Gisburn), Alice Holt, Wytham Woods, and Kielder Forest.
  - Each site comprises two plots (grassland vs woodland) with grids 1–6 and nine sampling locations per plot (18 samples per site).
  - Sampling: 0–100 cm soil cores with multiple depth increments; in-situ measurements of ANPP, soil infiltration, and earthworms in grids 2 and 5; topsoil 0–5 cm and 0–15 cm (where applicable) for certain analyses.
  - Field work occurred mainly 2018–2019, with additional measurements 2020–2021; SOC-D aims to relate biotic/abiotic controls to SOC turnover and vulnerability.

- Datasets and data structure
  - Four main environmental datasets (described in detail with linking files):
    - Aboveground net primary productivity (ANPP) and litter layer depth (2018–2019 litter measurements; 2021 ANPP via LDMC-based model).
    - Soil physical, chemical, and biological properties for 0–100 cm (up to six depth increments; common and less common properties).
    - Soil hydraulic properties (HYPROP-based water release curves; unsaturated hydraulic conductivity via mini-disk infiltrometer; in situ and lab measurements).
    - Earthworm counts and biomass (species-level counts and weights).
  - Data linking and location metadata:
    - SOC-D_DATABASE_CONNECTOR.csv: maps site, plot, grid, core, and sample IDs; includes distances to transition boundary and grid edges, and slice/depth information.
    - SOC-D_DATABASE_LOCATIONS.csv: site/location coordinates and grid references.
  - Additional datasets (site and depth-specific) connected via sample IDs:
    - SOC-D_DATABASE_ANPP.csv: ANPP estimates (mean and bounds) linked to location IDs and site data; LDMC-based predictions with uncertainties.
    - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth (mean of three measurements per grid) linked to locations.
    - SOC-DATABASE_COMMON_SOIL_METRICS.csv: common soil metrics across depths (0–1 m) including field water content, EC, BD, pH, LOI, total C/N, nitrate, DOC, CEC, etc.
    - SOC-DATABASE_SOIL_METRICS_GRID2_GRID5.csv: grid2 (grassland) and grid5 (woodland) soil metrics for all depths; extensive sociodata with C, N, P, enzyme activities, microbial community proxies, etc.
    - SOC-D_DATABASE_HYPROP_*, SOC-DATABASE_HYPROP_RETENTION_T_PF.csv: HYPROP raw data and derived hydraulic properties (pF, water content, K) for different bands; multiple files encapsulating conductivity and retention data.
    - SOC-DATABASE_EARTHWORMS.csv: earthworm counts, fresh biomass, and species-specific biomass data.
  - Microbial data (derived from topsoil and subsoil):
    - Prokaryotic and fungal community composition via 16S rRNA (bacteria) and ITS (fungi) amplicon sequencing; metagenome analyses with DIAMOND/SAMSA2 pipelines; data deposited in ENA under PRJEB66294 with derived metrics (e.g., NMDS axes, F/B ratios).
  - Depth and sampling details:
    - Topsoil segmentation: 0–15 cm (two layers in some sites: 0–5 cm and 15–60 cm), with later adjustments to 15–60 cm for consistency; five depth increments for 0–100 cm cores (0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm).

- Sampling methods and analytical workflow
  - Field sampling design:
    - Homogeneous vegetation and slope selection within grassland plots; grids 1–3 in grassland and 4–6 in woodland; three sampling points per grid chosen based on environment (distance to trees, slope, etc.).
    - Randomized sampling points mapped with GPS; distance to contrast boundary and lateral distance recorded for each core (Supplement A).
  - Core types and depths:
    - Hyprop cores (0–5 cm; some 30–35 cm) for soil hydraulic properties.
    - National survey-style cores (0–15 cm) for standard topsoil metrics and to assess compaction effects.
    - Split Tube Sampler (0–30 cm) and Cobra precision corer (0–100 cm; sometimes 30–100 cm) for deep soil profiling.
    - Russian auger for peat soils (0–50 and 50–100 cm segments).
  - Associated measurements:
    - ANPP: leaf biomass collected from dominant species (May–July 2021) with LDMC used to predict ANPP (cover-weighted LDMC; cLDMC).
    - Litter depth: measured around sampling points.
    - HYPROP: soil water release curves; unsaturated hydraulic conductivity via mini-disk infiltrometer.
    - Earthworms: hand-sorted 25 cm × 25 cm blocks to 25 cm depth; field-to-lab processing with species-level identification.
  - Laboratory analyses and QA/QC:
    - Soil carbon and nutrients: total C and N (Vario EL); total P; NO3-N; DOC; CEC; cations via ICP-OES; EC and pH in DIW and CaCl2; LOI via TGA; bulk density from cores.
    - PSD and texture: laser diffraction after OM removal; sieve-based sand fraction corroboration; duplicate checks and internal standards.
    - Density fractionation of SOC: four fractions (DOC, LP, OP, MA) using sodium polytungstate (SPT) with subsequent C and N analyses; SOM fraction data stored as LP-C, OP-C, MA-C, etc.
    - Enzyme activities: hydrolytic (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase) and phenol oxidase activities; measurement via fluorometric or spectrophotometric assays; site-specific data availability.
    - Microbial analyses: DNA extraction, 16S/ITS amplicon sequencing, metagenomics; data pipelines (DADA2, Kraken2, SAMSA2); derived ordination scores and microbial proxies.
  - Data processing and normalization:
    - Topsoil and subsoil layers harmonized to align with UK national datasets (Countryside Survey, GMEP, ERAMMP, LUCAS); decisions documented to ensure cross-dataset compatibility.

- Data quality, gaps and governance
  - Completeness and limitations:
    - Complete for common soil metrics (BD, LOI, pH, EC, etc.); some less common measurements (e.g., certain SOC fractions, enzymes) limited to select layers or grids (e.g., grids 2 and 5; top/bottom layers).
    - Missing data indicated as NA; some measurements not collected (e.g., HYPROP at Alice Holt; litter measurements in some cores).
    - Microbial biomass measurements were compromised by freeze-thaw effects, limiting reliability for certain indicators.
  - Metadata and transparency:
    - Detailed field and lab methods documented; supplementary materials provide site maps, coring details, and measurement rationales.
    - Metadata gaps acknowledged; data governance emphasizes data sharing while balancing data quality and provenance.
  - Data accessibility:
    - Raw sequencing data deposited in ENA (PRJEB66294); derived metrics and environmental measurements provided in SOC-D data files; connectors enable cross-dataset integration.

- Use for monitoring, policy, and modelling
  - The dataset supports monitoring of SOC dynamics under land-use change (grassland to woodland) across representative UK soils and climates.
  - Enables development and validation of process-based SOC models; informs land-management policies aimed at SOC sequestration and climate mitigation.
  - Provides a framework for linking field measurements to national-scale soil data and monitoring programmes, with explicit data-structure to facilitate integration with other datasets.

- Supplementary materials and funding
  - Supplement A–C provide field mapping images, coring details, and measurement rationales.
  - Project funded as part of UK-SCAPE, grant NE/R016429/1; collaborations with Forest Research; data contributions from Alice Holt and Kielder sites.

- References and data sources
  - Methods and QA references span HYPROP manuals, soil analysis standards, and foundational soil carbon literature (e.g., SOC fractions, enzyme assays, microbial community analyses).
  - ENA deposition PRJEB66294 for sequencing data; national and international datasets cited for comparability (LUCAS, Countryside Survey, GMEP, ERAMMP).