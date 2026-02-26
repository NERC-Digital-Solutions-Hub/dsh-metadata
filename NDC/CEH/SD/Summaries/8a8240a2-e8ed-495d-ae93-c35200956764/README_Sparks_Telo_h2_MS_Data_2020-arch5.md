# Telomere length data in a wild Seychelles warbler population

## Overview
- Long-term study of the Seychelles warbler on Cousin Island, with the population (~320 adults in 115 territories) monitored since 1985.
- Blood samples collected since 1990; relative telomere length (RTL) measured via qPCR from samples collected between 1995 and 2014.
- The cleaned dataset comprises 2,664 RTL measurements from 1,318 individuals, drawn from analyses in Bebbington et al. (2016), Spurgin et al. (2018), and Sparks et al. (2021).

## Data captured (nature and units)
- Primary variable: RTL (relative telomere length).
- Detailed sampling and metadata accompany RTL measurements (see data structure).

## Quality control and processing
- Technical repeatability:
  - Within-plate repeatability: GAPDH ~0.74; telomere cq ~0.73 (Spurgin et al., 2018).
  - Between-plate repeatability for RTL: ~0.68 (Spurgin et al., 2018).
- Data cleaning and filtering (from Spurgin et al., 2018):
  - Sample inclusion criteria: DNA concentration ≥15 ng/μl; 260/280 between 1.8–2.0; 260/230 > 1.8.
  - DNA integrity verified by 1.2% agarose gel (ethidium bromide visualization); degraded samples re-extracted or excluded.
  - Exclusion criteria: RTL values <3; telomere cq ≥25; GAPDH cq ≤21 or ≥26; replicate differences ≥0.5.
  - Samples with extreme cq values (telomere cq >25; GAPDH cq >26) excluded as failed reactions.
- Preparation and bias mitigation:
  - Random assignment of samples to qPCR plates to avoid systematic biases related to age, sex, cohort, or environment.
  - RTL values from a given blood sample may be used across plates to assess plate variance; plate included as a random effect in analyses (n = 388 with replicates across plates).
- Data scope notes:
  - No storage-time effects observed on telomere length in the examined samples.
  - A subset of 422 samples had duplicate measurements across time points.

## Data structure (key fields)
- BirdID: Individual bird identifier
- Sex: 0 = female, 1 = male
- AgeY: Age at capture in years
- AgeClass: A, CH, FL, J, OFL, SA (adult, chick, fledgling, juvenile, old fledgling, subadult)
- BirthFPID: Birth fieldwork period ID
- U_PlateID: qPCR plate ID for RTL measurements
- RTL: Relative telomere length
- Technician: Technician who performed qPCR (two levels)
- Terr: Territory during capture
- FPID: Fieldwork period ID of capture
- mum, dad: Pedigree IDs
- MAC, PAC: Maternal and paternal ages at conception
- BrF, BrM: Dominant female and male in the natal territory

## Experimental design and sampling
- Breeding season: Major breeding season June–September; some breeding in minor season January–March.
- Sampling method: As many birds as possible are captured each breeding season using mist nets.

## Fieldwork and laboratory instrumentation
- DNA extraction: DNeasy blood and tissue kit; overnight lysis at 37°C; final elution 80 μL.
- DNA quality checks: Gel electrophoresis (1.2% agarose) for integrity; concentration quantified with NanoDrop 8000.
- Telomere measurement: qPCR with random plate allocation to prevent bias; RTL derived from cq values.

## Data governance and reuse notes
- Data integrate findings from multiple studies (Spurgin et al. 2018; Bebbington et al. 2016; Sparks et al. 2021) and are documented with extensive metadata to support reuse in further analyses.
- The dataset emphasizes rigorous QC, metadata richness, and pilot checks for compatibility across plates and temporal sampling, facilitating reliable secondary analyses while acknowledging potential plate- and time-based variance.