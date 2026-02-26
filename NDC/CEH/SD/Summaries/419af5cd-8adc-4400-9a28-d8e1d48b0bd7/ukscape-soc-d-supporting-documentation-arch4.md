# Soil Organic Carbon Dynamics (SOC-D)

## Overview
- Large, collaborative study across five grassland-to-woodland contrasts in England (2018–2021).
- Co-located aboveground and belowground measurements to understand soil organic carbon (SOC) dynamics.
- Four primary data datasets plus ancillary metadata and rich methodological detail.

## Data Description (what’s included)
- Four main datasets:
  - Aboveground net primary productivity (ANPP) and litter layer depth (0–5 cm) measurements.
  - Soil physical, chemical, and biological properties for 0–100 cm across up to six depth increments.
  - Soil hydraulic conditions including water release curves and unsaturated hydraulic conductivity (HYPROP-based and field measurements).
  - Earthworm counts and species identification (with biomass data).
- Datasets are co-located across five sites (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest) with two plots per site (grassland vs. woodland) and a grid system to capture distance from the contrast boundary.
- Data structure includes:
  - CONNECTOR and LOCATION CSV files to link samples and sites.
  - ANPP and LITTER_DEPTH files.
  - COMMON_SOIL_METRICS, SOIL_METRICS_GRID2_GRID5, HYDRAULIC, HYPROP, EARTHWORMS datasets.
  - Raw sequencing data (16S rRNA, ITS, and shotgun metagenomes) with derived metrics (e.g., OTUs, NMDS axes, functional annotations).
- Missing values are recorded as NA; completeness varies by measurement type (common measurements complete; deeper/lab-intensive metrics limited to selected depths/sites).

## Project Background
- Objective: understand physical, chemical, and biological controls on SOC dynamics; identify UK regions and conditions at risk of SOC loss; identify management practices to enhance SOC storage.
- Core questions:
  1) SOC sensitivity to climate and land-management changes (local/global).
  2) Feedbacks between SOC, soil structure, chemistry, and functional biota.
  3) Metrics and modelling approaches that reflect current SOC understanding.
  4) UK regions most at risk and opportunities to protect/increase SOC.
- Rationale for grassland-to-woodland contrasts: rising woodland creation and unsettled evidence on when trees increase SOC; contrasts help test these dynamics across UK soil-vegetation-climate combinations.
- Site selection prioritized age/management history, access, area of grassland/woodland, and transect confounding factors.

## Site Selection and Contrasts
- Five contrasts chosen from an initial pool of 42 sites (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest).
- Sites feature long-term grassland vs. woodland plots with standardized plot/grid layouts and random sampling points within grids.
- Site-specific descriptions cover land-use history, soil type, and management context (e.g., Gisburn COSMOS-UK flux tower, Alice Holt road-N deposition gradient considerations).

## Data Collection Methods
- Sampling design:
  - Grassland plots and adjacent woodland plots divided into grids (1–3 in grassland; 4–6 in woodland).
  - Nine sampling locations per plot (18 total per contrast).
  - Sampling points randomized within each grid; distance to boundary and lateral distance recorded.
- Field measurements and samples:
  - ANPP: harvest of dominant vegetation at grids 2 and 5; LDMC used to predict ANPP.
  - Litter depth: measured at three points per sampling location.
  - Soil cores: multiple depth increments (0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm) using Hyprop, national survey cores, Split Tube, Cobra, and Russian Auger.
  - HYPROP cores for soil water release curves (0–5 cm at most sites; 30–35 cm at some) and unsaturated conductivity via mini-disk infiltrometer.
  - Earthworms: hand-sorted from 25 cm × 25 cm × 25 cm blocks (15 min sorting time).
