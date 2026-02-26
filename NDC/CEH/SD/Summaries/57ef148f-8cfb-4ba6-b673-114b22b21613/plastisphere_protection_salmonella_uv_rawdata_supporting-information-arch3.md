# Persistence_Salmonella_UV_exposure.csv

## Overview
- A data-focused study examining the persistence and decline of Salmonella Typhimurium on plastic waste (LDPE) and glass under controlled UV and lighting conditions, plus assessment of virulence after recovery using a Galleria mellonella infection model.
- Data support environmental health monitoring needs: colonisation/persistence on surfaces, response to UV stress, die-off rates, and virulence changes over time.

## What has been recorded (data content)
- Five CSV files with measurements across materials, conditions, and time:
  - Persistence_Salmonella_UV_exposure.csv: persistence levels on PE plastic and glass under UV exposure; conditions include dry, submerged, and associated water.
  - Concentration_killing_curve_Galleria_control.csv: virulence data for wild-type Salmonella Typhimurium D23580 in Galleria mellonella.
  - Virulence_in_Galleria_mellonella_model.csv: virulence of Salmonella Typhimurium recovered from PE and glass in Galleria model.
  - Temperature_logger_data.csv: temperature measurements throughout the study.
  - Linear_decline_analysis.csv: die-off rate analyses, including rate constants and D-values.
- Variables covered: material (Plastic/Glass), condition (Dry/Submerged/Water), UV exposure (UV/No_UV), time (days or hours), concentration (CFU/ml or inocula), survival (%), replicates, regression metrics (R^2, gradient), and die-off parameters (k, D-value).

## Where and when data were collected
- Location: Scotland, UK.
- Timeframe: February to August 2024.

## How data were collected (methods)
- Lab-based experimental setup with controlled photoperiod: 4 h white light; 4 h UV (UV index 8); 4 h white light; 12 h darkness.
- UV exposure delivered via bespoke frames using specific lamps; temperatures monitored hourly with i-Button loggers.
- Inoculation of Salmonella Typhimurium onto glass and LDPE surfaces in nutrient-rich and surface-water environments.
- Sampling at 1, 2, 3, 6, 8, 10, 14, and 21 days after inoculation for persistence; parallel Galleria mellonella virulence assays over 72 h.
- Galleria assays used a range of inocula (10^3–10^12 CFU) to determine infectious dose; negative PBS controls included.
- Bacterial enumeration via PBS suspensions, serial dilutions, and plating on LB-chloramphenicol; confirmatory PCR for Salmonella identity (ttr target).

## Experimental design and sampling regime
- Repeats: biological triplicate for persistence and virulence assessments; multiple replicates per condition.
- Die-off modelling: log10 CFU vs time to derive die-off rate constants (k, day^-1) and decimal reduction times (t90).
- Statistical analyses: ANOVA to test treatment effects on k; Tukey post-hoc tests for pairwise comparisons; two- and three-way ANOVAs to explore interactions among strain, temperature, and material (via SPSS v28).

## Data structure and file contents
- Each CSV file corresponds to a distinct experimental variable:
  - Persistence_Salmonella_UV_exposure.csv: persistence levels across material types, UV exposure, and surface conditions.
  - Concentration_killing_curve_Galleria_control.csv: virulence data from Galleria control challenges.
  - Virulence_in_Galleria_mellonella_model.csv: virulence data from recovered Salmonella on PE and Glass.
  - Temperature_logger_data.csv: hourly temperature data throughout the study.
  - Linear_decline_analysis.csv: regression outputs for decline rates, including RSquared, Gradient, K (day^-1), and D-values.
- Data columns include: Material, Condition, UV, Time, Concentration, Replicate, Survival, plus regression/fit metrics (RSquared, Gradient, K, D-value).

## Why data were collected
- To evaluate how a clinically relevant human pathogenic strain of Salmonella Typhimurium adheres to and persists on plastic waste and withstands environmental UV exposure.
- To assess changes in virulence after environmental exposure, informing environmental health monitoring and risk assessment under real-world conditions.
- To fulfil UKRI NERC-funded research on the Plastisphere and related environmental-microbial spillover concerns.

## Data quality, completeness, and governance
- Quality controls: biological triplicates; replication checks; statistical analyses (ANOVA, regression); confirmatory PCR (ttr gene) for strain verification; instrument calibration (plate reader, thermocycler).
- Completeness: missing data labeled as "ND" where applicable.
- Data governance notes: underlying data are shared as CSVs; some data may be restricted or require explicit sharing permissions; data provenance and metadata are described within the dataset documentation and associated methods.

## Relevance to monitoring frameworks (policy and practice)
- Key environmental health indicators:
  - Surface persistence of pathogens (plastic vs glass) under UV stress.
  - Die-off kinetics (k, t90, D-values) under environmental conditions.
  - Virulence potential after environmental exposure.
- Metadata and governance considerations highlighted:
  - Clear variable descriptions, units, replicates, and data structure to facilitate reuse in monitoring dashboards.
  - Emphasis on data provenance, quality control, and the need for open, well-documented datasets to support evidence-informed policy decisions.
  - Addresses common monitoring-framing challenges: data availability, standardisation, and data-sharing barriers, with explicit file-level and variable-level documentation.