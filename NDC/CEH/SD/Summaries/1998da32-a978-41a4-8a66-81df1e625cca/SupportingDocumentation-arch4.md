# Supporting Documentation

## Overview
- Dataset of 17 electrical resistivity tomography (ERT) surveys in the Makutapora Basin, central Tanzania, conducted between 28 June 2019 and 16 July 2019.
- Purpose: delineate superficial geological structures to understand their control on surface-groundwater interactions and recharge within the Makutapora wellfield.
- Authors responsible for design and oversight: E. Zarate and M. O. Cuthbert.

## Data Assets
- 17 survey results (ERT data).
- Metadata and geometry: coordinates, survey geometry, line name suffixes, and locations contained in Supp_Table_for_Survey.csv.
- Data formats:
  - Raw: .stg files from AGI STING resistivity meter.
  - Processed: .dat dataset files derived from raw .stg via bespoke Python code.
- Accessibility: Raw .stg and processed .dat, with Python code available on request from the corresponding author.

## Collection Methods
- Instrumentation: AGI SuperSting R8 resistivity meter.
- Configuration: dipole-dipole array; electrode spacings and related parameters documented in Supp_Table_for_Survey.csv.
- Method reference: detailed methodology described in the associated paper.

## Data Processing & Quality Control
- Quality control steps:
  - Remove negative values.
  - Each apparent resistivity measurement averaged from normal and reciprocal configurations.
  - Discard any value where the normal and reciprocal measurements differ by more than 5% from the mean.
- Objective: characterize superficial geological structures to infer their role in surface-groundwater interactions and recharge mechanisms.
- Oversight: QC and survey design overseen by E. Zarate and M. O. Cuthbert.

## Metadata & Discoverability
- Supp_Table_for_Survey.csv provides:
  - Coordinates and locations.
  - Survey geometry details.
  - Line suffixes for traceability.
- Metadata supports data discovery, interpretation, and reuse alongside the raw and processed data files.

## Access, Usage & Reuse
- Data products (.dat) are available; raw data (.stg) and associated materials can be requested from the corresponding author.
- Intended use: hydrogeological analysis and modeling of groundwater recharge in the Makutapora wellfield; methodology context provided in the related paper.

## Provenance & Responsibility
- Survey design and data collection led by E. Zarate and M. O. Cuthbert.
- Data processing and QC performed to ensure reliability and suitability for interpretation.

## Implications for Data Leaders
- Demonstrates the importance of comprehensive metadata (e.g., Supp_Table_for_Survey.csv) for discoverability and reuse.
- Highlights clear documentation of data collection parameters, processing steps, and QC criteria as part of an effective data system.
- Reflects practical considerations for data access (raw data availability on request) and cross-team collaboration for data quality and interpretation.