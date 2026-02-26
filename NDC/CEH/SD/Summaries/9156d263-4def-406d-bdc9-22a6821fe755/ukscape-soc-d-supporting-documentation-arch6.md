# Soil Organic Carbon Dynamics (SOC-D) dataset description

- Five long-term grassland-to-woodland contrasts across England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest) were sampled between 2018 and 2021.
- Data are organized into four primary datasets plus metadata linking files:
  - Aboveground Net Primary Productivity (ANPP) and litter layer depth
  - Soil physical, chemical, and biological properties (0–100 cm)
  - Soil hydraulic properties (hydraulic conductivity and HYPROP-derived measurements)
  - Earthworm counts and identifications (species-level)
- Each land-use contrast comprises two plots (grassland vs woodland) subdivided into grids (1–3 grassland, 4–6 woodland) with 18 sampling locations per site (2 plots × 9 locations).

## Datasets and key variables

- ANPP and litter depth
  - ANPP estimates derived from leaf dry matter content (LDMC) via a regression model
  - Litter depth measured at three points per sampling location
  - LDMC and cover-weighted LDMC used to predict ANPP
- Soil physical, chemical, and biological properties (0–100 cm)
  - Core-based measurements across depth increments: 0–5, 5–15 (or 15–60 depending on site), 15–30, 30–50/60, 50/60–100 cm
  - Core types and processing details documented (Hyprop, national survey cores, split tube, Cobra, Russian auger)
  - Parameters include EC, pH, BD, LOI, total C and N, total P, NO3–N, DOC, CEC, extractable cations (Ca, Mg, K, Na)
  - PSD (laser diffraction), texture, and aggregate size distribution; SOM density fractions (LP, OP, MA) and dissolved organic carbon (DOC) in density fractions
  - Extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) at a subset of sites
  - Microbial community data: 16S rRNA and ITS amplicons; shotgun metagenomes; downstream metrics (NMDS axes, gene counts)
- Soil hydraulic properties
  - Unsaturated hydraulic conductivity (Kfs) at specific tensions via mini-disk infiltrometer
  - HYPROP-derived water release curves (pF) and associated parameters
  - HYPROP raw data and derived conductivity across multiple datasets
- Earthworms
  - Counts and fresh biomass by species across locations
  - Detailed species list and abundances provided
- Data integration
  - CONNECTOR and LOCATION metadata to link samples across datasets
  - Locations include OS grid references, coordinates (lat/long), easting/northing

## Sites, design, and context

- Sites: Gisburn-1, Gisburn-2 (northern England), Alice Holt (south), Wytham Woods (south), Kielder Forest (north)
- Each site/contrast is selected to reflect age, management history, and landscape context; contrasts include grazed/un-grazed grassland, broadleaf or conifer woodland, and, at Kielder, unmanaged grassland with conifer woodland nearby
- Transect-based sampling to capture proximity effects of trees on soils and to enable distance-to-boundary analyses
- Field sampling used randomized point selection within grids, with GPS-enabled sampling matrices to quantify transition and lateral distances

## Collection methods and QA/QC

- Field sampling order and layout:
  - Grassland and woodland plots laid out, grids established, and sampling points randomized within grids
  - Infiltration (HYPROP) and Hyprop cores collected in grids 2 and 5 (where feasible)
  - Earthworm cores hand-sorted in 25 cm × 25 cm × 25 cm blocks to 25 cm depth; 15-minute sorting time
  - Litter depth recorded around sampling points
  - Litter and vegetation processed for ANPP and LDMC analyses
- Core types and depths:
  - Hyprop cores: 0–5 cm (and 30–35 cm at some sites)
  - National survey style cores: 0–15 cm
  - Split Tube Samplers: 0–30 cm
  - Cobra precision cores: 0–100 cm (or 30–100 cm)
  - Russian auger: 0–50 cm and 50–100 cm for deep cores
- Laboratory analyses and QA:
  - LOI and LOI-based SOC estimates via thermogravimetric analysis (TGA)
  - Bulk density (BD), EC, pH (DIW and CaCl2 method)
  - Total C and N by elemental analyzer
  - P by acid digestion and colorimetric measurement
  - NO3–N and DOC by standard extraction and analysis procedures
  - CEC by ammonium acetate extraction with ICP-OES
  - Soil texture by PSD and laser diffraction; additional aggregate-size data
  - SOM density fractions (LP, OP, MA) and DOC in density fractions via density separation using sodium polytungstate
  - Extracellular enzyme activities (site- and method-specific adjustments due to earlier issues)
  - Microbial ecology:
    - 16S rRNA (bacteria) and ITS (fungi) amplicon sequencing; OTUs via DADA2
    - Metagenomes via shotgun sequencing; functional annotation and ordination
    - Taxonomic/functional ratios (e.g., fungi:bacteria) derived from sequencing data
- Data quality notes:
  - Several enzyme measurements omitted due to buffer issues at Gisburn sites
  - Some soils frozen for enzyme/biomass analyses; microbial biomass data impacted by freeze-thaw
  - Missing values explicitly indicated as NA

## Data structure and access

- Two linking metadata files:
  - SOC-D_DATABASE_CONNECTOR.csv: links samples to site, plot, grid, core, and depth slices; includes transition and lateral distances
  - SOC-D_DATABASE_LOCATIONS.csv: site IDs, coordinates, latitude/longitude
- Datasets (each with site/location linkage):
  - SOC-D_DATABASE_ANPP.csv: ANPP estimates and LDMC-derived predictors; includes site, landuse, and LDMC-related inputs
  - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth (mean of three measurements per sampling location)
  - SOC-DATABASE_COMMON_SOIL_METRICS.csv: core-based soil metrics for all depths (0–100 cm)
  - SOC-DATABASE_SOIL_METRICS_GRID2_GRID5.csv: soil metrics for topsoil (0–15 cm) in grids 2 and 5; extensive mineral fraction metrics
  - SOC-DATABASE_HYPROP_* and HYPROP-related files: HYPROP raw data, retention curves, and conductivity (Kfs) at specified tensions
  - SOC-D_DATABASE_EARTHWORMS.csv: earthworm counts, biomass, and species identifications
- Additional supplements:
  - Supplement A: field-site visualization and mapping references
  - Supplement B: site-specific coring details and depth information
  - Supplement C: measurement matrix and analysis rationale for broader ecosystem measurements
- Data are provided with NA for missing values; sequencing and metagenomic data have accession and processing details
- Project and data provenance:
  - SOC-D is part of UK-SCAPE, funded by NERC
  - Data support and collaborations acknowledged (UKCEH, Forest Research)

## Purpose and applicability for data use

- Enables analysis of how biotic (soil biota, roots, earthworms) and abiotic (climate, soil structure, chemistry) controls affect soil organic carbon dynamics across UK land-use contrasts
- Supports development of process-based SOC models integrated with national soil monitoring datasets
- Facilitates cross-site comparisons of SOC sensitivity to climate and land management, soil structure-chemistry-biota feedbacks, and SOC risk areas across the UK
- Provides self-contained, linkable data products (ANPP, soil properties, hydraulics, earthworms, microbial data) suitable for dashboards, reports, or in-depth analyses