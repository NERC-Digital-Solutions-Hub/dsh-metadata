# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

## Overview
- Objective: Determine chemical deterioration and material changes of three anonymised bio-based teabags (PLA-cellulose) after 7 months buried at -10 cm in UK soil.
- Timeframe and setting: November 2021 – June 2022, field burial in the UK.
- Funding: NERC BIO-PLASTIC-RISK project (grants NE/V007556/1 and NE/V007246/1).
- Data scope: Six data files capturing mass loss, crystallinity, PLA content, and chemical composition of teabags before and after burial.
- Materials: Teabags composed of polylactic acid (PLA) – cellulose blends; three anonymised brands (Tbag A, B, C).

## Data files included
- Degradation_crystallinity.csv — crystallinity measurements after 7 months.
- Degradation_Mass.csv — teabag mass loss after burial.
- Degradation_PLA.csv — proportion of PLA in teabags after burial.
- Degradation_prGCMS_TbagA.csv — Py-GCxGC-TOF MS data for Tbag A.
- Degradation_prGCMS_TbagB.csv — Py-GCxGC-TOF MS data for Tbag B.
- Degradation_prGCMS_TbagC.csv — Py-GCxGC-TOF MS data for Tbag C.

## Measurements and computations
- Mass loss
  - Calculation: mass_loss_percent = 100 - (final_mass / initial_teabag_mass) * 100
- PLA proportion
  - Method: dissolve PLA in chloroform (30 min at room temperature), filter, evaporate solvent, dry mass; compute cellulose:PLA as:
    cellulose:PLA = (mass_cellulose) / (mass_cellulose + mass_PLA) : (mass_PLA) / (mass_PLA + mass_cellulose)
  - Notes: some data may be NAN (no data obtained); no data included for Tbag C in this file.
- Crystallinity
  - Method: Dynamic Scanning Calorimetry (DSC) using Discovery DSC25; heating/cooling at 20 °C/min under nitrogen with a complex ramp program.
  - Crystallinity calculation: crystallinity (%) = [(ΔHm − ΔHcc) / ΔH100%] × 100
    - ΔHm: enthalpy of melting; ΔHcc: enthalpy of cold crystallisation; ΔH100%: theoretical enthalpy of melting for 100% crystalline PLA (93 J/g).
  - Precision: enthalpy precision 0.1%.
- Chemical composition (Py-GCxGC-TOF MS)
  - Instrumentation and workflow: Pyrolysis GCxGC-TOF MS with a CDS6200 Pyroprobe (600 °C, 30 s), constant flow GC (1D: 0.5 mL/min; 2D: 20 mL/min), INSIGHT flow modulator, and a dual-column setup (BPX5 1D, BPX50 2D). Data processed with ChromSpace; compounds identified via NIST MS library.
  - Sample:
    - Teabags: 80–100 μg per replicate; teabags analysed in triplicate (for each teabag type).
  - Data output: retention times (1tR, 2tR), compound name, and main ion information.

## Data structure and variables
- Degradation_crystallinity.csv
  - Columns: Tbag (anonymised brand, e.g., Tbag-A, Tbag-B), Time (months), crystallinity (%)
  - Note: No crystallinity data for Tbag-C.
- Degradation_Mass.csv
  - Columns: Tbag (A, B, or C), Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), Mass_loss_percent (%)
- Degradation_PLA.csv
  - Columns: Tbag (A or B; C data NAN), Time (months), PLA_content (%)
- Degradation_prGCMS_TbagA.csv, Degradation_prGCMS_TbagB.csv, Degradation_prGCMS_TbagC.csv
  - Columns: 1tR (min), 2tR (s), Compound (name), ions (characteristics of main ions)
  - Structure consistent across the three files; used for chemical composition analysis of each teabag type.
- Data notes:
  - NAN indicates no data obtained.
  - Data include multiple teabag brands sampled from various boxes to capture variability; samples stored and processed under controlled conditions.

## Quality control
- Sampling: teabags sourced from at least five boxes across multiple stores in Plymouth, UK (July–October 2021) to capture variability.
- Sample handling: washed, dried, vacuum-sealed in Mylar within polyethylene bags; stored at 4°C until analysis.
- Measurements:
  - Mass: analytical balance with calibration checks prior to use.
  - Crystallinity: DSC with specified thermal protocol; enthalpy precision 0.1%.
  - Py-GCxGC-TOF MS: triplicate analyses per teabag type; thorough instrument cleaning between teabag types.

## Data usage and provenance
- This dataset accompanies the research output:
  Courtene-Jones et al (2024) Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment. DOI: https://doi.org/10.1016/j.scitotenv.2024.172806

## Limitations and notes
- Some data are missing for certain teabag types (e.g., Tbag-C crystallinity data absent; PLA data NAN for Tbag C).
- Teabags are anonymised; experimental context is limited to burial in UK soil at a single depth and duration (7 months).
- Results pertain to specific brands and may not generalise beyond these samples without further replication.