# Soil Organic Carbon Dynamics (SOC-D) dataset description

- Scope and purpose
  - Describes co-located aboveground and belowground measurements from five grassland-to-woodland contrasts across England (2018–2021) as part of the UK-SCAPE SOC-D project.
  - Aims to understand biotic and abiotic controls on soil organic carbon (SOC) dynamics and to identify where UK SOC stocks are at risk and how management could enhance SOC storage.
  - Data are intended to support process-based modelling of SOC dynamics and integration with national soil monitoring and other environmental datasets.

- Study design and site information
  - Five land-use contrasts: Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest.
  - Each site comprises a grassland plot and a woodland plot (two plots per site) with nine sampling locations per plot arranged in grids (1–3 in grassland, 4–6 in woodland); a 5-site, 2-plot-per-site, 18 sampling locations per site design.
  - Sampling occurred between Nov 2018 and Mar 2019 (soil cores) with additional measurements (infiltration, earthworms, ANPP) in 2020–2021.
  - Soil cores collected to 100 cm depth with up to six depth increments: 0–5, 5–15, 15–30, 30–50/60, and 50/60–100 cm (top layer sometimes split into 0–5 and 5–15 cm depending on site). Additional top/bottom layer measurements performed at specific grids/sites.
  - Field data complemented by site-level metadata (location coordinates, grid references, transect layout, distance to transition boundary).

- Data components (datasets)
  - ANPP and litter depth
    - Aboveground net primary productivity (ANPP) estimates using cover-weighted leaf dry matter content (LDMC) with regression-based prediction; LDMC values linked to dominant species.
    - Litter depth measured at three points per sampling location.
  - Soil physical, chemical, and biological properties (0–1 m)
    - Measured properties include bulk density, pH, EC, LOI, total C and N, total P, NO3-N, DOC, CEC, cations (Ca, Mg, K, Na), SWC, PSD, textures, aggregates, and density fractions (LP, OP, MA) with DOC and DOM considerations.
    - Density fractionation yields LP-, OP-, MA-fractions plus DOM; C and N analyzed by elemental analyser; N–P–S data via standard colourimetric methods; ENZYME activities measured for select sites.
  - Soil hydraulic properties and infiltration
    - HYPROP-derived soil water release curves (0–5 cm; 30–35 cm at selected sites), unsaturated hydraulic conductivity (K) via mini-disk infiltrometer.
    - HYPROP raw data (PF, water content) and derived conductivity data (K at various tensions) provided.
  - Earthworms
    - Counts and species identification with fresh biomass for a range of earthworm taxa; weight data available for several taxa.
  - Microbial communities
    - DNA/RNA-based analyses including amplicon sequencing (16S rRNA for bacteria, ITS for fungi) and metagenomics.
    - Derived metrics include NMDS axes and microbial biomass proxies; Kraken2/taxonomic annotations and SAMSA2-based functional annotations provided.
  - Additional soil fractions and enzymes (where available)
    - SOM density fractionation (LP, OP, MA fractions) with carbon and nitrogen content; DOM measurements; extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) for select sites (Alice Holt, Wytham, Kielder).
  - Supplementary connectivity data
    - Data connectors (SOC-D_DATABASE_CONNECTOR.csv) and SITE LOCATIONS (SOC-D_DATABASE_LOCATIONS.csv) enable linking of all measurements to sampling locations, plots, grids, and site coordinates.
  - Data file structure and links
    - Four main data groups plus supplementary materials:
      - ANPP and LITTER_DEPTH CSVs with linking identifiers.
      - COMMON_SOIL_METRICS, SOIL_METRICS_GRID2_GRID5, SOIL_HYDRAULIC_CONDUCTIVITY, HYPROP/CONDUCTIVITY, EARTHWORMS, and microbial/metagenomic data files.
      - Topsoil and subsoil metrics files (0–15 cm topsoil; 15–60 cm subsoil increments) and full 0–100 cm core data flow.
    - Sequencing data deposited in ENA under project PRJEB66294; derived sequence metrics provided in corresponding CSVs.
    - Missing values are represented as NA; data are designed to be joined via sample IDs (SAMPLE_ID) and LOCATION_ID.

