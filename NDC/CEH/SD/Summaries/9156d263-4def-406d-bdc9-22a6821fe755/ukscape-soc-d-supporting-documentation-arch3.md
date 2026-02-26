# Soil Organic Carbon Dynamics (SOC-D) project data descriptor

- Purpose and aim
  - Develop environmental health measures to scrutinise policy, evaluate policy effectiveness, and inform future decisions.
  - Understand biotic/abiotic controls on soil organic carbon (SOC) dynamics to identify UK areas at risk and inform land management for SOC storage.
  - Provide tools and data to support process-based modelling and integration with national soil-monitoring frameworks.

- Study design and sites
  - Five long-term grassland-to-woodland contrasts across England:
    - Gisburn-1 (N England), Gisburn-2 (N England), Alice Holt (S England), Wytham Woods (S England), Kielder Forest (N England).
  - At each site, two plots (grassland vs woodland) with a transect comprising six grids (grassland grids 1–3; woodland grids 4–6) and 9 randomized sampling locations per plot (total sampling locations per site: 18).
  - Grassland-to-woodland contrasts chosen to explore SOC responses to woodland creation and varying tree influence on SOC storage.

- What was measured and datasets included
  - Aboveground and belowground measurements (2018–2021):
    - Aboveground net primary productivity (ANPP) and litter layer depth.
    - Soil properties: chemical, physical, and biological across up to six 0–100 cm soil layers; soil hydraulic properties (water release curves and unsaturated hydraulic conductivity); earthworm counts and species.
  - Four main data datasets (co-located measurements):
    - ANPP and litter depth (0–5 cm and 30–35 cm data subsets where applicable).
    - Soil properties (chemical, physical, biological) across depth increments.
    - Soil hydraulic properties (HYPROP-derived water-release curves; unsaturated conductivity).
    - Earthworm counts and biomass (species-level data).
  - Depths, site soils, vegetation, and management practices documented per site.

- Data collection methods (field)
  - Homogeneous vegetation and slope-appropriate field transects established; grids within grassland and woodland sampled.
  - Sampling points randomly distributed within grids; distance to contrast boundary and lateral distances recorded.
  - In situ measurements conducted in grids 2 (grassland) and 5 (woodland) where applicable (ANPP, infiltration, earthworms).
  - Soil cores collected to 100 cm depth using multiple corer types; detailed field notes on hole depth, core length, and sampling slice depths.
  - Litter depth recorded; ANPP collected as fresh leaves for LDMC-based estimation; leaf samples processed for LDMC and used to predict ANPP via regression.

- Analytical methods and quality control
  - ANPP estimation via leaf dry matter content (LDMC) and cover-weighting; LDMC linked to species via databases (LEDa, ECeP) and regression model from Smart et al. 2017; uncertainty propagated through Bayesian methods (MCMC).
  - Soil hydraulic properties:
    - HYPROP-based water release curves (0–5 cm; 30–35 cm in some sites) analyzed with HYPROP-FIT; KW determined via HYPROP and mini-disk infiltrometer.
  - Soil sampling and processing:
    - Topsoil and subsoil slices (0–5, 5–15 or 15–60/50 cm, etc.) standardized; documentation of core lengths and depths.
    - Deep soil cores (0–100 cm) measured with Cobra, Split Tube Sampler, or Russian Auger depending on soil type; cores processed in labs (Bangor, Lancaster, Wallingford).
  - Physical and chemical soil analyses (core-derived samples):
    - Electrical conductivity (EC), pH in DIW and CaCl2, bulk density (BD), LOI, total C and N (Vario EL), total P, NO3-N, DOC, CEC, NH4-N, NO3-N, and related soil chemical properties.
    - Particle size distribution (PSD) by laser diffraction; aggregate size distribution (ASD); soil organic matter density fractions (LP-, OP-, MA- fractions) via density fractionation with sodium polytungstate (SPT).
    - Dissolved organic carbon (DOC) and related fractionation; enzymatic activities (phosphatase, β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phenol oxidase) where buffers were appropriate.
  - Biological and microbial analyses:
    - Extracellular enzyme activities assayed; microbial community profiling via amplicon sequencing (16S rRNA for bacteria, ITS2 for fungi) and metagenomics; data processed with DADA2, DIAMOND/SEAD, Krakken2 for taxonomic annotation; ordination analyses (metaMDS).
  - Earthworms:
    - Hand-sorted earthworms from soil blocks; species counts and fresh biomass recorded; standardized sorting times.
  - Data governance and QA:
    - UKCEH-accredited laboratories processed soils; internal standards, duplicates, and QA controls implemented; data linked via connector and location files to enable integration across datasets.

- Data structure and accessibility
  - Four primary data files with linking metadata:
    - SOC-D_DATABASE_CONNECTOR.csv: connects samples to site, plot, grid, core, layer, and spatial metadata.
    - SOC-D_DATABASE_LOCATIONS.csv: site coordinates and location IDs (OS grid references and lat/long).
    - SOC-D_DATABASE_ANPP.csv: ANPP estimates and LDMC-based model inputs.
    - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth measurements.
  - Additional soil datasets (common soil metrics, grid-specific metrics, topsoil/subsoil metrics, hydrology datasets, earthworm datasets) with explicit sample IDs (SAMPLE_ID) and linkage to connector file.
  - Microbial data (amplicon and metagenomes) and derived metrics included; ENA accession PRJEB66294 for raw sequences; derived community metrics included.
  - Data completeness and gaps documented; NA values used where data were not collected or not analysed (e.g., HYPROP cores at Alice Holt; some enzyme datasets unavailable for Gisburn due to buffer issue).

- Key findings and program context
  - SOC-D aims to test how biotic (soil biota, structure) and abiotic (climate, chemistry) controls influence SOC stability and dynamics.
  - Aims to identify UK regions and land-use scenarios most at risk of SOC loss and opportunities to enhance SOC through land management.
  - The project builds a modular, process-based SOC model intended for embedding in broader soil and ecosystem models.

- Data governance, access, and references
  - Outputs designed for reuse in monitoring frameworks and policy evaluation; clear metadata, sampling designs, and QA documentation accompany datasets.
  - Data are linked to national monitoring programmes (UKSCAPE, Countryside Survey, GMEP, ERAMMP) and are aligned with standard soil analysis protocols.
  - Acknowledgments to Forest Research for access and permissions; project funded under UK-SCAPE by NERC (NE/R016429/1).

- Supplemental material and project context
  - Supplement A: field maps and photos illustrating grassland-woodland contrasts and sampling points.
  - Supplement B: detailed coring and hole-depth data by site.
  - Supplement C: site-level table of potential measurements, rationale, and prioritization for future data collection and analyses.

- Practical implications for monitoring frameworks
  - Demonstrates integration of multi-omics (microbial), physical (soil structure and hydraulics), chemical (C, N, P, micronutrients), and biological (earthworms, enzymes) datasets across parallel land-use contrasts.
  - Provides a replicable field-to-lab workflow with standardized cores, QA controls, and metadata that can inform routine monitoring and cross-site comparisons.
  - Highlights data governance challenges and metadata needs, such as harmonizing depth increments, data sharing constraints, and site-specific measurement feasibility across a national-scale monitoring program.