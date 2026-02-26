# Soil Organic Carbon Dynamics (SOC-D)

- A data-intensive study within the UK-SCAPE programme (funded by NERC) to understand what controls soil organic carbon (SOC) dynamics across UK grassland-to-woodland contrasts and to identify areas at risk of SOC loss.
- Objectives focus on biotic and abiotic drivers, links between SOC, soil structure, chemistry, and functional biota, and development of a modular process-based SOC model.

## Study Design and Sites

- Five long-term field contrasts across England:
  - Gisburn-1, Gisburn-2 (north England)
  - Alice Holt (south England)
  - Wytham Woods (south England)
  - Kielder Forest (north England)
- Each contrast comprises two plots: plot 1 grassland, plot 2 woodland; each plot divided into six grids (1–3 grassland; 4–6 woodland) with 9 sampling locations per plot (total n ≈ 18 per site).
- Sampling occurred from 2018–2019 (field cores) and 2020–2021 (supplement measurements such as infiltration, ANPP).
- Aims to explore how woodland creation (net-zero targets) affects SOC, with site-specific management histories considered.

## Datasets and Measurements

- Four main data groups (plus metadata/connectors):
  - Aboveground productivity and litter
    - Aboveground Net Primary Productivity (ANPP) estimates using leaf dry matter content (LDMC) as predictor
    - Litter depth (3 measurements per sampling point)
  - Soil physical, chemical, and biological properties (0–100 cm; up to six depth increments)
    - Common: bulk density, soil moisture, pH (DIW and CaCl2), electrical conductivity (EC), LOI (via TGA), NO3-N, DOC, CEC, total C and N, P, etc.
    - Less common: texture, aggregates, enzymes, microbial biomass proxies
  - Soil hydraulic properties
    - Infiltration (unsaturated hydraulic conductivity, Kfs) via mini-disk infiltrometer
    - Soil water release curves (HYPROP) for 0–5 cm (and 30–35 cm where possible)
  - Earthworms
    - Counts and biomass by species across sites
  - Microbial communities
    - Prokaryotic and fungal community composition via 16S rRNA (V4–V5) and ITS2 amplicon sequencing
    - Metagenomes for functional gene analysis
- Density fractionation and SOM pools
  - Density fractionation into dissolved organic carbon (DOC), light fraction (LP), occluded fraction (OP), and mineral-associated fraction (MA)
  - Additional C, N content and enzyme activities for selected sites
- Data availability and linking
  - Sequencing data deposited in ENA (project PRJEB66294)
  - Data structure designed to link measurements across depths, grids, and samples

## Data Structure and Access

- Primary data packages (with connectors):
  - SOC-D_DATABASE_CONNECTOR.csv: links site, land-use, grid, core, transition/lateral distances, sample IDs
  - SOC-D_DATABASE_LOCATIONS.csv: location coordinates and OS grid references
  - SOC-D_DATABASE_ANPP.csv: ANPP estimates and site metadata
  - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth per location
  - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv: soil metrics for all depths (0–100 cm)
  - SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv: additional metrics for grid2 (grassland) and grid5 (woodland)
  - SOC-D_DATABASE_HYPROP_* and HYPROP_CONDUCTIVITY files: HYPROP raw data and conductivity metrics
  - SOC-D_DATABASE_EARTHWORMS.csv: earthworm counts and biomass per location
  - Earthworm species and biomass details (full taxonomy and weights)
  - Associated metadata and supplementary documents (Supplement A–C)
- Depths and sampling structure
  - Core depths predominantly 0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm
  - In some sites, topsoil defined as 0–5 cm or 0–15 cm; 15–60 cm ranges adjusted for consistency
- Data quality and missing values
  - Missing values indicated as NA
  - Site- and method-specific data gaps documented (e.g., HYPROP not collected at Alice Holt; some enzyme data excluded due to buffer issues)

## Analytical Methods and Quality Control

- ANPP estimation
  - Leaves collected May–July 2021; LDMC-based regression model used to predict ANPP
  - Uncertainty propagated via Bayesian (MCMC) framework; predictions with 95% credible intervals
- Soil chemistry and physical properties
  - Bulk density, water content, EC, pH (DIW and CaCl2), LOI (via TGA), total C and N (Vario EL elemental analyser), P, NO3-N, DOC
  - CEC measured via ammonium acetate extraction and ICP-OES; NH4-N and NO3-N quantified by colorimetric/discrete analysers
  - LOI quality checks with internal standards and replicates
- Particle size, aggregates, and SOM fractions
  - PSD by laser diffraction (Beckman Coulter LS13 320)
  - ASD measured to describe aggregate-size distributions
  - SOM density fractionation into LP, OP, MA fractions with DOC and nutrients measured per fraction
- Enzyme activities (selected sites)
  - Phosphatase, β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phenol oxidase
- Microbial analyses
  - Amplicon sequencing (16S rRNA, ITS2) and metagenomic sequencing
  - Data processing includes OTU/ASV clustering (DADA2), ordination (metaMDS), Kraken2 taxonomic annotation
- Data provenance and QA
  - UKCEH laboratories for soil analyses; standard QC protocols, calibration with standards, and blanks
  - ENA for sequence data; associations between samples and site/location via connectors
  - Discussions on microbial biomass estimates with caveats due to sample handling (freeze-thaw effects)

## Practical Implications for Analysts Monitoring the Environment

- Standardised data formats and an integrated framework enable cross-site comparisons of SOC dynamics under grassland-to-woodland transitions.
- The dataset supports:
  - Stock assessments (SOC, C/N pools) across depth profiles
  - Evaluation of how tree establishment and land-use change impact soil hydrology, structure, and biology
  - Multi-domain data integration (soil chemistry, physics, biology, and microbial ecology) for process-based SOC modelling
- Data products can feed into outputs such as national-scale SOC risk mapping, policy evaluation, and model calibration/validation.
- Completeness varies by metric and site, but core SOC and physical-chemical measurements are broadly available; missing data are clearly flagged.

## Project Context and Accessibility

- Part of the SOC-D project (Soil Organic Carbon Dynamics) under UK-SCAPE, with outputs intended for integration into national monitoring and modelling efforts.
- Collaborative acknowledgments include Forest Research and multiple UKCEH laboratories; data are deposited with detailed lineage and metadata to support reproducibility and reuse.