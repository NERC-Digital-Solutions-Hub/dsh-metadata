# Overview

- The document supports the accompanying data file titled 'Global_river_decomposition_assay_data_2016_17.csv' and describes data collected to study how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Data were gathered from field observations, laboratory processing, and statistical analysis across multiple countries (Alaska, Austria, Ecuador, France, New Zealand, Norway) during 2016 and 2017 summers.
- A standardized cotton-strip (cellulose) decomposition assay was deployed at each river site, with three types of observations collected:
  - Physicochemical parameters
  - Decomposition data (tensile-strength loss)
  - Fungal ITS and cbhI data (DNA/RNA-based measures and fungal community info)

## Study Design and Data Types

- Cotton-strip assay
  - Four strips per site (up to six at more unstable sites)
  - Incubation period: 31–39 days
- Observed parameter categories (Table 2)
  - 1) Physicochemical data: catchment glacier cover (%CGC), mean river temperature (temp, °C), pH, optical turbidity (turb, NTU), 1/Pfankuch (channel stability)
  - 2) Decomposition data: mean tensile-strength loss (TS_DD in %·N/degree-day; TS_D in %·N/day), with standard deviation (TS_DD_SD)
  - 3) Fungal ITS and cbhI data: ITS and cbhI copy numbers per cm2 of cotton strip (qPCR), relative abundances of saprotrophs (sapro), Ascomycota (asco), and Tetracladium (tetra) from PCR/NGS data
- Data processing details
  - Molecular data: DNA extraction, qPCR for ITS and cbhI, Illumina sequencing for fungal communities, OTU classification with RDP and UNITE, trophic guild assignment with FUNGuild
  - Data processing references include standardized protocols (e.g., CELLDEX) and established methods for quality control and taxonomic assignment

## Study Sites and Scope

- Sites span the following regions with specific coordinates provided (Table 1): Alaska, Austria, Ecuador, France, New Zealand, Norway, and additional sites coded as A1–A14, E1–E10, F1–F11, NZ1–NZ3, N1–N14, USA1–USA5, among others.
- Data include geographic coordinates for all sites and a mix of lat/long formats.

## Data Attributes and Units (Summary)

- Physicochemical data
  - %CGC: catchment glacier cover
  - temp: mean river water temperature (°C)
  - pH: measured at site
  - turb: optical turbidity (NTU)
  - 1/Pfankuch: channel stability index (dimensionless)
- Decomposition data
  - TS_DD: tensile-strength loss per degree-day (%·N/degree-day)
  - TS_DD_SD: standard deviation of TS_DD
  - TS_D: tensile-strength loss per day (%·N/day)
- Fungal ITS and cbhI data
  - ITS: ln fungal ITS copy number per cm2 (qPCR)
  - cbhI: ln cbhI copy number per cm2 (qPCR)
  - sapro: estimated relative abundance of saprotrophs (PCR)
  - asco: relative abundance of Ascomycota (PCR)
  - tetra: relative abundance of Tetracladium (PCR)

## Data Quality, Gaps, and Considerations for Stewardship

- Data quality and completeness
  - Temperature data unavailable for sites E9, E10, and F11 due to instrument error
  - Some assays were lost or could not be completed at certain sites (e.g., E9, E10, F11 for decomposition measurements)
  - Data collection involved multiple instruments and loggers, introducing cross-site measurement variance (pH and temperature were measured with different instruments across countries)
- Data governance implications
  - Procedures rely on standardized protocols for cross-site comparability (e.g., Tiegs 2013/2015 CELLDEX and cotton-strip methodology)
  - Comprehensive metadata (site coordinates, parameters, units) supports data provenance and reuse
  - Data processing steps for molecular data (quality control, OTU classification, guild assignment) should be captured for reproducibility
  - Potential data sharing considerations include updates to missing data and harmonization across diverse data formats and instruments
- Documentation and updating
  - The dataset is anchored by a single CSV data file and the accompanying methodological descriptions, with references for all protocols and analyses
  - Documentation provides explicit details on measurement procedures, incubation conditions, and data transformations to support future updates and dataset expansion

## References and Key Methods

- Standardized cotton-strip decomposition protocols (Tiegs et al.;CELLDEX protocols)
- Molecular and bioinformatic workflows for fungal community analysis (DNA/RNA extraction, qPCR for ITS and cbhI, Illumina sequencing, OTU classification with UNITE/RDP, FUNGuild for trophic guilds)
- Instrumentation and data logger usage for temperature and site measurements
- Relevant literature cited for methods and data processing (e.g., Pfankuch index, cellulose-decomposition methodology, qPCR and sequencing approaches)