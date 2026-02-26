# Kākāpō Egg Fertility 2019: Documentation

## Overview
- Dataset documents origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season.
- 252 eggs laid; 129 failed to develop. Yolk from undeveloped eggs preserved in formalin and transported to the University of Sheffield, UK for dissection and analysis.
- Objective: distinguish between fertilisation failure and early embryo death to inform conservation management.
- Funded by Natural Environment Research Council Urgency Grant.

## Aims and Purpose (How this supports data stewardship)
- Provide a comprehensive, well-documented data package to support conservation decisions.
- Capture provenance, collection, processing, and analysis steps to enable reuse and integration with other datasets.
- Ensure data reflect true observations (fertilisation status, PVL sperm, and egg characteristics) for robust interpretation.

## Data Sources and Provenance
- Primary collection by the New Zealand Department of Conservation Kākāpō Recovery Programme (KRT) on Anchor and Whenua Hou islands.
- Samples and data shipped/processed with University of Sheffield (NH, JS) analyses on fertilisation and PVL sperm.
- Supported by a NERC Urgency Grant NE/T00200X/1.
- Additional population and management context held by the NZ Department of Conservation.

## People, Roles, and Responsibilities
- Nicola Hemmings (University of Sheffield): Principal Investigator; analysed undeveloped eggs; overall project administration.
- James Savage (University of Sheffield): Researcher Co-Investigator; oversaw sample collection/transport; responsible for data management.
- Jodie Crane (Kākāpō Recovery, NZ DOC): Senior Ranger; performed egg sampling and recorded egg size/weights; liaison among team.
- Kākāpō Recovery Team (NZ DOC): Field operations and broader breeding monitoring; multiple named staff contributed to data collection and logistics.

## Study Population
- Endangered kākāpō population managed by Kākāpō Recovery Team on predator-free offshore islands (Anchor Island and Whenua Hou/Codfish Island).
- 110 individuals in breeding program; breeding season marked by high egg production (252 eggs in 2018/19).
- Mating data include natural matings and artificial insemination events.

## Data Collected and Methods
- In-field: daily candling during artificial incubation; sampling of undeveloped eggs; yolk preservation in 5% formalin.
- Transport: yolk samples shipped to University of Sheffield (CITES GB041).
- In-lab (Sheffield): yolk extraction; staining with Hoechst 33342; fluorescence microscopy to detect embryonic cells and sperm; PVL (perivitelline layer) sperm counts; recording of fertilisation status.
- Measurements recorded: egg length/width, preserve/fresh weights, albumen/yolk weights, eggshell weight, PVL area, sperm counts, and related notes.
- Two linked datasets capture complete and undeveloped egg data; egg_id serves as the key for merging records.

## Dataset Structure
- File 1: kakapo_egg_fertility_2019-1_all_eggs
  - 252 rows, 10 columns
  - Key fields: egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI
- File 2: kakapo_egg_fertility_2019-2_undeveloped_eggs
  - 129 rows, 15 columns
  - Key fields: egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
- The egg_id field is the linkage key across both files, enabling dataset merges if needed.

## Data Governance, Provenance, and Sharing
- Explicit provenance: field collection by NZ DOC,Analysis by UK university, formalin preservation and international shipment; dataset structure to support traceability.
- CITES-relevant note: yolk samples shipped to UK institution; documentation indicates regulatory compliance.
- Metadata and schema clearly define variable meanings and data lineage to support reuse across platforms and portals.
- Additional data about the wider kākāpō population and management practices are held by NZ DOC, indicating potential for future integration.

## Quality Assurance and Data Management
- Data management responsibilities distributed among researchers: data collection in the field, careful labeling of egg_id, standardized measurements, and post-collection processing.
- Data are organized into two CSV files with explicit, consistent variable definitions to facilitate quality checks and merging.
- Clear documentation of methods (candling, sampling, PVL assessment, staining, microscopy) supports reproducibility and auditability.

## Limitations and Considerations for Stewardship
- The dataset is focused on a single breeding season and two specific islands; broader temporal/spatial coverage exists but is not included here.
- Some fields may contain missing values (e.g., fertilized status in undeveloped eggs), which should be handled carefully in analyses.
- Multiple collaborating organizations and regulatory steps imply ongoing governance requirements when sharing or reusing the data.

## Access, Use, and Next Steps for Data Stewards
- Data produced for conservation management and research; access likely via NZ DOC and collaborating institutions (University of Sheffield) with appropriate approvals.
- Potential for integration with broader kākāpō population datasets and reproductive histories held by NZ DOC.
- Suggested actions: maintain data provenance, ensure ongoing updates and linkage with related datasets; consider publishing a data dictionary and data access statement to guide reuse.