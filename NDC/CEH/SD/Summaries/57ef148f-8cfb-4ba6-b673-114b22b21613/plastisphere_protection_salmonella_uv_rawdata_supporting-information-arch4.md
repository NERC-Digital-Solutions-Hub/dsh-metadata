# Persistence and Virulence of Salmonella Typhimurium on Plastic Waste Under UV Exposure

## Overview
- Study of the ability of a clinically relevant Salmonella Typhimurium strain to adhere to and persist on plastic waste (PE and Glass) under UV exposure, and to assess virulence using a Galleria mellonella model.
- Experimental design includes a defined photoperiod with white light, UV exposure (UV index 8), and darkness; sampling at multiple days post-inoculation; virulence testing across a range of inocula; biological triplicates.
- Data created to support understanding of microbial persistence, die-off rates, and pathogenicity in environmental contexts, aligned with UKRI/NERC grants on the plastisphere.

## Data Assets and Structure
- Five CSV data files:
  - Persistence_Salmonella_UV_exposure.csv: persistence levels on PE or Glass after UV exposure, including dry and submerged conditions.
  - Concentration_killing_curve_Galleria_control.csv: virulence data for Salmonella Typhimurium D23580 in G. mellonella.
  - Virulence_in_Galleria_mellonella_model.csv: virulence data for Salmonella recovered from PE and Glass in G. mellonella.
  - Temperature_logger_data.csv: temperature data recorded during the study.
  - Linear_decline_analysis.csv: die-off rate analysis (k, D-values, etc.).
- Data content includes:
  - Material (Plastic PE or Glass)
  - Condition (Dry, Submerged, or water)
  - UV exposure (UV or No_UV)
  - Time (Days or Hours)
  - Concentration (CFU/ml) and inocula
  - Replicates
  - Survival percentages for G. mellonella
  - Regression metrics (R-squared, Gradient, K/day, D-value)

## Metadata and Data Standards
- Units and variables:
  - Temperature in °C; CFU/ml for concentrations; days and hours for time; percentages for survival.
  - Regression and decline metrics: R-squared, Gradient, K (per day), D-value (days).
  - ND denotes missing data.
- Provenance:
  - Collected in Scotland, UK, February–August 2024.
  - Biological triplicates; confirmatory PCR for Salmonella identity (ttr gene verification).
- Data organization:
  - Separate CSV files per experimental variable; columns describe factors (strain, material, temperature, etc.) with units and description.

## Data Collection Methods
- Experimental setup:
  - Salmonella Typhimurium inoculated onto glass and PE surfaces in nutrient-rich and surface water environments.
  - Photoperiod: 4 h white light; 4 h UV (UV index 8); 4 h white light; 12 h darkness.
  - UV exposure, temperature, and materials controlled and monitored.
- Sampling regime:
  - Timepoints: 1, 2, 3, 6, 8, 10, 14, 21 days after inoculation (DAI) for persistence assays.
  - Galleria mellonella virulence assays conducted with a dose range from 10^3 to 10^12 CFU per larva; survival monitored for 72 hours.
  - Additional 21-day samples recovered from materials to assess pathogenicity upon re-challenge.
- Laboratory instrumentation:
  - 96-well plates, incubators, PCR systems, plate reader; iButton temperature loggers for environmental monitoring.
  - Calibration of plate reader and PCR thermocycler per standard protocols.

## Experimental Design and Sampling Regime
- Materials: glass and LDPE (PE) surfaces.
- Conditions: Dry, Submerged, or water environments.
- UV: UV-exposed vs. non-UV controls.
- Sampling: 1, 2, 3, 6, 8, 10, 14, 21 DAI for persistence; 72 h for Galleria virulence post-challenge.
- Replication: Biological triplicates; multiple replicates per condition and timepoint.
- Data analysis approach:
  - Die-off rates modeled with log-linear regression on log10-transformed CFU data.
  - Calculation of t90 (decimal reduction time) from decline rates.
  - ANOVA and post-hoc tests (Holm-Šídák) to assess treatment effects; SPSS used for multi-factor analyses (strain, temperature, material).

## Data Quality, Provenance, and Completeness
- Quality controls:
  - Replication, ANOVA, regression modelling, and confirmatory PCR for strain verification.
  - Temperature and light conditions tightly controlled and recorded.
  - Data checked for anomalous values; missing data indicated as ND.
- Responsible steward:
  - Michael J. Ormsby led data collection and interpretation.
- Completeness:
  - Data file set defined; some data may be missing (ND noted where applicable).

## Data Access and Reuse
- Data files and descriptions:
  - Persistence_Salmonella_UV_exposure.csv: persistence after UV exposure on plastic and glass.
  - Concentration_killing_curve_Galleria_control.csv: virulence in G. mellonella model.
  - Virulence_in_Galleria_mellonella_model.csv: virulence of recovered Salmonella from materials.
  - Temperature_logger_data.csv: environmental temperature throughout the study.
  - Linear_decline_analysis.csv: die-off rate analyses (k, D-values, RSquared, etc.).
- Context and citation:
  - Data collected under UKRI/NERC projects on the plastisphere; related publications cited for broader context.