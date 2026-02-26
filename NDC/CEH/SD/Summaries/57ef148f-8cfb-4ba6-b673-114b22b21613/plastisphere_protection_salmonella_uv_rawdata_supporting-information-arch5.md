# Persistence and virulence of Salmonella Typhimurium on plastic and glass under UV exposure

## Overview
- Investigates persistence, decline rates, and virulence of a clinically relevant Salmonella Typhimurium strain on plastic (PE/LDPE) and glass under a defined light regime with UV exposure.
- Includes virulence assessment in Galleria mellonella larvae.
- Data collected in Scotland, UK, between February and August 2024.
- Dataset supports understanding of how plastic waste and environmental UV stress affect Salmonella persistence and pathogenicity.

## What has been recorded and how the data are structured
- Five CSV data files:
  - Persistence_Salmonella_UV_exposure.csv: persistence levels on plastic and glass under UV exposure (dry, submerged, and surrounding water).
  - Concentration_killing_curve_Galleria_control.csv: virulence data for wild-type S. Typhimurium D23580 in Galleria mellonella infection model.
  - Virulence_in_Galleria_mellonella_model.csv: virulence data for S. Typhimurium recovered from PE and glass in Galleria infection model.
  - Temperature_logger_data.csv: temperature measurements across the study duration.
  - Linear_decline_analysis.csv: die-off rate characteristics (k values, D-values, etc.).
- Data columns (examples):
  - Material (Plastic/Glass), Condition (Dry/Submerged/Water), UV (UV/No_UV), Time (Days or Hours), Concentration (CFU/ml), Survival (%), Replicate, Temperature, R-Squared, Gradient, K (Day^-1), D-value (Days).
- Replicates: biological triplicate for key experiments; multiple replicates documented per condition.
- Data completeness: ND used to indicate missing data.
- Units: clearly specified per file and variable (e.g., CFU/ml, % survival, Days, Hours, Days^-1, etc.).

## Experimental design and data collection details
- Experimental setup:
  - Inoculation of Salmonella Typhimurium onto materials in nutrient-rich and surface water environments.
  - Photoperiod: 4 h white light; 4 h UV (UV index 8); 4 h white light; 12 h darkness.
  - UV exposure applied via bespoke frames with controlled light sources; samples incubated in controlled conditions.
  - Temperature data logged hourly using an iButton temperature logger.
- Sampling schedule:
  - 1, 2, 3, 6, 8, 10, 14, and 21 days after inoculation (DAI) for persistence assessments.
  - Galleria mellonella virulence assays conducted with dose ranges from 10^3 to 10^12 CFU; survival monitored for 72 hours.
  - Additional 21-day material samplings used to recover bacteria for Galleria challenges.
- Analytical approaches:
  - Die-off rates calculated with log10 transformations and linear regression (log10 C = log10(C0) − k t).
  - Decimal reduction times (t90) derived from k values.
  - ANOVA to test treatment effects on k; Holm-Šídák post-hoc for multiple comparisons.
  - Two- and three-way ANOVAs Examining effects of strain, temperature, and material.
  - Regression and ANOVA performed in Minitab v18; PCR verification targeting ttr gene for Salmonella identity.
- Virulence assessment:
  - Galleria assays used to determine pathogenicity after recovery from PE and glass surfaces.
  - Controls included PBS-injected larvae to account for handling mortality.

## Data governance, quality control, and provenance
- Quality control measures:
  - Biological triplicates; replication across conditions.
  - Confirmatory PCR for strain verification; calibration of plate reader and PCR thermocycler.
  - Temperature logging and environmental controls to maintain consistency.
- Documentation and metadata:
  - Detailed descriptions of each dataset file, variable descriptions, and units provided within the data files.
  - Replicate identifiers (R1, R2, etc.) and clear labeling of materials (Plastic/Glass) and conditions (Dry/Submerged/Water; UV exposure).
- Provenance:
  - Data collected under UKRI NERC grants related to the plastisphere and environmental persistence studies; authorship attributed to Michael Ormsby and collaborators.
  - Related publications cited for methodological context and validation.

## Completeness, limitations, and notes for data users
- Completeness:
  - Data files cover persistence, virulence, temperature, and decline analysis; missing data explicitly labeled as ND.
- Limitations:
  - Some data described as “data not shown” in related references; dataset includes core quantitative measurements with documented QA steps.
- Reuse considerations:
  - Clear linkage between experimental conditions and data columns enables replication of die-off modeling and virulence assessments.
  - Metadata-rich files facilitate traceability of methods, materials, and timepoints for Data Stewards and secondary analysis.
- Context and references:
  - Related methodological and ecological context provided via cited works on plastisphere persistence and environmental pathogens.