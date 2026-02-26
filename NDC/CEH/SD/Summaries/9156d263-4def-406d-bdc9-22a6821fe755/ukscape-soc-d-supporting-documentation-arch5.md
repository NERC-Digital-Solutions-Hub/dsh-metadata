# Soil Organic Carbon Dynamics (SOC-D) dataset

- A multi-site dataset describing soil organic carbon (SOC) dynamics across five grassland-to-woodland contrasts in England (2018–2021), funded by UK-SCAPE and led by UKCEH.
- Aims to understand biotic and abiotic controls on SOC, identify UK areas at risk of SOC loss, and inform land-management policies to increase SOC storage.
- Includes rich, co-located measurements across aboveground and belowground components, with modular data products suitable for process-based modelling and integration with national soil datasets.

## Aims and scope for data stewardship

- Test the biological and structural controls on SOC stability and dynamics across key UK land-use combinations.
- Build a flexible, process-based SOC dynamics model that can be embedded in broader soil models.
- Provide a nationally relevant, openly accessible data resource linking field measurements to soil properties, enabling policy-relevant insights.

## Study design and objectives

- Location and contrasts: five long-term grassland-to-woodland contrasts across England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest).
- Sampling framework: two plots per site (grassland vs woodland), each plot subdivided into grids (1–3 grassland; 4–6 woodland); 18 sampling locations per site (2 plots × 9 locations).
- Temporal scope: soil cores collected 2018–2019; follow-up measurements (infiltration, ANPP, earthworms) 2020–2021.
- Core objective: quantify SOC dynamics across depth and site conditions, linking physical, chemical, and biological drivers.

## Datasets and content (data products)

- ANPP and litter depth (0–5 cm litter layer; grassland/woodland comparisons).
- Soil properties (0–100 cm, up to six depth increments): chemical, physical, and biological measurements.
- Soil hydraulic properties: soil water release curves (HYPROP) and unsaturated hydraulic conductivity (minidisk infiltrometer), plus HYPROP raw data (PF and water content) and derived K values.
- Earthworms: counts and biomass by species.
- Aboveground and belowground biological data: LDMC-derived ANPP; MOBI (soil microbial data) through metagenomics and amplicon sequencing (16S rRNA, ITS2) and shotgun metagenomics.
- Soil organic matter (SOM) fractionation: density fractionation into LP-fraction, OP-fraction, MA-fraction, plus dissolved organic carbon (DOC) and total N, with C and N contents for each fraction.
- Enzyme activities: EXO hydrolytic and oxidative enzymes (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) for select sites.
- Additional soil metrics: NO3-N, DOC, CEC, base cations (Ca, Mg, K, Na), pH (DIW and CaCl2), bulk density, LOI, SWC, PSD (laser diffraction), particle-size distributions, aggregate size distributions, and SOM-related metrics.
- Data structure and connectivity: co-located datasets linked via sample and location identifiers; connectors and locations files enabling cross-dataset joins.

## Data structure and connectivity

- Two main linking files accompany datasets:
  - SOC-D_DATABASE_CONNECTOR.csv: connects sample IDs to site, plot, grid, core, depth slice, and location geometry, including distances to transition boundary and grid edges.
  - SOC-D_DATABASE_LOCATIONS.csv: site-level coordinates, grid references, and latitude/longitude data.
- Datasets are organized by content (e.g., ANPP, LITTER_DEPTH, COMMON_SOIL_METRICS, SOIL_METRICS_GRID2_GRID5, HYPROP-related files, EARTHWORMS, sequencing outputs).
- Additional soil-depth-resolved data are provided for topsoil (0–15 cm) and deeper increments (0–100 cm), with five depth increments for core slicing.
- Metadata and data dictionaries are included; NA values indicate missing data.
- The European Nucleotide Archive (ENA) accession PRJEB66294 hosts raw sequencing data (16S rRNA, ITS, and shotgun metagenomics), with derived metrics provided in the associated CSV files.

## Collection methods and measurement details

- Field design: homogenous fields were selected per site, with sampling along transects that run from grassland to woodland to capture edge and proximity effects.
- Core sampling and corers:
  - Hyprop cores for soil water release curves (0–5 cm; 30–35 cm at some sites).
  - National survey style cores (0–15 cm) to assess topsoil carbon and compaction effects.
  - Split Tube Sampler (0–30 cm) and Cobra precision corer (0–100 cm or 30–100 cm) for deep profiling.
  - Russian auger for peat or water-saturated segments (0–50 and 50–100 cm).
