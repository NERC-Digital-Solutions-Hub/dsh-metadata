# Global river decomposition assay data 2016_17.csv

## Overview
- Describes a dataset investigating how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Data collected from field observations, laboratory processing, and statistical analysis across sites in Alaska, Austria, Ecuador, France, New Zealand, and Norway during 2016 and 2017 (summer and austral summer).
- The accompanying data file is Global_river_decomposition_assay_data_2016_17.csv.
- Three main observation categories per site: physicochemical parameters, decomposition measurements, and fungal ITS/cbhI genetic data; plus derived fungal group abundances (saprotrophs, Ascomycota, Tetracladium).
- Emphasis on standardized methods and data quality, with outputs suitable for cross-site environmental health and policy monitoring.

## Study design and data collection
- Cotton-strip (cellulose) decomposition assay deployed at each site; four strips per site (up to six at highly unstable sites); incubation period 31–39 days.
- Three observation streams:
  - Physicochemical parameters to characterize each river site.
  - Decomposition data: tensile-strength loss (TS_DD) and related metrics.
  - Fungal data: ITS and cbhI gene copy numbers (qPCR), plus amplicon-based estimates of saprotrophs and select fungal groups.
- Data gathered through field measurements, laboratory processing, and molecular analyses (PCR/NGS).
- Some sites reported missing data due to instrument error or assay loss (e.g., E9, E10, F11).

## Variables and measurements
- Physicochemical data (Table 2):
  - %CGC: Catchment glacier cover (percent).
  - temp: Mean river water temperature (°C) during incubation.
  - pH: pH at study start.
  - turb: Optical turbidity (NTU).
  - 1/Pfankuch: Inverse Pfankuch Channel Stability index (where available).
- Decomposition data:
  - TS_DD: Mean tensile-strength loss per degree-day (% per N per degree-day).
  - TS_DD_SD: Standard deviation of TS_DD.
  - TS_D: Mean tensile-strength loss per day (% per N per day).
- Fungal ITS and cbhI data:
  - ITS: ln fungal ITS copy number per cm2 of cotton strip (qPCR).
  - cbhI: ln cbhI gene copy number per cm2 of cotton strip (qPCR).
  - sapro: Estimated relative abundance of saprotrophs (PCR-based).
  - asco: Estimated relative abundance of Ascomycota (PCR-based).
  - tetra: Estimated relative abundance of Tetracladium (PCR-based; available where amplified).
- Data processing and interpretation rely on standard molecular pipelines (CTAB DNA extraction, qPCR with ITS2 primers, Illumina amplicon sequencing, taxonomic classification via UNITE/RDP, and ecological guild assignment via FUNGuild).

## Study sites and locations
- Site labels and coordinates cover multiple geographic regions:
  - A1–A14: European Alps region (coordinates provided).
  - E1–E10: South American/Caribbean-like coordinates listed (varied).
  - F1–F11: European sites (northern Switzerland/France area; coordinates listed).
  - NZ1–NZ3: New Zealand sites (lat/long provided).
  - N1–N14: Additional Northern Hemisphere sites (lat/long provided).
  - USA1–USA5: United States sites (lat/long provided).

## Data processing, quality assurance, and outputs
- Data were standardized, quality-checked, and transformed for cross-site comparability.
- Outputs include a structured dataset with physicochemical, decomposition, and molecular metrics, suitable for linking glacier cover with microbial-mediated decomposition.
- Data and datasets are stored and uploaded to appropriate portals to enable access by researchers and policymakers.

## Challenges and opportunities for Analysts Monitoring the Environment
- Valuing datasets beyond single-use applications by integrating them with other environmental data (e.g., glacier cover, hydrology, microbial communities).
- Facilitating access to underlying data used to generate final outputs to support transparency, reproducibility, and broader policy analysis.

## References
- Citations provided for methods in microbial DNA/RNA extraction, qPCR, sequencing, data processing, and the standardized cotton-strip assay protocol, along with glacier data sources and ecological annotation tools.