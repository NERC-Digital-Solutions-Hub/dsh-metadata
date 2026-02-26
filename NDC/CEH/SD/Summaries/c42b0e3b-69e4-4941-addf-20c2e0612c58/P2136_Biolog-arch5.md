# Substrate utilisation profiles and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland [NERC Soil Biodiversity Programme] - Supporting Information

## Overview
- Documentation for soil bacterial community ecology data collected during the NERC Soil Biodiversity Thematic Programme at Sourhope, Scottish Borders (1999–2000).
- Aims to understand how soil biota diversity and functional roles influence ecological processes in semi-natural upland grassland.
- Data accompany 24 related research projects; this item provides methodological details, data structure, and references.

## Datasets and content
- Two CSV data files:
  - BIOLOG_GN substrate utilisation data: P2136_Biolog_Utilisation.csv
    - Records substrate utilisation (1/0) across BIOLOG-GN wells for multiple cores, depths, and sampling dates.
    - Key fields: SAMPLING_DATE, MAX_DEPTH (cm), BIOLOG_CELL, SUBSTRATE, SUBSTRATE_TYPE, UTILISATION.
  - Soil moisture data: P2136_Soil_Moisture.csv
    - Means of moisture content across replicate cores for each sampling date and depth.
    - Key fields: SAMPLING_DATE, MAX_DEPTH (cm), PERCENTAGE_MOISTURE.
- Metadata and data structure details:
  - Sampling dates: multiple dates in 1999–2000 (three replicates 0–5 cm, 5–10 cm, 10–15 cm, 15–20 cm slices per date).
  - Depths: cores separated into four 5 cm increments (0–5, 5–10, 10–15, 15–20 cm).
  - SITE: Sourhope field site, control plot; grid ref NT854196; soil: shallow organic-rich brown forest soil on glacial till.
  - Biological analyses: BIOLOG-GN plates incubated at 18°C; colour development scored as presence/absence.
  - Moisture: determined by oven-drying three replicate cores at 105°C for 24 hours.
- Data provenance and usage notes:
  - Background literature and related datasets referenced (SOURHOPE FIELD DATA HANDBOOK 2003; FEMS Microbiology Ecology 2003; Applied Soil Ecology 2006).
  - Supporting information accessible via EIDC catalogue record (link provided) and published papers with DOIs.

## Data structure and metadata
- BIOLOG_GN data
  - Columns include: SAMPLING_DATE, MAX_DEPTH (cm), BIOLOG_CELL, SUBSTRATE, SUBSTRATE_TYPE, UTILISATION (0/1).
- Soil moisture data
  - Columns include: SAMPLING_DATE, MAX_DEPTH (cm), PERCENTAGE_MOISTURE (percent).
- Data quality and standards
  - Subject to quality assurance procedures.
  - Metadata describes units, data types, and descriptions for each field to facilitate interpretation and reuse.

## Provenance, references, and access
- Origin: NERC Soil Biodiversity Programme; Sourhope upland grassland experiment.
- Related publications and resources:
  - Griffiths et al. 2003: Influence of depth and sampling time on bacterial community structure in an upland grassland soil (FEMS Microbiology Ecology 43:35-43).
  - Sourhope Field Data Handbook (2003): available via EIDC catalogue.
  - Usher et al. 2006: Understanding biological diversity in soil (Applied Soil Ecology).
- Access and usage constraints
  - Data are provided as-is; NERC disclaims warranty on accuracy or suitability for any purpose and excludes liability for use of the data.
  - Availability references include the EIDC catalogue entry and associated publications.

## Data stewardship considerations (for Data Stewards)
- Standards and interoperability
  - Ensure clear, machine-readable metadata aligned with common data conventions (fields, units, data types) as shown in the data dictionaries.
  - Maintain consistent depth measurement units (centimetres) and date formats for SAMPLING_DATE.
- Data governance and access
  - Document provenance, QA steps, and disposal of non-applicable fields where relevant.
  - Capture licensing/disclaimer language (as per NERC statement) and provide guidance on liability and intended use.
- Data quality and updates
  - Preserve original QA status; consider future re-analyses or re-curation as methods evolve.
  - Link datasets to related resources (handbooks, publications) to support discoverability and contextual understanding.
- Discoverability and metadata completeness
  - Ensure dataset-level metadata includes site location, soil type, sampling regime, and analysis methods.
  - Provide data dictionaries and example queries to facilitate reuse by data users with diverse needs.
- Long-term preservation
  - Store CSV files with stable identifiers; maintain versioning if updates occur.
  - Store related publications and supporting information references to preserve context.

## Key notes for users
- The data provide a temporal and depth-resolved view of substrate utilisation by soil bacteria (BIOLOG-GN) and moisture content across several sampling dates.
- For accurate interpretation, users should consult the accompanying Supporting Information and cited literature, as well as the EIDC catalogue entry for access details.
- Use with acknowledgment of the disclaimer regarding data accuracy and responsibility.