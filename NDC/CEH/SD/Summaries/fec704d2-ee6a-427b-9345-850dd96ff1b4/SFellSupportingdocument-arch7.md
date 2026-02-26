# Global_river_decomposition_assay_data_2016_17.csv

## Overview
- A data document supporting the data file Global_river_decomposition_assay_data_2016_17.csv.
- Investigates how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Data were collected from rivers across Alaska, Austria, Ecuador, France, New Zealand, and Norway during 2016–2017 (summer and austral summer).
- Collected through field observations, laboratory processing, and statistical analyses.

## Spatial Coverage and Sites
- Spatial scope includes multiple river sites across six regions, with precise coordinates provided for each site.
- Site codes and locations include:
  - A1–A14 (European region)
  - E1–E10 (Ecuador)
  - F1–F9 (France/Swiss region)
  - NZ1–NZ3 (New Zealand)
  - N1–N14 (Norway)
  - USA1–USA5 (USA)
- Total sampled sites: 55 (approximate, based on code listings).

## Data Structure (Table References)
- Table 1: Study site location information (lat/long for each site).
- Table 2: Observed parameters and their units, organized into three data categories.

## Data Types and Measurements
- Three observation categories:
  1) Physicochemical data
  2) Decomposition data
  3) Fungal ITS and cbhI data

### 1) Physicochemical data
- %CGC: Catchment glacier cover (percent).
- temp: Mean river water temperature during incubation (°C); measured with various loggers; some sites lack data due to instrument error (E9, E10, F11).
- pH: pH at study start.
- turb: Optical turbidity (NTU).
- 1/Pfankuch: Reciprocal of Pfankuch bottom-channel stability index.

### 2) Decomposition data
- TS_DD: Tensile-strength loss per degree-day (% per N per degree-day). Temperature-adjusted degree-days (DD) calculated from mean daily temperatures during incubation.
- TS_DD_SD: Standard deviation of TS_DD across replicates.
- TS_D: Tensile-strength loss per day (% per N per day).
- Notes: Four cotton strips per site (up to six at highly unstable sites); incubations ran ~31–39 days; some assays were lost (e9/e10/f11).

### 3) Fungal ITS and cbhI data
- ITS: ln fungal ITS copy number per cm² of cotton strip (qPCR).
- cbhI: ln copy number of the cbhI gene per cm² (qPCR).
- sapro: Estimated relative abundance of saprotroph-associated fungal OTUs (PCR/Illumina).
- asco: Estimated relative abundance of Ascomycota OTUs (PCR).
- tetra: Estimated relative abundance of Tetracladium OTUs (PCR); available only where Tetracladium amplified.
- Methods: CTAB-based DNA extraction; ITS2 primers for ITS qPCR (qPCR on a Bio-Rad system); cbhI qPCR with appropriate primers; PCR-based amplicon sequencing with Illumina MiSeq; OTU classification via RDP/UNITE; trophic assignment via FUNGuild.

## Data Quality, Gaps and Considerations
- Temperature data missing for some sites (E9, E10, F11).
- Assays at Alaska had exclusions for certain measurements (e.g., bottom-component Pfankuch index not listed for Alaska).
- Some incubation assays were lost (E9, E10, F11).
- Data compiled from multiple instruments and protocols; careful harmonisation required for cross-site analyses.

## GIS and Spatial Analytics Implications
- Site coordinates enable map-based visualisation and spatial analyses of glacier cover effects on decomposition.
- Variables suitable for GIS:
  - Spatial distribution of %CGC and mean river temperature.
  - Decomposition metrics (TS_DD, TS_DD_SD, TS_D) by site.
  - Fungal community metrics (ITS, cbhI copy numbers; sapro/asco/tetra abundances).
  - Channel stability proxy (1/Pfankuch).
- Potential analyses:
  - Correlate glacier-cover gradients with decomposition rates and fungal activity.
  - Overlay with glacier maps, watershed boundaries, and climatic layers.
  - Spatial modelling of decomposition drivers across regions and terrain.

## References and Data Provenance
- Methods references for microbial DNA/RNA analysis, qPCR, and cotton-strip assays (e.g., Tiegs et al.; Dumbrell et al.; UNITE/RDP/FUNGuild pipelines).
- Data are presented with explicit site-level measurements and derived variables, enabling reproducible GIS-enabled analyses.