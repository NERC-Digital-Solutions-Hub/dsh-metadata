# Soil Organic Carbon Dynamics (SOC-D) data description

- Purpose and scope
  - A UK-led study funded by NERC UK-SCAPE to understand the biotic and abiotic controls on soil organic carbon (SOC) dynamics.
  - Aims to identify where UK soil carbon stocks are most at risk and how to increase SOC through land management.
  - Investigates SOC sensitivity to climate and management, links between SOC, soil structure/chemistry/biota, and suitable metrics/models for SOC dynamics.
  - Uses grassland-to-woodland contrasts to explore SOC responses amid expected woodland creation.

- Datasets and content
  - Four main co-located data sets collected at five long-term grassland-to-woodland contrasts across England (2018–2021):
    - Aboveground Net Primary Productivity (ANPP) and litter layer depth (0–5 cm, and 0–5/30–35 cm for some plots).
    - Soil chemical, physical and biological properties for up to six depth increments within 0–100 cm.
    - Soil hydraulic conditions: soil water release curves and unsaturated hydraulic conductivity (K) measurements.
    - Earthworm counts and species identification/weights.
  - Additional data connections provided to link all measurements to site/location and sampling points.
  - Datasets include a range of common metrics (e.g., LOI, BD, pH, EC, NO3-N, DOC, CEC, total C/N, P), soil texture, PSD/aggregate metrics, SOM density fractions (LP, OP, MA) and DOC, along with microbial community data (amplicon sequencing and metagenomics) and enzyme activities.

- Study sites and sampling design
  - Five contrasts across England:
    - Gisburn-1 (G1), Gisburn-2 (G2), Alice Holt (AH), Wytham Woods (WW), Kielder Forest (KF).
  - Each site includes two plots: Plot 1 = grassland, Plot 2 = woodland; each plot subdivided into six grids (grassland grids 1–3, woodland grids 4–6).
  - Nine sampling locations per plot (total n = 18 per site).
  - Field sampling conducted mainly November 2018–March 2019, with additional measurements in 2020–2021.
  - Grassland-to-woodland contrasts chosen to reflect potential woodland creation impacts, with site-specific considerations (e.g., Gisburn blocks near roads, Wytham openness, Kielder bog/peat context).

- Field and laboratory methods (highlights)
  - Aboveground productivity and litter
    - ANPP estimated from leaf material and leaf dry matter content (LDMC) using a model; LDMC values sourced from species-specific data (LEDA, ECPE) when needed.
  - In-field measurements
    - Infiltration (0–5 cm in most sites; 30–35 cm in WW/KF where possible), earthworm counts (grids 2 and 5 where present), litter depth (three per sampling point).
    - HYPROP soil hydraulic measurements for 0–5 cm (and 30–35 cm at some sites) in grids 2 and 5.
  - Soil sampling and cores
    - Deep soil cores (0–100 cm) collected with multiple corers:
      - Hyprop cores (0–5 cm; 30–35 cm at some sites).
      - National survey style cores (0–15 cm).
      - Split Tube Sampler (0–30 cm).
      - Cobra precision corer (0–100 cm; some sections 30–100 cm).
      - Russian auger for peat/wetter conditions (0–50 and 50–100 cm).
    - 0–100 cm cores subdivided into depth increments: 0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm.
  - Soil analyses and quality control
    - Bulk density, field moisture content and LOI (via TGA) for SOC estimation.
    - Soil pH (DIW and CaCl2), EC, NO3–N, DOC, CEC, total C and N, total P.
    - PSD via laser diffraction (LD) after OM removal; aggregated fractionation and OC content in LP/OP/MA fractions; DOM analysis.
    - SOM density fractions: LP (light particulate), OP (occluded particulate), MA (mineral-associated), plus DOM; elemental and C/N measurements across fractions.
    - Extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) where buffers and samples permitted.
    - Microbial communities: DNA extraction from 0–5 cm and 30–60 cm (topsoil and subsoil for selected sites), 16S (bacteria) and ITS2 (fungi) amplicon sequencing; shotgun metagenomics for functional profiling; downstream community ordination (e.g., nmds) and taxa/genes abundance metrics.
  - Data processing and lab workflow notes
    - Topsoil depth definitions: 0–5 cm or 0–15 cm depending on site; 15–60 cm increments adjusted per site.
    - Some measurements were not performed at all sites (e.g., HYPROP at Alice Holt; some earthworm measurements at WW; microbial biomass data affected by freezing).
    - QA steps include internal standards, duplicates, and batch-level checks for EC/pH, LOI, and other analyses.

