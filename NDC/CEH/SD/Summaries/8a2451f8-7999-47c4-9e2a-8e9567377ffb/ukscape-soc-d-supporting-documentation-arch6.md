# SOC-D: Soil Organic Carbon Dynamics

- A data-rich project describing co-located aboveground and belowground measurements across five grassland-to-woodland contrasts in England (2018–2021), funded by the UK-SCAPE programme.
- Primary aim: understand physical, chemical, and biological controls on soil organic carbon (SOC) dynamics to identify where UK SOC stocks are most at risk and how to enhance storage through management.

## What the datasets cover

- Four main data datasets, plus linking/locations files:
  - Aboveground Net Primary Productivity (ANPP) and litter layer depth (0–5 cm, 0–15 cm topsoil considerations) for five contrasts.
  - Soil physical, chemical, and biological properties from 0–100 cm (up to six depth increments) per site.
  - Soil hydraulic conditions, including soil water release curves (HYPROP) and unsaturated hydraulic conductivity (minidisk infiltrometer) measurements.
  - Earthworm counts and biomass by species (including detailed species-level data).
- Additional materials:
  - ENA deposition for metagenomic and amplicon sequencing (bacteria, fungi, and functional genes).
  - Density fractionation and multiple SOM (soil organic matter) pools (LP, OP, MA fractions, plus DOM).
  - Extracellular enzyme activities and microbial community data (amplicon sequencing and metagenomes).

## Data structure and accessibility

- Two connector files: SOC-D_DATABASE_CONNECTOR.csv (experimental layout and sampling geometry) and SOC-D_DATABASE_LOCATIONS.csv (site/location coordinates and OS grid references).
- Datasets 2–5 (ANPP, litter depth, soil metrics, hydraulics, earthworms) link via LOCATION_ID to the connector file.
- Four main soil metrics datasets (COMMON_SOIL_METRICS, SOIL_METRICS_GRID2_GRID5, plus TOP_AND_SUB_SOIL metrics) cover different depths and resolutions.
- Microbial data provided as pre-processed axes (nmds scores) plus sequencing counts; ENA accession PRJEB66294 holds raw data.
- All missing values are encoded as NA; detailed linking allows cross-dataset joining (sample/core IDs, depth slices, grid IDs, etc.).

## Site selection, design, and sampling

- Five long-term grassland-to-woodland contrasts across England:
  - Gisburn-1, Gisburn-2 (N England)
  - Alice Holt (S England)
  - Wytham Woods (S England)
  - Kielder Forest (N England)
- Each contrast comprises two plots (grassland vs woodland) with three grids per plot (total 6 grids per site) and 9 sampling locations per plot (18 locations per contrast).
- Sampling depths and measurements:
  - Soil cores collected to 100 cm, with 0–5 cm (top) and 30–35 cm (where possible) HYPROP cores in grids 2 and 5.
  - Infiltration and earthworms measured in specified grids (2 and 5); litter depth recorded around sampling points.
- Field methodology emphasizes randomized sampling within grids and a transect approach to account for proximity effects from trees on soil processes.

## Data collection methods and analytical approaches

- ANPP estimation using leaf dry matter content (LDMC) and cover-weighted LDMC (cLDMC) as predictors; ANPP values produced with regression models and uncertainties propagated via MCMC.
- Soil core processing:
  - Hyprop cores for unsaturated hydraulic properties (0–5 cm; 30–35 cm where possible).
  - National survey style cores for 0–15 cm (topsoil) to assess compaction effects.
  - 0–15 cm to 0–30/50–100 cm cores using Cobra precision corer, Split Tube Sampler, and Russian Auger, with depth increments defined per site.
  - Bulk density, pH (DIW and CaCl2), EC, LOI (via TGA), and total C and N are measured; P, NO3-N, and DOC quantified using standard procedures.
- Soil physical, chemical, and biological analyses:
  - PSD and LD/texture metrics via laser diffraction.
  - SOM density fractions: LP (light particulate), OP (occluded particulate), MA (mineral-associated), plus DOM; total C and N measured per fraction.
  - Enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) using MUB/MC substrates or L-DOPA for phenol oxidase; some site data excluded due to buffer issues.
  - Microbial community profiling:
    - Amplicon sequencing (16S rRNA for bacteria, ITS2 for fungi) using Earth Microbiome Project protocols.
    - Shotgun metagenomes; data processed to derive OTU/genic abundance metrics and ordination scores; ratio metrics like fungi-to-bacteria derived via Kraken2/PlusPFP processing.
- Earthworms: hand-sorted counts with biomass, species-level identifications, and notes per location.
- Supplemental materials document field sheets, core-depth details, and supplementary methods (Supplement A–C).

## Quality control, completeness, and limitations

- Completeness:
  - Common soil measurements (LOI, BD, soil moisture, pH, EC) are complete.
  - Less common/expensive measurements (e.g., certain SOC fractions, enzymes, detailed textures) are limited to specific layers (top or bottom) or grids (2 and 5); missing values clearly labeled as NA.
- QA/QC:
  - Robust QA measures across chemistry (internal standards, duplicates, blanks), instrument calibration, and reference materials.
  - LOI and other critical measurements include batch-level QC checks; enzyme and microbial data flagged for site-specific data quality issues (e.g., Gisburn buffer problems).
  - Hypotheses around soil depth and sampling inconsistencies acknowledged; soil depth increments standardized as 0–5, 5–15, 15–30/60 cm, with adjustments to ensure adequate material.
- Limitations:
  - Microbial and enzymatic data quality affected by sample handling and storage (e.g., freezing impacts microbial biomass data).
  - Certain site-specific measurements (e.g., ENA data, enzyme assays) have site-level exclusions or caveats.
  - Some measurements (e.g., HYPROP cores) were not collected at all sites (e.g., Alice Holt).

## Project context and aims (high-level)

- The SOC-D project seeks to test modern SOC controls, focusing on biotic-abiotic interactions, soil structure, and function across UK land-use gradients.
- Core questions addressed:
  - SOC sensitivity to climate and land management changes.
  - Critical feedbacks between SOC, soil structure, chemistry, and biota.
  - Metrics and modeling approaches that reflect contemporary SOC dynamics.
  - UK regions most at risk of SOC loss and opportunities to enhance SOC storage.
- The grassland-to-woodland contrasts were selected to evaluate plausible future land-use changes in the UK and their impact on SOC dynamics.

## Usage notes for data users

- Data are structured to allow integrated analyses across multiple domains (physical, chemical, biological, and molecular).
- Depth-resolved data enables SOC stock modeling across topsoil and subsoil compartments.
- Connections across datasets are made via SITE/LOCATION IDs, GRID, CORE, SLICE, and SAMPLE_ID fields; ENA data provide raw microbial sequences for deeper analyses.
- Users should account for site- and grid-specific caveats noted in the metadata (e.g., measurement limitations, excluded samples, buffer issues).

## Acknowledgments and project metadata

- Acknowledges UK-SCAPE programme support and collaboration with Forest Research, including access permissions at Alice Holt and Kielder Forest.
- Data described are part of a broader suite of projects (ELUM, GMEP, UGRASS, ERAMMP) and build on long-term soil monitoring programs at UKCEH and partners.