- Depth increments: topsoil defined as 0–5 cm or 0–15 cm (site-dependent), then 15–30 cm and 30–50/60 cm, with 50/60–100 cm as deeper increments.
- ANPP and LDMC: leaf material collected seasonally (May–July 2021) from dominant species; leaf dry matter content used to predict ANPP via regression.
- Infiltration and hydraulic measurements: in-situ infiltration (grids 2 and 5) and HYPROP lab analyses; field Kfs measured with mini-disk infiltrometer at specified tensions.
- Earthworms: hand sorting of soil blocks (25 cm × 25 cm × 25 cm depth) with standardized 15-minute sorting; field and lab handling and weighing.
- Litter depth: measured at three points around each sampling location.
- Microbial metrics: DNA extraction from soil for amplicon sequencing (16S V4-V5; ITS2) and metagenomics; sequencing performed with Illumina MiSeq (amplicons) and Novaseq (metagenomics); data processed with DADA2 for OTUs, Kraken2 for taxonomic annotation, and downstream ordination (metaMDS).
- Enzymes and CUE: potential analyses for extracellular enzyme activities and microbial carbon use efficiency were considered but microbial biomass and CUE measurements encountered reliability issues due to sample handling (freezing compromised results).

## Data processing, quality control, and limitations

- Quality control across labs and instruments:
  - Regular use of internal standards and duplicates for EC, pH (DIW and CaCl2), LOI, and other chemical measurements.
  - UKCEH SOP-based analyses (e.g., SOP3102 for C and N; ICP-OES for cations).
  - LOI validation via internal standards and batch replication checks; calibration and instrument maintenance documented.
- Analytical workflows:
  - ANPP derived from LDMC using regression models; uncertainty propagated via MCMC posterior distributions.
  - HYPROP and Kfs data processed with HYPROP-FIT software; Kfs derived from field measurements.
  - PSD measured by laser diffraction; cross-validated with sieve-derived sand fraction and internal standards.
  - SOM density fractions (LP/OP/MA) extracted using sodium polytungstate, with batch QA and duplicate checks.
- Data gaps and site-specific notes:
  - Some measurements missing or limited to certain depths or grids (e.g., HYPROP absence at Alice Holt; certain enzyme data excluded from Gisburn due to buffer issues).
  - Topsoil depth increments adjusted (0–5 cm vs 0–15 cm) to balance sample mass and analytical viability.
  - Microbial biomass and CUE measurements affected by freezing; results deemed unreliable.
- Data governance:
  - Clear identifiers for site, plot, grid, core, and layer ensure traceability.
  - Supplementary materials (A–C) provide field field sheets, coring logs, and measurement planning details to support reproducibility.

## Practical access, reuse, and citation

- Data deposition format includes multiple CSV files with explicit schema for cross-linking sample IDs, locations, and measurements.
- Raw sequencing data available in ENA under PRJEB66294; derived data and measurement tables are provided in accompanying SOC-D_* CSV files.
- Acknowledgment of project partners and permissions (e.g., Forest Research) and explicit references to SOPs and methodological literature for proper reuse.

## Supplementary materials and documentation

- Supplement A: Field-site maps and photos illustrating grassland-to-woodland contrasts and sampling layouts.
- Supplement B: Detailed soil coring logs and hole-depth records per site.
- Supplement C: A measurement prioritization table outlining planned soil and ecosystem measurements, rationale, and analysis approaches.

## Key governance and stewardship takeaways

- Robust linking structure (CONNECTOR and LOCATIONS) enables precise data integration across datasets, supporting reproducible analyses and provenance tracking.
- Comprehensive metadata and method documentation accompany the data to facilitate reuse, interpretability, and cross-study comparability.
- Documented quality control procedures and site-specific caveats help users assess uncertainty and data suitability for SOC modelling and policy-relevant insights.
- While most core measurements are complete and well-documented, certain high-cost or site-specific measurements are incomplete or excluded in places; users should consult Supplementary materials and method sections when aggregating across sites.