- Data structure and linking (connecting data)
  - Two primary linking files:
    - SOC-D_DATABASE_CONNECTOR.csv: connects samples to site, land use (grassland/woodland), plot, grid, core, depths, and sampling coordinates; includes transition and lateral distances for the sampling points.
    - SOC-D_DATABASE_LOCATIONS.csv: site-level location information with OS grid references, coordinates (X, Y, latitude/longitude).
  - Datasets and file structure
    - ANPP.csv: ANPP estimates and associated LDMC-derived predictors; linked via LOCATION_ID.
    - LITTER_DEPTH.csv: litter depth measurements linked by LOCATION_ID.
    - COMMON_SOIL_METRICS.csv: soil metrics (0–100 cm) for all depths; includes fields like FIELD_WATER_CONTENT, ELECTRICAL_CONDUCTIVITY, BD, pH, LOI, total C/N, NO3-N, DOC, CEC, etc.
    - SOIL_METRICS_GRID2_GRID5.csv: detailed soil metrics for grids 2 (grassland) and 5 (woodland) across depths; includes LP/OP/MA fractions and related C/N, nutrients, and enzyme metrics.
    - SOIL_METRICS_TOP_AND_SUB_SOIL.csv: topsoil and subsoil metrics (0–15 cm for topsoil, deeper sections as required) including NO3-N, DOC, CEC, pH, enzyme data, etc.
    - HYDRAULIC_CONDUCTIVITY.csv and HYPROP-related files: unsaturated hydraulic conductivity (Kfs) and HYPROP raw data for pF curves and conductivity, enabling HYPROP-FIT analyses.
    - EARTHWORMS.csv: earthworm counts and biomass by species, location-linked to sampling coordinates.
  - Data completeness and caveats
    - Completeness highest for common soil metrics; some deeper or more expensive measurements limited to subsets (e.g., SOC fractions, CEC, specific enzyme activities) or absent from certain grids/sites.
    - Missing values represented as NA; some data adjustments and site-specific exclusions due to methodological issues (e.g., wrong buffers at Gisburn, FE data gaps).

- Quality control, data provenance and limitations
  - Processing and QA performed at UK Centre for Ecology & Hydrology laboratories; use of accredited methods (SOP3102 for C and N, etc.).
  - Internal standards and replicated samples included for accuracy and precision; QC protocols described for EC, pH, LOI, and other measures.
  - Some data limitations:
    - Microbial biomass data affected by freezing; microbial biomass measurements not considered reliable.
    - Certain measurements not collected or fully analyzed at all sites (e.g., HYPROP at Alice Holt; some earthworms at WW; buffer issues affecting enzyme data at Gisburn).
  - Supplementary materials provide field-sheet details, coring records, and measurement prioritization for broader context (Supplements A–C).

- Background and references
  - SOC-D project context: part of the UK-SCAPE programme; builds a flexible, modular, process-based SOC model to be embedded in other soil models.
  - Core questions addressed include SOC sensitivity to climate/land management, SOC–soil structure/chemistry/functional biota feedbacks, appropriate metrics/models for SOC dynamics, and UK-wide areas at risk of SOC loss.
  - Key supporting references and methodologies cited for sampling, LDMC predictions, SOC fractionation, HYPROP analyses, and microbial sequencing workflows.

- Practical use and aims for policy and monitoring
  - Data designed to support national-scale understanding of SOC dynamics under different land-use scenarios, informing land-management policies to enhance SOC storage.
  - Standardized, co-located datasets enable cross-site comparisons and integration with long-term soil monitoring programs.
  - Outputs are intended to feed process-based SOC models and drive policy-relevant insights into SOC resilience and carbon storage potential across the UK.