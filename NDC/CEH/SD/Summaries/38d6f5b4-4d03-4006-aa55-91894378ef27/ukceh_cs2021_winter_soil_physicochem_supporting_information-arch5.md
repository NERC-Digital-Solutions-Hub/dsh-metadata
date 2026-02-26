# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

## Overview
- National long-term soil monitoring project (Countryside Survey) with a rolling program since 2019 to detect changes in topsoil condition and function across Great Britain.
- Focuses on topsoil (0–15 cm) properties and co-located vegetation assessments; data intended for national and sub-national analysis and to support soil health understanding.
- The 2021 dataset is part of the rolling program and is designed to enable comparison with previous surveys and track trends over time.

## Study Design and Sampling
- Survey design uses 1-km x 1-km squares with a rolling cycle: 500 squares per cycle, visited over five years (100 squares annually).
- Squares are stratified by the Land Classification of Great Britain (LC07) and environmental zones; squares dominated by urban/sea are excluded.
- Covid-19 disruption in 2020 affected fieldwork; 50 England-only squares were added later in 2020.
- Winter 2021 sampling subset: 30 (+5 reserve) squares selected to reflect environmental zones; selections prioritize squares surveyed in 1978, 1998, and 2007 and exclude squares dominated by Broad Habitats (e.g., woodlands).
- Within each square: five soil sampling locations (PLOTs) sampled at approximately 15 cm depth using a 15 cm soil core; five cores per square (when feasible).

## Data Collected and Metrics
- Metrics are collected as five soil cores per square, with samples analyzed for typical soil properties and derived carbon metrics.
- Key measured and derived metrics include:
  - pH in deionised water (PH)
  - Loss on ignition (LOI) as a proxy for soil organic matter, plus derived soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
  - Bulk density (BULK_DENSITY) and soil moisture (MOISTURE, MOISTURE_DRY)
  - Total nitrogen (N_PERCENT, N_STOCK)
  - Olsen phosphorus (PO4_OLSEN) not measured in the 2021 winter survey
  - Soil group classification based on LOI (SOIL_GROUP)
  - Land Classification (LC07, LC07_NUM) and Environmental Zones (EZ_DESC_07)
- Data structure comprises 18 columns across 576 rows; missing values are denoted by -9999.
- The dataset relates to the 2021 winter survey and is prepared for integration with other CS data (e.g., vegetation data).

## Data Processing, QA, and Provenance
- A robust data workflow ensures data quality and traceability:
  - Lab QA: laboratories perform initial QA and flag anomalies; outcomes reviewed by data analysts.
  - Analyst QA1: cross-check lab data against records; document queries and changes.
  - Derivation of soil metrics via two R scripts (calculate_soil_derived_metrics_function.R and Derive soil data.R) to ensure reproducibility.
  - QA2: automated HTML QA reports to identify patterns and outliers, with collaboration between analysts and labs to resolve queries.
  - All dataset changes are recorded against data records and QA steps for auditability.
- Supporting metrics from other components (habitat and vegetation) are joined to facilitate downstream QA and analyses.

## Data Structure and Access
- Dataset metadata (Table 5 style) includes:
  - SQUARE: 1-km square identifier
  - PLOT: plot number within the square
  - YEAR: year of survey (noted as 2022 in the metadata, linked to the 2021 winter survey context)
  - PH, LOI, C_CONC_LOI, C_STOCK_LOI, BULK_DENSITY, MOISTURE_DRY, N_PERCENT, N_STOCK
  - PO4_OLSEN: not measured in 2021 winter
  - LC07, LC07_NUM: land classification
  - COUNTRY, EZ_DESC_07: geographic and environmental zone descriptors
- Data are stored and shared via UKCEH data resources (e.g., Soil Bank) with documentation and contact points provided for access requests.

## Data Availability and Sharing
- Data collected under the UKCEH Countryside Survey program and processed for sharing with the research community and policymakers.
- Documentation and data access pathways are provided through UKCEH channels; data are designed to be interoperable with other CS datasets (habitat/vegetation data).
- Versioning and traceability are supported by the QA workflow and accompanying documentation.

## Limitations and Considerations for Data Stewards
- 2021 winter subset specifics: Olsen phosphorus not measured for this survey; subset selection criteria may affect representativeness for certain habitats or regions.
- Covid-related disruptions and resampling could introduce temporal or spatial biases relative to full-year coverage.
- Data are designed for national/regional indicators rather than single-site interpretation; cross-year comparability relies on consistent methodology and documentation.

## Governance, Standards, and Stewardship Guidance
- Ensure alignment of metadata with LC07, EZ_DESC_07, LOI soil groups, and 1-km square identifiers for consistent discovery and reuse.
- Maintain full audit trails of data processing steps (lab QA, analyst QA, derived metrics) and any data corrections.
- Preserve links to related CS datasets (vegetation, habitat) to support integrated analyses and reproducibility.
- Monitor and document any methodological changes (e.g., sample selection during rolling surveys, Covid-related adjustments) to maintain temporal comparability.
- Facilitate access requests with clear provenance, data usage guidance, and citation information.

## References and Further Reading
- References and methodological documents are provided within the Countryside Survey materials (Soils Manual, QA procedures, land classification documents, and related technical reports).