# Global_river_decomposition_assay_data_2016_17.csv

## Overview
- Supports the data file Global_river_decomposition_assay_data_2016_17.csv.
- Collected to examine how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Data were gathered through field observations, laboratory processing, and statistical analysis during 2016 and 2017 across multiple countries.
- Utilizes a standardised cotton-strip decomposition assay with three observation types: physicochemical parameters, cotton-strip decomposition metrics, and fungal ITS/cbhI molecular data.

## Data Contents and Structure
- Study sites and coordinates (Table 1): samples from a wide geographic range including Alaska, Austria, Ecuador, France, New Zealand, Norway, the USA, and others, with explicit latitude/longitude for each site (A1–A14, E1–E10, F1–F9/F10/F11, NZ1–NZ3, N1–N14, USA1–USA5).
- Observed parameters and units (Table 2): three data groups
  - 1) Physicochemical data (%CGC, temp, pH, turb, 1/Pfankuch)
  - 2) Decomposition data (TS_DD, TS_DD_SD, TS_D, plus SD)
  - 3) Fungal ITS and cbhI data (ITS, cbhI, sapro, asco, tetra)
- Each parameter has explicit units and collection method described in the data description.

## Measurements and Methods
- Cotton-strip decomposition assay
  - Four cotton strips per site (up to six at highly unstable sites).
  - Incubation period: 31–39 days.
  - Metrics derived: TS_DD (tensile-strength loss per degree-day), TS_DD_SD (standard deviation), TS_D (tensile-strength loss per day).
  - Temperature-adjusted degree-days (DD) calculated from mean daily temperatures during incubation.
  - Aimed to quantify organic-matter decomposition across sites.
- Physicochemical measurements
  - %CGC: catchment glacier cover derived from watershed delineation and ice-area boundaries.
  - temp: mean river water temperature during incubation, measured with various loggers; some sites had unavailable values due to instrument error.
  - pH: measured at study start with multiple meters across sites.
  - turb: optical turbidity measured from 100 mL samples at study start; reported in NTU.
  - 1/Pfankuch: reciprocal of the Pfankuch channel stability index (except Alaska).
- Molecular and fungal data
  - ITS (fungal ITS) and cbhI (cellobiohydrolase I gene) via qPCR; units are copy number per cm2 of cotton strip.
  - sapro (saprotrophs), asco (Ascomycota), tetra (Tetracladium): estimated relative abundances of fungal OTUs via PCR-based metabarcoding; units are relative abundances.
  - Molecular workflows include DNA extraction, qPCR, Illumina MiSeq sequencing, quality control, OTU classification (RDP, UNITE), and ecological guild/trophic assignments (FUNGuild).

## Study Sites
- Site coverage spans a diverse set of geographic regions with detailed coordinates provided in Table 1.
- Data gaps noted: values unavailable for certain sites (e.g., temp for E9, E10, F11 due to instrument error; some incubation assays were lost at E9, E10, F11).

## Data Quality, Gaps, and Governance Notes
- Explicit documentation of instrument-related data gaps and assay losses, reflecting real-world field challenges.
- Metadata include site-level conditions, equipment used, and incubation parameters, supporting data traceability.
- The dataset links to a set of established protocols and references for replication and auditability (e.g., Tiegs et al., Dumbrell et al., UNITE/FUNGuild pipelines, Pfankuch index).

## Analytical Pipeline and Outputs
- Data are organized to enable analyses across three axes: changes in glacier cover, environmental conditions, and decomposition/fungal responses.
- Multilevel data (field measurements, laboratory processing, and molecular sequencing) enable integrated assessments of ecosystem processes in mountain river systems.

## Relevance for Monitoring Frameworks
- Demonstrates an integrated monitoring framework combining physical, biochemical, and molecular indicators to understand environmental health and ecosystem functioning.
- Emphasizes the importance of:
  - Comprehensive site metadata (location, climate, hydrology, substrate stability)
  - Standardized assays (cotton-strip decomposition) for cross-site comparability
  - Rigorous data processing pipelines (qPCR, sequencing, OTU classification, ecological guild assignment)
  - Clear documentation of data gaps and measurement limitations
- Provides a replicable template for monitoring programs that aim to link land/water surface conditions (e.g., glacier cover) to upstream ecosystem processes (organic-matter decomposition and fungal activity).