# SOC-D: Soil Organic Carbon Dynamics data deposition

- Overview
  - Long-term study across five grassland-to-woodland contrasts in England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest) conducted 2018–2021.
  - Aims to understand biotic and abiotic controls on soil organic carbon (SOC) dynamics, identify UK regions at SOC risk, and develop a modular, process-based SOC dynamics model that can inform land management and policy.
  - Cohesive data package including aboveground productivity, detailed soil properties, soil hydraulic properties, earthworm communities, and microbial community data.

- Data content and datasets
  - Four main co-located datasets (collected at each site/plot): 
    - Aboveground net primary productivity (ANPP) and litter layer depth (0–5 cm for common measurements; contextual sampling across grids 2 and 5).
    - Comprehensive soil properties (chemical, physical, biological) for 0–100 cm across up to six depth increments (0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm; with site-specific variations).
    - Soil hydraulic properties (water release curves and unsaturated hydraulic conductivity; HYPROP-derived and field mini-disk infiltration measurements).
    - Earthworm counts and species composition (and biomass) from hand-sorted samples.
  - Additional datasets:
    - Soil organic matter density fractions (DOC, LP, OP, MA) and related C and N contents; dissolved inorganic components; cation exchange capacity; enzymatic activities (where available); microbial community data (amplicon sequencing for bacteria 16S and fungi ITS; metagenome sequencing).
    - Extensive metadata linking sample IDs to locations and sampling context.

- Data structure and connectivity
  - Two key linking files:
    - SOC-D_DATABASE_CONNECTOR.csv: links sample IDs to site, land use (grassland/woodland), grid, core, transition and lateral distances, slice/ depth, and location IDs.
    - SOC-D_DATABASE_LOCATIONS.csv: provides site-level coordinates and grid references.
  - Site-specific ANPP and litter depth data stored in dedicated CSVs, with linking via LOCATION_ID.
  - Soil metrics datasets (common soil metrics, grid2/grid5 grid-specific metrics, and top/bottom soil depths) and four HYPROP-related data files (raw and processed) are cross-referenced through SAMPLE_ID and LOCATION_ID.
  - Microbial sequencing data available as raw sequence archives in ENA (Project PRJEB66294) with derived metrics included (ordination scores, read counts, and pathway/functional annotations via SAMSA2/DIAMOND/kraken2 pipelines).
  - Data completeness varies by measurement type and site (e.g., HYPROP unavailable for Alice Holt; some extracellular enzyme data excluded from Gisburn due to buffer issues). Missing values are indicated as NA.

- Site selection, design, and sampling
  - Grassland-to-woodland contrasts selected to address planned SOC questions, with criteria covering woodland age, management history, plot size, and accessible sampling permissions.
  - Five contrasts/sites chosen for detailed sampling (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest); each site includes two plots (grassland and woodland) and six grids with 18 sampling locations per contrast.
  - Transect-based sampling along grassland-woodland boundary to capture edge effects; randomized points within grids with distance metrics to transition boundary and grid edges recorded.
  - Collection methods varied by site and depth:
    - HyPROP cores for 0–5 cm (and 30–35 cm at some sites) to derive water retention and hydraulic properties.
    - National survey-style cores for top 0–15 cm (0–15 cm).
    - Split Tube Sampler for 0–30 cm, Cobra precision corer for 0–100 cm (or 30–100 cm), and Russian auger for deeper increments (50–100 cm) depending on soil type.
    - In-field measurements: ANPP (via leaf dry matter content, LDMC, and calibration with dominance species), litter depth, and in-situ earthworm sampling in grids 2 and 5.
  - Depth slicing for laboratory analyses: 0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, and 50/60–100 cm; core processing and subsampling designed to support multiple analyses.

- Analytical methods and quality control
  - ANPP: derived from LDMC-based regression with species-level LDMC values; uncertainty propagated via MCMC-derived prediction intervals.
  - Soil properties (common & site-specific):
    - Bulk density (BD), field and laboratory water content, pH (DIW and CaCl2), electrical conductivity (EC), LOI via thermogravimetric analysis, total carbon and nitrogen (Elementar Vario EL), total phosphorus (H2O2/H2SO4 digestion), nitrate, dissolved organic carbon (DOC), and cation exchange capacity (CEC) with ICP-OES for cations.
    - Topsoil 0–15 cm and subsoil layers (15–50+ cm) characterized; depth increments and sample handling aligned with UK national datasets (Countryside Survey, GMEP, ERAMMP) and European LUCAS guidelines.
  - Soil physical-chemical and microbial fractions:
    - Particle size distribution (PSD) using laser diffraction; aggregate size distribution (ASD) and occluded organic matter; soil organic matter density fractions (LP, OP, MA) with density fractionation using sodium polytungstate (SPT).
    - Enzyme activities (phosphatase, β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phenol oxidase) where buffers and methodology allowed; cross-site comparability limited.
    - Microbial community analyses: amplicon sequencing (16S rRNA V4-V5; ITS2) and shotgun metagenomics; data processed to generate OTU/functional profiles and ordination scores (metaMDS).
  - Earthworm data: species counts and biomass from hand-sorted soil blocks; standardized sorting time and handling in-field and lab processing.
  - Data quality controls:
    - Internal standards, duplicates, and calibration checks for EC and pH.
    - QA/QC considerations for LOI, CEC, and multiple chemical analyses (matrix-matched standards, blanks, and reference materials).
    - Documentation of site-specific data issues (e.g., Gisburn buffer problem for enzymes; aerobic preservation challenges for microbial biomass).

- Project background and research questions
  - Central aim: to understand SOC dynamics through links between soil biota, soil structure, and soil chemistry; identify regions at risk of SOC loss and potential management levers to enhance SOC storage.
  - Four guiding questions:
    1) SOC sensitivity to climate and land management changes.
    2) Critical feedbacks among SOC, soil structure, chemistry, and functional biota.
    3) Soil metrics and modelling approaches that best reflect modern SOC dynamics.
    4) UK areas at risk of SOC loss and opportunities to protect/increase SOC.
  - The land management component focuses on the influence of grassland-to-woodland transitions as woodland creation expands under Net Zero policies; the aim is to assess how SOC responds to such transitions across UK soil-vegetation-climate combinations.

- Data availability, governance, and supplementary materials
  - Project funded under UK-SCAPE (NE/R016429/1); collaboration with UKCEH labs and partner sites.
  - Data and code: multiple datasets with cross-referencing connectors and location tables; sequencing data deposited in ENA (PRJEB66294); analyses supported by described software (HYPROP-FIT, R, DIAMOND, SAMSA2, Kraken2 pipelines).
  - Supplementary materials include field maps (Supplement A), detailed soil coring logs (Supplement B), and a Supplement C table outlining potential measurements, rationale, and prioritization.
  - Acknowledgements to Forest Research for access and permissions; provides a framework for integrating these data with broader long-term monitoring programs.

- Practical implications for data leaders
  - Comprehensive, multi-modal dataset enabling process-based SOC modelling across UK-relevant land-use gradients.
  - Clear data governance through connector/locations files to link disparate measurements and depths; explicit documentation of missing data and site-specific limitations.
  - Rich metadata and supplementary materials to support reproducibility, cross-site comparisons, and integration with national soil datasets.
  - Potential for leveraging the modular SOC-D model in policy planning and land-management decision-making, while maintaining attention to data quality and site-specific caveats.