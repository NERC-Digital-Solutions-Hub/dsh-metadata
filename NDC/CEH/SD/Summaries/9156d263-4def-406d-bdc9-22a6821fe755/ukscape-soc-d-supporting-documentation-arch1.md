# Soil Organic Carbon Dynamics (SOC-D) Data Description

- Aim and scope
  - Understand physical, chemical, and biological controls on soil organic carbon (SOC) dynamics.
  - Identify where UK soil carbon stocks are at risk and opportunities to increase SOC through land management.
  - Test the role of biotic (soil biota) and abiotic (soil structure, chemistry, climate) interactions in SOC stability.
  - Develop process-based tools/models that can be embedded into broader soil models.

- Key datasets (four main data groups)
  - Aboveground measurements: Aboveground net primary productivity (ANPP) and litter layer depth.
  - Soil properties: Chemical, physical, and biological properties for up to six soil layers from 0 to 100 cm.
  - Soil hydraulics: Soil water release curves and unsaturated hydraulic conductivity (K).
  - Earthworms: Counts and species IDs with biomass data.
  - Additional linking data: Metadata and sample/location connectors to enable data integration across all four datasets.

- Study design and sites
  - Five grassland-to-woodland contrasts across England: Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest.
  - Selection criteria prioritized mature, well-documented land-use histories, adequate plot sizes (40–75 m), accessible transects, and sampling permissions.
  - Each site includes two plots (grassland and woodland) with nine sampling locations per plot (18 per contrast).
  - Transect-based sampling with grids (1–3 in grassland; 4–6 in woodland) to capture spatial gradients near the land-use boundary.

- Timeline and field sampling
  - Field cores collected between November 2018 and March 2019; additional measurements conducted 2020–2021.
  - In situ measurements at grids 2 (grassland) and 5 (woodland) for ANPP, infiltration, and earthworms; litter depth measured around sampling points.
  - Core sampling depths: 0–5 cm, 5–15 cm, 15–30 cm, 30–50 cm, 50–60 cm, up to 100 cm (with site- and depth-specific increments).

- Collection methods (soil cores and related measurements)
  - Hyprop cores for 0–5 cm (and 30–35 cm where feasible) to derive water release curves.
  - National survey-style 0–15 cm cores for topsoil compaction studies.
  - Split Tube Sampler (0–30 cm) and Cobra precision corer (0–100 cm) for deep cores; Russian auger used for peat/wet soils.
  - Infiltration and earthworm sampling conducted in select grids; litter depth recorded at three points per sampling location.

- Aboveground productivity and leaf traits
  - ANPP estimates derived from leaf LDMC (cover-weighted LDMC; cLDMC) and a regression model (Smart et al. 2017).
  - LDMC and LDMC-derived ANPP values linked to species-level trait databases (LEDA, ECPE).

- Soil hydraulic measurements and analysis
  - HYPROP measurements to generate soil water release curves; HYPROP-FIT used for curve fitting.
  - Unsaturated hydraulic conductivity (K) measured with mini-disk infiltrometers at various suctions (grids 2 and 5).

- Earthworms
  - Hand-sorted earthworms from 25 cm x 25 cm soil blocks (to 25 cm depth); specimens weighed and identified to species; field sorting limited to 15 minutes per sample.

- Soil chemical, physical, and biological properties
  - Core-sliced soil samples (0–5, 5–15, 15–30, 30–50/60, 50–100 cm) processed in UKCEH labs.
  - Key measurements include: field water content, bulk density, pH (DIW and CaCl2), electrical conductivity (EC), LOI, total C and N, total P, nitrate-N (NO3-N), DOC, CEC, and various forms of soil fractions and aggregates.
  - Particle size distribution (PSD) by laser diffraction; textural fractions (<2 µm, 2–63 µm, >63 µm; also <53 µm for literature compatibility).
  - Density fractionation to separate dissolved organic carbon (DOC), light fractions (LP), occluded particulate (OP), and mineral-associated (MA) fractions; C and N contents measured for each fraction.
  - Extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, and phenol oxidase) at select sites (Alice Holt, Wytham, Kielder); data cross-site comparability limited by buffer issues at Gisburn.
  - Soil microbial communities: 16S rRNA (bacteria) and ITS2 (fungi) amplicon sequencing; metagenomes; data processed for ordination (e.g., NMDS) and community composition ratios (fungi:bacteria).

- Data structure and linking
  - SOC-D_DATABASE_CONNECTOR.csv: links sample IDs to site, plot, grid, core, transition distances, lateral distances, and sample IDs.
  - SOC-D_DATABASE_LOCATIONS.csv: site and sampling location coordinates (OS grid references, lat/long).
  - Datasets with ANPP, litter depth, common soil metrics, grid2/grid5 soil metrics, hydraulic conductivity, HYPROP data, earthworm data, and sequencing/metagenomics data are designed to be joined via LOCATION_ID/SAMPLE_ID.
  - Missing values are represented as NA.

- Data availability and sequencing
  - Microbial sequencing data deposited in ENA under PRJEB66294; derived metrics included (e.g., NMDS axes, functional gene abundances, and reads-per-category).
  - Related processing scripts and models described (e.g., Bayesian regression for ANPP, LDMC-based predictions) and available in project materials.

- Quality assurance and limitations
  - Quality control measures include internal standards, duplicates, blanks, calibration checks, and standard operating procedures (SOPs).
  - Some site-specific data issues:
    - Extracellular enzyme data excluded from Gisburn due to buffer mismatch.
    - Microbial biomass data affected by freezing; some biomass measurements deemed unreliable.
    - Not all measurements were collected at every site (e.g., certain HYPROP cores not collected at Alice Holt; some topsoil properties limited to top/bottom increments).
  - Documentation and supplementary materials (A–C) provide field mapping, coring details, and measurement rationales.

- Context and related projects
  - SOC-D is a UK-SCAPE programme initiative (grant NE/R016429/1) aiming to deliver a modular, process-based SOC dynamics model.
  - Linked projects and data streams: ELUM, GMEP, UGRASS, ERAMMP; supplementary site mapping and soil data resources are provided.
  - Acknowledgements note collaboration with Forest Research and access at Alice Holt and Kielder Forest.

- Practical use for analysts
  - Enables cross-site, depth-resolved analyses of SOC drivers by integrating soil physics, chemistry, biology, plant productivity, and soil fauna data.
  - Supports correlation analyses between SOC dynamics and factors such as soil texture, structure, CEC, SOM fractions, root and litter inputs, and microbial/enzymatic activity.
  - Provides opportunities to develop and test predictive, process-based SOC models across UK land-use contrasts (grassland vs woodland) and soil types.
  - Rich metadata and connectors facilitate reproducible analyses and data discoverability.