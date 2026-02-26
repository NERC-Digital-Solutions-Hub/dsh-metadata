# Soil Organic Carbon Dynamics (SOC-D)

## Purpose and relevance for Data Stewards
- Ensure datasets are governed with clear metadata, provenance, and standards to support discoverability, reuse, and updating.
- Maintain data quality across multiple sites, instruments, and analyses; document data lineage and processing steps.
- Align with repository and data-sharing practices; manage access controls, embargoes, and updates; document any limitations or missing data (NA).
- Provide guidance on dataset interdependencies (ground-truth measurements, lab analyses, and bioinformatic outputs) to support reproducibility and interoperability.

## Dataset scope and structure (what’s in scope for reuse)
- Five long-term grassland-to-woodland contrasts across England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest) collected 2018–2021.
- Four main data themes, each published as dedicated data files, plus connecting location and sample metadata:
  - Aboveground net primary productivity (ANPP) and litter layer depth.
  - Soil physical, chemical, and biological properties across up to six 0–100 cm soil layers.
  - Soil hydraulic properties (water release curves, unsaturated hydraulic conductivity).
  - Earthworm counts and species identification (biomass and counts).
- Additional datasets and analyses include: soil organic carbon dynamics context, microbial community sequencing (bacteria and fungi) and metagenomes, density fractionation of soil organic matter, enzyme activities, and detailed metadata connectors.
- Data are linked through:
  - SOC-D_DATABASE_CONNECTOR.csv (experimental layout and sample linking)
  - SOC-D_DATABASE_LOCATIONS.csv (site/location coordinates and grid references)
  - Datasets for ANPP, litter depth, soil metrics (common and top/sub soil), hydraulic data, earthworms, and microbial data
- Raw sequence data archived in ENA (PRJEB66294) with derived metrics provided.

## Sampling design and collection methods (high-level for governance and reproducibility)
- Sites represent grassland-to-woodland contrasts sampled along transects to capture edge effects; grids 1–3 in grassland and 4–6 in woodland; 18 sampling locations per contrast (3 per grid, across 2 plots).
- Measurements taken in grids 2 (grassland) and 5 (woodland) where in-situ ANPP, infiltration, and earthworms were collected; 0–5 cm samples (and deeper where applicable) for soil analyses.
- Core sampling and depths:
  - Deep 0–100 cm soil cores (mineral and peat soils) using Cobra precision corer, Split Tube Sampler, and Russian Auger as site-specific practices.
  - Additional topsoil sampling (0–15 cm, occasionally 0–5 cm) using national survey cores for comparison of carbon stocks and compaction effects.
  - HYPROP cores (0–5 cm; 30–35 cm at some sites) for water retention curves; unsaturated hydraulic conductivity measured with a mini-disk infiltrometer in the field.
- Aboveground measurements and litter:
  - ANPP estimated from leaf dry matter content (LDMC) using cover-weighted LDMC and species-specific LDMC values; 2021 field sampling in grids 2 and 5.
  - Litter depth measured at three points around each sampling location.
- Earthworms:
  - Hand-sorted sampling (25 cm x 25 cm x 25 cm blocks; 15-minute sorting) with specimens collected and weighed in the field and lab.
- Laboratory analyses (soil and biological materials):
  - Standard soil metrics: moisture content, EC, pH (DIW and CaCl2), bulk density, LOI, total C and N, P, NO3-N, DOC, CEC, and other soil chemistry.
  - Physical/inorganic: particle size distribution (PSD) via laser diffraction; aggregate size distribution (ASD); soil texture fractions (<2 μm, 2–63 μm, >63 μm; also <53 μm).
  - Soil organic matter fractions via density fractionation into DOC, LP (light particulate), OP (occluded particulate), MA (mineral-associated); associated C and N quantifications; C:N ratios for each fraction.
  - Enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) in select sites (Alice Holt, Wytham Woods, Kielder Forest).
  - Microbial community analyses:
    - Amplicon sequencing (16S rRNA for bacteria; ITS2 for fungi) and metagenomics (shotgun sequencing) with downstream OTU/ASV and functional profiling.
- Data processing and QA:
  - ANPP regression-based estimation with credible intervals via MCMC; LDMC-based predictions; linked to field observations.
  - HYPROP data analyzed with HYPROP-FIT software to derive water retention curves and hydraulic properties.
  - QA measures include instrument calibration, use of internal standards, duplicates, blanks, and site-specific QA notes (e.g., Gisburn enzyme data excluded due to buffer issue).
  - Microbial biomass and enzyme data sensitive to sample handling; freezing can affect results; such data treated accordingly in QA and interpretation.
- Data completeness and gaps:
  - Completeness varies by measurement; some molecules/parameters are only measured in specific layers or sites (e.g., HYPROP core availability, specific soil fractions, top vs. subsoil distinctions).
  - Missing values are indicated as NA in the datasets.

## Data quality, provenance, and processing notes (for data governance)
- Documented field methods, core types, depths, and transect design; detailed Supplement A–C provide site-specific field sheets, core depth logs, and measurement rationales.
- Metadata connectors enable reproducible cross-dataset joins (sample IDs, location IDs, grid references, site names).
- Data processing standards referenced (e.g., SOP3102 for carbon/nitrogen analyses; UKAS QA for lab measurements); quality control measures include duplicates, blanks, reference materials, and calibration checks.
- Data limitations:
  - Some datasets are site-specific and not directly comparable across sites due to buffer/buffer-type issues (e.g., wrong buffer used in Gisburn enzyme data; selective site exclusions).
  - Microbial biomass and enzyme results can be impacted by storage conditions (e.g., freezing) and thus are treated as partial or context-limited data.
- Raw data and derived metrics are provided, with documentation on how to reproduce transformations (e.g., ANPP predictions via LDMC, metagenome/OTU processing pipelines).

## Practical uses and reusability (for data stewards and data users)
- Enables cross-site comparisons of SOC dynamics under different land uses (grassland vs woodland) and across soil depths (0–100 cm) and soil types (mineral vs peat).
- Supports process-based understanding of SOC stability, relationships with soil structure, biology, and chemistry, and tests of SOC models under UK landscape conditions.
- Data are linked via structured identifiers (LOCATION_ID, SITE_NAME, GRID, PLOT, CORE, SAMPLE_ID) to support reproducible analyses and integration with other UKCEH programmes.
- Additional data types (ancillary soil metrics, hyporheic-like proxies, enzyme activities, and microbial communities) enable multifactorial analyses of SOC drivers and soil health.
- Data deposited in established repositories; sequence data in ENA; supports transparent traceability and future data reuse.

## Supplementary materials and data access notes (for governance and transparency)
- Supplements include field sheets and site-specific coring information (Supplement A and B) and a detailed supplement (Supplement C) outlining measurement prioritization and analysis plans.
- Location and experimental layout metadata are available to facilitate data discovery and cross-dataset linkage.
- Data are prepared for cross-disciplinary reuse while clearly marking site-specific caveats and data gaps.
- The project is part of the UK-SCAPE programme (funded by NERC) with collaborative support from Forest Research and affiliated UKCEH laboratories.

## Data management and contact (high-level)
- Managed by the SOC-D team within UKCEH; documentation provides dataset-level descriptions, data-file-specific schemas, and guidelines for linking datasets.
- For reuse or access inquiries, refer to the SOC-D management team and the linked project documentation (UGRASS, ELUM, GMEP, ERAMMP).