# Global_river_decomposition_assay_data_2016_17.csv

## Aim and scope
- Investigates how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Data collected from multiple rivers across Alaska, Austria, Ecuador, France, New Zealand, and Norway during 2016 and 2017.
- Uses a standardized cotton-strip (cellulose) decomposition assay at each site and collects three types of observations: physico-chemical parameters, cotton-strip decomposition metrics, and fungal ITS/cbhI gene data (via qPCR/PCR and amplicon sequencing).

## Study sites and geography
- Study sites distributed across six regions: Alaska, Austria, Ecuador, France, New Zealand, Norway.
- Site labels include A1–A14, E1–E10, F1–F10, NZ1–NZ3, N1–N14, USA1–USA5 with corresponding latitude/longitude coordinates provided.

## Data types and collection
- Three observed parameter categories per site:
  - Physicochemical data
  - Decomposition data
  - Fungal ITS and cbhI data

## Measurements and units (Table 2 overview)
- Physicochemical data
  - %CGC: catchment glacier cover, units: %
  - temp: mean river water temperature during incubation, units: °C
  - turb: optical turbidity, units: NTU
  - Pfankuch index (1/Pfankuch): bottom component index, units: N/A
- Decomposition data
  - TS_DD: mean tensile-strength loss per degree-day, units: (%)(N/degree-day)
  - TS_DD_SD: standard deviation of TS_DD
  - TS_D: mean tensile-strength loss per day, units: (%)(N/day)
- Fungal ITS and cbhI data
  - ITS: ln fungal ITS, units: copy number/cm2 of cotton strip (qPCR)
  - cbhI: ln cbhI gene, units: copy number/cm2 of cotton strip (qPCR)
  - sapro: estimated relative abundance of saprotrophs (PCR)
  - asco: estimated relative abundance of Ascomycota (PCR)
  - tetra: estimated relative abundance of Tetracladium (PCR)

## Methods and data collection details

- Physicochemical measurements
  - temp: recorded using site-appropriate data loggers (iButton, HOBO, TinyTag) during incubation; some sites lacked data (e.g., E9, E10, F11) due to instrument error.
  - pH: measured at study start across sites with various portable meters.
  - turb: turbidity measured from 100 mL water samples at the start using a spectrophotometric method.
  - Pfankuch: reciprocal of the Pfankuch channel stability index (bottom component) measured at study start (except Alaska).
- Decomposition data
  - Cotton-strip assay: four strips per site (up to six at highly unstable sites), incubated for 31–39 days.
  - TS_DD: tensile-strength loss per degree-day calculated from final strip strength relative to incubation temperature (temperature-adjusted degree-days).
  - TS_D: tensile-strength loss per day (non-temperature-adjusted).
  - TS_DD_SD: standard deviation of TS_DD across strips per site.
- Fungal ITS and cbhI data
  - ITS: DNA extracted from a 2 cm2 cotton-strip subsample; qPCR targeting ITS2 region to quantify copy number per cm2.
  - cbhI: similar protocol targeting cellulose-degrading cbhI gene; copy number per cm2.
  - sapro, asco, tetra: fungal community analysis via Illumina MiSeq amplicon sequencing of ITS2; OTU assignment with RDP classifier and UNITE database; trophic guilds via FUNGuild; sapro and asco reflect relative abundances of saprotrophs and Ascomycota; tetra reflects abundance of Tetracladium (where amplified).

## Data processing and provenance
- Standardized, multi-method workflow integrating field measurements, laboratory processing, and molecular analyses.
- Data quality controlled and integrated with metadata; core references include CELLDEX protocol developments, Pfankuch channel stability work, and fungal molecular ecology pipelines (RDP/UNITE/FUNGuild).

## Data quality, coverage, and limitations
- Some measurements missing or uncertain due to instrument errors or assay failures (e.g., temperature data for certain sites; incubation losses at E9, E10, F11).
- Glacier-cover ( %CGC ) is a catchment-scale metric that may not perfectly represent local microhabitat conditions.
- Cross-site standardization challenges due to use of different instruments and local protocols for pH, temp, and turbidity measurements.
- Relative abundance metrics (sapro, asco, tetra) depend on sequencing depth and bioinformatic pipelines; tetra data available only for sites with successful amplification.

## Potential analyses and applications
- Correlate glacier-cover (%CGC) with decomposition metrics (TS_DD, TS_D) across sites and regions, accounting for covariates such as temp, turbidity, and Pfankuch index.
- Build predictive models linking glacier cover to decomposition rates, incorporating microbial functional data (ITS and cbhI copy numbers) and fungal community composition (saprotrophs, Ascomycota, Tetracladium).
- Use mixed-effects models with site or region as random effects to partition regional vs local drivers.
- Explore whether microbial gene abundances (ITS, cbhI) and fungal community structure explain variation in decomposition beyond physico-chemical predictors.

## References and data sources
- Key methodological and background references include Tiegs et al. on standardized cotton-strip assays, CELLDEX DNA/RNA sampling protocols, Pfankuch channel stability index, and fungal community analysis tools (RDP, UNITE, FUNGuild). Additional sources include GLIMS for glacier data and Illumina-based metagenomic library preparation references.