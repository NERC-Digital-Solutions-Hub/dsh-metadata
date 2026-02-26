# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

## Overview
- A dataset from a study on Salmonella spp. ability to adhere to and persist on plastic and glass under environmentally relevant temperatures, with virulence assessed in a Galleria mellonella infection model.
- Collected in Scotland, UK, from Allan Water, June–December 2023.
- Comprises eight CSV files detailing persistence, decline rates, virulence, regression metrics, and material/water parameters, aligned with a manuscript: Ormsby et al., J Hazard Mater. 2024.

## Data content and structure
- Eight CSV files:
  - Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Viurlence_in_Galleria_mellonella_model.csv
  - Intercept_slope_and_R_squared_of_decline_rates.csv
  - Properties_of_water_for_biofilm_generation.csv
  - Inocula_used_in_galleria_challenge_control.csv
  - R_squared_Gradient_K_value_D_value.csv
  - Challenge_doses_Salmonella_in_Galleria_model.csv
- Key variables (across datasets):
  - Strain (bacterial strain)
  - Material (Glass, HDPE, PP)
  - Time (Days)
  - Temperature (20, 30, or 40 °C)
  - Concentration (CFU/ml)
  - Replicate
- Derived metrics and related data:
  - Die-off parameters (k, t90, D-value)
  - Linear regression outputs (Intercept, Slope, R-squared)
  - Galleria survival (Survival_actual, Survival_expected)
  - Inocula concentrations and challenge doses
  - Water properties used for biofilm generation
  - Gradient/K-value and D-value context for related microbial analyses
- Data completeness:
  - Missing data labeled as ND

## Data collection context
- Location: Scotland, UK (Allan Water surface water used for experiments)
- Timeframe: June–December 2023
- Purpose: fulfill UKRI NERC grants on microbial hitchhikers of marine plastics and related projects

## Methods and measurements
- Biofilm assays:
  - Salmonella strains cultured, exposed to surface water or LB, incubated at 20, 30, 40 °C for 48 h
  - Biofilms quantified using crystal violet
  - Experiments conducted in biological triplicate
- Persistence assays:
  - Inoculated surfaces (HDPE, PP, glass); timepoints at 7, 14, 21, 28 DAI
  - Biofilms dispersed; CFU enumerated on selective agar
  - Glycerol stocks stored for subsequent Galleria assays
  - PCR validation (ttr gene) for Salmonella identification
- Galleria mellonella virulence assays:
  - Larvae challenged with Salmonella recovered from surfaces
  - Controls: PBS, PBS-G ( glycerol toxicity control ), and pure culture dose ranges
  - Survival monitored for 72 h
  - Dose–response data used to compare to recovered concentrations
- Die-off and regression analysis:
  - CFU/ml log10-transformed; linear regression to model decline
  - Calculation of die-off rate constant (k) and decimal reduction times (t90)
  - ANOVA for treatment effects; Tukey post-hoc tests; SPSS used for multi-factor analyses

## GIS-relevant aspects and potential uses
- Spatial visualization opportunities:
  - Map persistence and die-off dynamics across material types (Glass, HDPE, PP) and temperatures as a spatial-analog of environmental plastics studies (Plastisphere).
  - Temporal trends (days) and temperature effects can be represented as time-aware layers or animated maps.
  - Potential to integrate with environmental geospatial datasets (locations of peri-urban waste piles, water bodies) to explore risk zones.
- Data for map-based indicators:
  - Die-off constants (k), D-values, and predicted survival percentages enable creation of risk surfaces or trend maps.
  - Virulence indicators from Galleria model could inform risk stratification alongside persistence metrics.
- Practical data integration:
  - Variables are clearly defined and structured for GIS-friendly joins (Strain, Material, Time, Temperature, Concentration).
  - Derived metrics (Intercept, Slope, R-squared; k; t90; Survival_expected) ready for thematic mapping and simple dashboards.

## Data quality, provenance, and completeness
- Collected and interpreted by Michael Ormsby; linked to the referenced manuscript.
- Data checked for anomalies; ND denotes missing values.
- PCR validation performed to confirm Salmonella identity in infection-relevant isolates.

## Limitations and considerations for GIS use
- Lab-based, controlled-environment data rather than direct field spatial data; spatial analysis would require integration with real-world environmental geodata.
- Temporal sampling is within a laboratory timeframe, not natural dispersal dynamics.
- Some datasets include non-Salmonella-related measurements (e.g., E. coli gradient data) that may require careful filtering for Salmonella-focused GIS analyses.

## Related documentation
- Manuscript: Ormsby MJ, White HL, Metcalf R, Oliver DM, Feasey NA, Quilliam RS. Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles. J Hazard Mater. 2024;461:132439.