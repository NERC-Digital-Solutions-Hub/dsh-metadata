# Details of data structure to ' NW_N2O.csv '

## Overview
- Supplement to supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Contains N2O emissions data from a grassland fertiliser trial (2016) conducted at North Wyke Research Station (Rothamsted Research)
- Data recorded with manual static chambers
- NW_N2O.csv comprises 6 columns and 608 rows

## Dataset Details (Structure and Content)
- Time: Date and time of N2O sampling
- N_app: fertiliser application indicator
  - 1 or 2 denotes first or second application (90 kg N ha-1)
  - 3 denotes the third application (60 kg N ha-1)
- Block: Blocking factor of the randomized block design (1–4)
- Plot: Experimental unit identifier
- Treatment: Fertiliser type
  - AN = ammonium nitrate (Nitram)
  - IU = inhibited urea (agrotain)
  - U = urea
  - C = 0N Control
- Flux_N2O: N2O flux for each chamber measurement
  - Unit: g N2O-N ha-1 day-1
- Quality note: Flux data with R^2 < 0.6 and all negative Flux_N2O values replaced with 0

## Data Size and context
- 6 columns, 608 rows
- Data series origin: grassland fertiliser trial 2016

## Provenance and Context
- Part of a larger CINAg experiment framework; data are supplementary to the primary supporting documentation
- Data collection method: manual static chambers

## Metadata, Units, and Standardization
- Column-level definitions and units specified (times, numeric flux units, and coded categories for N_app, Block, Plot, Treatment)
- Clearly defined codebooks for N_app, Block, Plot, and Treatment categories

## Data Access, Sharing, and Management
- Data are prepared for sharing via NW_N2O.csv alongside supplementary documentation
- Practices implied: upload to relevant portals and catalogue data holdings; maintain dataset alongside its metadata

## Data Stewardship Implications and Actions
- Ensure consistency of coding schemes (N_app, Block, Plot, Treatment)
- Preserve time stamps and sampling context for reproducibility
- Maintain and enforce the QC rule: negative Flux_N2O values replaced with 0; retain R^2 filtering criterion (R^2 < 0.6)
- Document data provenance, processing steps, and any alterations to flux data
- Align metadata with other datasets in the series to support discoverability and reuse

## Challenges and Considerations for Data Stewards
- Potential gaps between user needs and dataset availability
- Timely ingestion from field sources and synchronization with supplementary documentation
- Managing multiple systems/formats and ensuring interoperability of codes
- Handling and transferring data from potentially large or complex field experiments
- Addressing incomplete metadata or lineage information in related datasets

## Recommendations for Use and Future Curation
- Maintain a clear data dictionary for all coded fields (N_app, Block, Treatment)
- Record any updates to data processing rules (e.g., QC criteria or unit changes)
- Ensure dataset versioning and traceability within the data portal
- Cross-link NW_N2O.csv with related datasets from the same trial for holistic analyses