- Data collection methods and quality control
  - Field methods
    - Grassland-to-woodland contrasts sampled along transects with randomized field points; 5 sampling points per grid chosen based on environmental constraints (e.g., distance to trees, slope).
    - Multiple corer types used to obtain cores: Hyprop, national-survey style, Split Tube, Cobra precision, and Russian auger; depth increments recorded; litter depth and ANPP sampled in grids 2 and 5.
  - Laboratory analyses
    - ANPP estimated from LDMC-based regression; LDMC values drawn from observed species or trait databases (LEDA, ECPE).
    - LOI and SOC measured by elemental analysis and TGA; CEC measured via ammonium acetate extraction and ICP-OES; NO3-N, DOC measured with standard colorimetric and spectrophotometric methods; P via acid digestion and colorimetry.
    - PSD and ASD measured by laser diffraction after digestion; calibration and reproducibility checks with standards and replicates.
    - SOM density fractionation performed with sodium polytungstate to separate LP, OP, MA fractions; COD/N ratios reported for each fraction; total C and N measured for each fraction.
    - Enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) measured using fluorometric or spectrophotometric assays; samples stored at -20°C prior to analysis; QC includes blanks and standards.
    - Hydraulics: HYPROP data analyzed with HYPROP-FIT; additional field K measurements with mini-disk infiltrometer; calibration and standard procedures followed; instrument-specific manuals cited.
  - Biological analyses
    - Microbial community profiling via 16S rRNA (bacteria) and ITS (fungi) amplicon sequencing following Earth Microbiome Project protocols; metagenomic sequencing performed with Illumina Novoseq; reads processed with DADA2 or standard pipelines; ordination and diversity metrics included.
  - Data provenance and QA
    - UKCEH laboratories (Bangor, Lancaster, Wallingford) handled soil processing and QA; internal standards, duplicates, and SOP-based QC applied; dating and core lengths recorded to assess compaction and sampling integrity; some site-specific data omitted due to quality or methodological issues (e.g., Gisburn enzyme data excluded due to buffer mismatch; microbial biomass data compromised by freeze-thaw).

- Data structure, linking, and accessibility
  - Central data model
    - Two main connector tables at the core: SOC-D_DATABASE_CONNECTOR.csv (experimental layout: site, land use, plot, grid, core, transition distances, lateral distances, slice, lab layer, location and sample IDs) and SOC-D_DATABASE_LOCATIONS.csv (location coordinates and grid references).
    - Four primary data groupings aligned to the project’s four scientific objectives (ANPP, litter depth; soil physical/chemical/biological properties; soil hydraulic properties; earthworms; microbial data), plus supplementary soil fractions and enzyme data.
  - Data integration
    - Sample-level data linked to site and sampling location via LOCATION_ID; cross-dataset joins enabled by SAMPLE_ID and CORE-LAYER identifiers.
    - Datasets include NA values where measurements were not collected or data failed QC; ENA sequence data linked via project accession.
  - Data availability and rights
    - Datasets are deposited with UKCEH for long-term access and reuse; sequencing data publicly available via ENA; accompanying metadata (locations and connectors) provided to enable data discovery and reuse.
  - Documentation and references
    - Supplementary materials (A, B, C) detail field logistics, coring information, and measurement considerations; project references and supplementary methods provide traceability for methods and QA procedures.

- Key considerations for data stewardship
  - Data completeness and gaps
    - Most common soil measurements are complete; several expensive or less-used measurements are missing in certain grids or sites (e.g., HYPROP at Alice Holt; some enzyme data removed due to buffering issues at Gisburn; microbial biomass measurements affected by sample handling).
  - Data standardization and interoperability
    - Consistent depth increments and lab methods across sites where possible; explicit documentation for depth definitions and cutting points to align with UK national soil datasets (0–15 cm vs 0–5 and 15–60 cm adjustments as needed).
  - Provenance and traceability
    - Clear chain from field sampling to lab processing; core lengths and hole depths recorded; QA protocols documented; data connected via the SOC-D connectors and locations files.
  - Data governance and use
    - Data suitable for cross-site SOC dynamics analyses, model development, and benchmarking of SOC responses to land-use change; sequence data enable microbial community and functional analyses; data are ready for integration into larger environmental data infrastructures.
  - caveats and constraints
    - Some measurements are site- or grid-specific; cross-site comparability for enzyme activities may be limited due to buffer issues; certain data (e.g., microbial biomass) affected by sample handling; LOI and COD-derived metrics rely on standardized TXA/TGA protocols with QA controls.

- References and project context
  - Project: UK-SCAPE program, SOC-D (Grant NE/R016429/1); aims to test paradigms of SOC dynamics across UK land-use/soil types.
  - Data sources and standard references include: ANPP/SLA/LDMC relationships; HYPROP manuals; standard soil analytical methods; Earth Microbiome Project protocols; ENA accession PRJEB66294 for sequence data.

- Additional notes for users
  - Use the CONNECTOR and LOCATIONS files to assemble site-level datasets; align grid and core identifiers to retrieve corresponding measurements across the four data groups.
  - Consult Supplement A–C for field, lab, and measurement nuances; reference SOP3102 for soil carbon and total nutrient analyses; observe site-specific caveats when comparing enzyme activities and microbial metrics across contrasts.