- Lab processing (summary):
  - Samples stored at 4°C; 1-m cores processed in segments; careful labeling and layering.
  - Determinations include EC, pH (DIW and CaCl2), BD, LOI via TGA, total C and N, total P, NO3-N, DOC, CEC, enzyme activities, and microbial biomass proxies (subject to quality controls).
  - ANPP regression models use LDMC and leaf area data with site-specific calibration.
  - Hydraulics: HYPROP data analyzed with HYPROP-FIT; Kfs via mini-disk data.
  - Soil texture and structure: PSD via laser diffraction; aggregate size distribution; SOM density fractionation into LP, OP, MA fractions plus DOM.
  - Enzyme activities: hydrolytic (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase) and oxidative (phenol oxidase); results expressed as µmol substrate g−1 soil h−1.
  - Microbial ecology: DNA extraction, amplicon sequencing (16S rRNA for bacteria, ITS2 for fungi) and shotgun metagenomics; downstream OTU and functional analyses; microbial community metrics (e.g., NMDS axes) included.
- Quality and site-specific notes:
  - Some field/lab measurements excluded due to issues (e.g., incorrect buffers at Gisburn; microbial biomass results affected by freezing); overall QC processes documented.

## Analytical Methods and Quality Control
- ANPP estimation: model-based predictions using LDMC; uncertainty propagated from regression model parameters via MCMC chains.
- Soil hydraulics: HYPROP data analyzed with HYPROP-FIT; pore-size/active porosity inferred from curves; Kfs derived from field measurements.
- Soil metrics: standard UK CEH SOPs for C, N, P, NO3-N, DOC, EC, pH; CEC measured with NH4 acetate and ICP-OES; LOI via TGA with internal QC checks.
- PSD and SOM fractions: laser diffraction for PSD; density fractionation for LP/OP/MA and DOM; carbon and nitrogen content measured per fraction; enzyme activities standardized to substrate g−1 soil h−1.
- Microbial analyses: sequence data processed with DADA2 (OTU inference) for amplicons; metagenomes annotated with DIAMOND/SAMSA2; ordination and sample metrics included.
- Connectivity: two CSVs (SOC-D_DATABASE_CONNECTOR.csv and SOC-D_DATABASE_LOCATIONS.csv) enable linking sample IDs to site coordinates and plots.

## Data Structure and Access
- Datasets are organized with connectors to align location, plot, grid, core, and slice information (SAMPLE_ID and LOCATION_ID keys).
- Main data files:
  - ANPP and LITTER_DEPTH: site-location linkage with ANPP estimates and litter-depth means.
  - COMMON_SOIL_METRICS: 0–1 m soil metrics across all sites and depths.
  - SOIL_METRICS_GRID2_GRID5: detailed soil metrics for grids 2 and 5 (grassland and woodland).
  - HYDRAULIC_CONDUCTIVITY and HYPROP files: field and HYPROP-derived hydraulic properties.
  - EARTHWORMS: earthworm counts and fresh biomass by species.
  - SEQUENCE DATA and derived metrics: amplicon and metagenome results, including NMDS axes and taxonomic/functional counts.
- ENA deposition: sequencing data (PRJEB66294) with derived metrics included in the respective tables.
- Data completeness and NA entries documented across datasets.

## Supplementary Information and Acknowledgements
- Supplementary materials provide site maps, field-sheets, and detailed coring information (including core depths and attempts per site).
- Supplement C outlines a prioritized, site-wide list of measurements and analyses with rationale and plans.
- Acknowledgement: UK-SCAPE programme (NE/R016429/1) and Forest Research collaboration; access permissions for Alice Holt, Kielder Forest, and Gisburn.
- Related projects and datasets reference: ELUM, GMEP, UGRASS, ERAMMP.

## Data Usefulness for Data Leaders
- Comprehensive, multi-ecosystem dataset enabling systems-level analysis of SOC dynamics under grassland-to-woodland transitions.
- Rich metadata and connecting files support cross-site integration, reproducibility, and policy-relevant analyses.
- Enables development and testing of process-based SOC models incorporating biological, physical, and chemical controls across UK landscapes.