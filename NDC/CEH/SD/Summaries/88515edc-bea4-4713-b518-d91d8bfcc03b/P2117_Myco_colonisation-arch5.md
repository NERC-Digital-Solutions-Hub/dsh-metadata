# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks

## Overview
- Describes data from the NERC Soil Biodiversity Thematic Programme focusing on nitrogen and phosphorus dynamics in arbuscular mycorrhizal (AM) networks within grassland.
- Two related experiments using core-based systems to study AM colonisation and nutrient transfer between soil and plants.
- Data support functional studies of AM mycelia in soil and their role in carbon and nutrient cycles.

## Context and Site Details
- Programme (1999) studied soil biodiversity and ecosystem processes at Sourhope, Scotland (NGR NT 8545019630).
- Site features: grassland turf with high plant species richness; 24 higher-plant species, 21 forming AM, soil pH 4.5–5.0, organic C ~25%.
- Experimental setup used large intact monoliths removed from Sourhope plots and installed in controlled conditions at the University of Sheffield.

## Data Content and Structure
- Three comma-separated values (CSV) files provided:
  - Dataset 1077: P2117_MYCORRHIZAL_COL_BIO_1.csv
    - Content: Mycorrhizal colonisation of Agrostis capillaris bioassay plants; shoot N and P; root colonisation metrics; sampling date; block; treatment; and related measurements.
    - Key fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, TREATMENT, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES.
    - Units provided; missing values coded as null.
  - Dataset 1078: P2117_MYCORRHIZAL_COL_BIO_2.csv
    - Content: Mycorrhizal colonisation of Trifolium repens roots; shoot N and P; core area; and related AM indicators.
    - Key fields include AREA, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES.
    - Missing values coded as -999.
  - Dataset 1079 (implicit label in text): P2117_PLANT_UPTAKE_PHOS_33.csv
    - Content: Measurement of plant uptake of phosphorus-33 (33P) via AM networks; includes MESH_CORE (static/rotated), DAYS_POST_LABEL, PME (phosphomonoesterase), and related measurements.
    - Data structured to track 33P uptake over multiple harvests and core rotation conditions.
- Data provenance: linked to Sourhope field data and related publications; dataset notes reference SOURHOPE FIELD DATA HANDBOOK 2003 and related methodological papers.

## Experimental Design and Methods (for context)
- Experiment 1: Hyphal severance effects on AM colonisation
  - 42 cores (28 with mesh barriers, 14 solid); bait plants (Trifolium repens) in half the cores.
  - Rotated and static core sets to assess hyphal penetration; 10-week endpoint with root staining and microscopy for colonisation; N and P content analysed in shoots.
- Experiment 2: Hyphal severance and 33P transfer
  - Plant-free soil cores were introduced into pots; after AM in-growth, cores were labeled with 33P.
  - Some cores rotated to disrupt hyphal connections; multiple harvests up to 201 days with P uptake and PME measurements.
- Analyses include: root colonisation (McGonigle et al. method), total N and P in shoots, 33P in shoots and soils, and biocontrol measures (e.g., hyphal lengths).

## Metadata, Standards, and Value for Data Stewards
- Metadata elements covered in datasets: SAMPLE_ID, sampling date, block/area, treatment, root colonisation metrics, shoot N and P concentrations and contents, arbuscule/vesicle presence, mesh/core status, and days post label.
- Units and data types clearly specified for each field; explicit conventions for missing values (null or -999).
- Data quality controls: numeric range checks, format validation, and logical integrity checks described; however, the Australian programme disclaims accuracy and liability, clarifying data are provided without warranty.
- Data access and provenance notes:
  - Datasets available as Supporting Information via the EIDC catalogue record.
  - Ties to published literature and data handbooks for traceability.
- Practical considerations for reuse:
  - Clear documentation of core design, AM inoculation context, and measurement methods to enable proper interpretation and cross-study integration.
  - Availability of standardized fields supports integration with other soil biota and nutrient cycling datasets.

## Practical Challenges and Considerations for Data Governance
- Complex experimental design with multiple cores, rotations, and treatments requiring careful metadata capture to maintain interpretability across studies.
- Heterogeneous data formats and historical conventions (e.g., different missing value codes) necessitate harmonization for long-term preservation.
- Potential gaps in user needs or discovery due to specialized AM network measurements; dataset documentation helps mitigate incomplete understandings.

## Limitations and Legal/Usage Notes
- QA steps performed, but data providers do not guarantee accuracy or fitness for a particular use.
- Provision of data carries no liability for inaccuracies or damages arising from use.
- Users should consult the linked methodological references and field data handbooks for full context.

## Governance Recommendations for Data Stewards
- Maintain consistent metadata schemas across all three datasets, including explicit units, data types, and value ranges.
- Preserve original missing value conventions but consider adopting a unified standard (e.g., standardized null codes) for interoperability.
- Link datasets to persistent identifiers and associated publications to enhance discoverability and provenance.
- Document data lineage, processing steps, and any transformations to support reproducibility.
- Ensure clear licensing and liability statements are retained, and provide guidance on appropriate use and attribution.