# Persistence and UV Exposure of Salmonella Typhimurium on Plastic Waste and Associated Virulence in Galleria mellonella — Dataset Description

## Objective
- Document a study on the ability of a clinically relevant Salmonella Typhimurium strain to colonise and persist on plastic waste and withstand UV exposure, with virulence assessed in the Galleria mellonella model.
- Data collected to support UKRI NERC grants on the plastisphere and related projects.

## Data files and what they contain
- Persistence_Salmonella_UV_exposure.csv
  - Persistence levels of S. Typhimurium on plastic (PE) and glass under UV exposure, including dry, submerged, and surrounding water conditions.
- Concentration_killing_curve_Galleria_control.csv
  - Virulence data of wild-type S. Typhimurium D23580 in Galleria mellonella infection models (control curves).
- Virulence_in_Galleria_mellonella_model.csv
  - Virulence data for S. Typhimurium recovered from PE and glass in Galleria mellonella challenges.
- Temperature_logger_data.csv
  - Temperature measurements recorded throughout the study.
- Linear_decline_analysis.csv
  - Die-off (decline) rates of S. Typhimurium over time on plastic and glass, including UV vs no-UV conditions.

## Study setting and timescale
- Location: Scotland, United Kingdom.
- Period: February to August 2024.
- Materials: plastic (PE or LDPE referenced) and glass surfaces.
- Photoperiod and UV exposure: 4 h white light; 4 h UV (UV index ~8); 4 h white light; 12 h darkness.
- Temperature monitoring: logged continuously (1-hour intervals).

## Experimental design and sampling
- Inoculation: S. Typhimurium D23580 onto materials in nutrient-rich and surface water environments.
- UV exposure: Controlled photoperiod with UV exposure at UV index 8.
- Timepoints for persistence and die-off: 1, 2, 3, 6, 8, 10, 14, and 21 days after inoculation (DAI).
- Galleria mellonella virulence assay:
  - Dose range: 10^3 to 10^12 CFU per larva in a tenfold dilution series.
  - Inoculum: 10 µL per larva; temperature 37 °C; survival assessed at 72 hours.
  - Replicates: biological triplicate; negative PBS controls.
  - Post-recovery virulence: 21-day material samples recovered in PBS injected into larvae to assess remaining pathogenicity.
- Replication and controls: biological triplicates; confirmatory PCR for strain verification; negative controls for larval challenges.

## Analytical methods
- Die-off analysis: CFU counts log10-transformed and analyzed with log-linear regression to estimate decline rate (k, day^-1) and decimal reduction time (D-value). Equation: log10(C) = log10(C0) − k·t.
- Statistical testing:
  - ANOVA to assess effects of treatments on k values.
  - Tukey post-hoc tests for mean comparisons.
  - Two- and three-way ANOVAs (strain, temperature, material) to examine combined effects.
  - Regression diagnostics include R-squared (R²) and slope (gradient) reporting.
- Data validation: PCR verification of Salmonella strains used in the assays.

## Data structure and variables
- Variables common across files include:
  - Material: Plastic (PE) or Glass
  - Condition: Dry, Submerged, or water
  - UV: UV exposure (UV) or no UV (No_UV)
  - Time: Time after inoculation (Days for persistence/decline; Hours for Galleria assays)
  - Replicate: Replicate number
  - Concentration: Bacterial concentration (CFU/ml) or inocula
  - Survival: Galleria larval survival percentage
  - RSquared: Fit quality for regressions
  - Gradient: Slope of the response variable
  - K(Day-1): Die-off rate
  - D-value: Decimal reduction time (days)
- Data completeness: ND denotes missing data.

## Quality control and data provenance
- Rigorous QC: replication, statistical analyses (ANOVA, regression), and confirmatory PCR for strain identity.
- Instrumentation calibration: Plate reader and PCR thermocycler calibrated per standard protocols.
- Data collection and interpretation led by Michael Ormsby.
- Data and methods aligned with prior and related publications on plastics, UV stress, and environmental pathogens.

## How this data can be used (analyst perspective)
- Investigate how material type (PE vs. Glass), UV exposure, and environmental conditions influence Salmonella persistence and die-off rates.
- Compare die-off constants (k) and D-values across treatments to identify conditions that promote or hinder survival on surfaces.
- Examine whether persistence on plastics alters subsequent virulence in the Galleria mellonella model, including virulence of bacteria recovered from surfaces after extended exposure.
- Build predictive models to estimate environmental persistence under UV and surface conditions, informing public health risk assessments related to microbial hitchhikers on plastics.
- Integrate temperature data to assess potential interactions between environmental temperature fluctuations and bacterial persistence. 

## Completeness and accessibility
- Five CSV data files provide a complete set of persistence, virulence, and temperature measurements.
- Data were curated for anomalies; missing data labeled as ND.
- Datasets are suitable for meta-analyses or integration with related plastisphere studies and can support model validation or cross-study correlations.