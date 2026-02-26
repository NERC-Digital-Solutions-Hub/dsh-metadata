# Global_river_decomposition_assay_data_2016_17.csv

## Overview
- Dataset supports analysis of how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Data were collected via field observations, laboratory processing, and statistical analysis from sites in Alaska, Austria, Ecuador, France, New Zealand, and Norway during 2016 and 2017 (summer and austral summer).
- A standardized cotton-strip (cellulose) decomposition assay was deployed at each site, with three observation streams: physicochemical parameters, cotton-strip tensile-strength (decomposition) data, and fungal ITS and cbhI gene data (qPCR/PCR) on the cotton strips.
- References provided for methods and data processing.

## Data Collection Scope
- Field sites: multiple rivers across the listed countries; study sites labeled A1–A14, E1–E10, F1–F9, NZ1–NZ3, N1–N14, USA1–USA5 with geographic coordinates (Table 1).
- Incubation: cotton-strip assay deployed at each site for 31–39 days; four strips per site (up to six at highly unstable sites).

## Data Structure and Content

### 1) Physicochemical data
- Purpose: characterize each river site.
- Key parameters and units:
  - %CGC: Catchment glacier cover (%).
  - temp: Mean river water temperature (°C); derived from hourly records during incubation.
  - pH: pH at study start.
  - turb: Optical turbidity (NTU).
  - 1/Pfankuch: Reciprocal of the Pfankuch bottom-channel stability index.
- Notes: Temperature data not available for sites E9, E10, F11 due to instrument error.

### 2) Decomposition data
- Purpose: quantify cotton-strip decomposition performance.
- Key parameters:
  - TS_DD: Tensile-strength loss per degree-day (%)(N/degree-day); temperature-adjusted degree-days used.
  - TS_DD_SD: Standard deviation of TS_DD values across replicates.
  - TS_D: Tensile-strength loss per day (%)(N/day); non-temperature-adjusted rate.
- Notes: Four strips per site (up to six at unstable sites); some assays (E9, E10, F11) were lost during incubation.

### 3) Fungal ITS and cbhI data
- Purpose: quantify fungal community composition and functional genes on cotton strips.
- Key measurements:
  - ITS: ln fungal ITS copy number per cm2 of cotton strip (qPCR).
  - cbhI: ln cbhI gene copy number per cm2 (qPCR).
- Community data (PCR-based):
  - sapro: relative abundance of saprotrophic fungal OTUs (PCR; Illumina sequencing; ITS2 region).
  - asco: relative abundance of Ascomycota (PCR).
  - tetra: relative abundance of Tetracladium (PCR); available only at sites where amplification occurred.
- Processing workflow:
  - DNA extraction (CTAB-based) and qPCR for ITS and cbhI.
  - Illumina MiSeq sequencing of ITS region; quality control; OTU classification with RDP/UNITE; trophic guild via FUNGuild.
- Units: copy number per cm2 for ITS and cbhI; relative abundance for sapro, asco, tetra (PCR-based).

## Study Design and Sampling Details
- Cotton-strip assay: standardized deployment method (Tiegs protocol) with four strips per site (six at highly unstable sites).
- Incubation duration: 31–39 days.
- Measurements taken to enable self-service data exploration and cross-site comparisons, including both physical/chemical context and microbial/ecological dimensions.

## Data Processing and Quality Assurance
- Data integrated from field measurements, lab processing, and molecular analyses.
- Documentation includes detailed methodological references for:
  - Cotton-strip protocol and decomposition metrics (Tiegs et al.; CELLDEX protocol).
  - DNA/RNA extraction and qPCR methods for ITS and cbhI.
  - Illumina-based fungal community analysis (UNITE/RDP, FUNGuild).
- Quality checks include standard PCR/qPCR controls and sequencing data quality workflows.

## Known Gaps and Limitations
- Temperature data gaps: incomplete temp records for some sites (E9, E10).
- Assay losses: certain deployments were lost during incubation (E9, E10, F11).
- Some parameters (e.g., tetra) may be unavailable at sites lacking amplification data.

## Usage Notes for Data Support
- Data are organized to support multi-parameter analyses linking glacier cover to decomposition rates and fungal community structure.
- Coordinates and site metadata facilitate geospatial analyses and cross-site comparisons.
- The dataset enables exploration of:
  - Relationships between catchment ice cover and cotton-strip decomposition metrics.
  - Associations between physicochemical context and fungal gene abundances (ITS, cbhI) and relative abundances of saprotrophs and particular fungal groups (Ascomycota, Tetracladium).

## References
- Methodological and analytical references for field protocols, molecular analyses, and data processing (e.g., Tiegs et al., CELLDEX protocols, Illumina/UNITE/FUNGuild pipelines, Pfankuch index, and related PCR/QC methods).