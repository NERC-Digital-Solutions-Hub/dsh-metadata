# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

## Overview
- A data package supporting a study of how clinically relevant Salmonella spp. adhere to and persist on plastics and glass under environmentally relevant conditions, and their virulence in a Galleria mellonella infection model.
- Linked to UKRI NERC grants on microbial hitchhikers of marine plastics and SPACES project; data collected in Scotland (UK) during 2023 and described in a 2024 manuscript.

## Data collected and file structure
- Eight CSV data files:
  1. Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv — Salmonella persistence on plastic and glass across temperatures over time.
  2. Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv — Die-off rates (decline rates) under different temperatures.
  3. Viurlence_in_Galleria_mellonella_model.csv — Virulence levels of strains after recovery from surfaces in a G. mellonella model.
  4. Intercept_slope_and_R_squared_of_decline_rates.csv — Regression parameters for decline rates (intercept, slope, R^2).
  5. Properties_of_water_for_biofilm_generation.csv — Characteristics of water used to generate natural biofilms (e.g., source, quality).
  6. Inocula_used_in_galleria_challenge_control.csv — Concentrations of control inocula used for G. mellonella challenges.
  7. R_squared_Gradient_K_value_D_value.csv — Data related to minimum inhibitory concentrations (E. coli from plastic) and related regression metrics.
  8. Challenge_doses_Salmonella_in_Galleria_model.csv — Salmonella challenge doses used for G. mellonella experiments.
- Data dictionary and variable descriptions are embedded within the files, including detailed column mappings and units.

## Data collection location and timing
- Location: Scotland, United Kingdom.
- Time frame: Experiments conducted June–December 2023.

## Data collection and experimental methods
- Biofilm generation and quantification:
  - Salmonella strains grown in LB at 37°C, then inoculated into 96-well plates with LB or surface water, incubated at 20, 30, or 40°C for 48 h.
  - Biofilms quantified via crystal violet method; experiments conducted in biological triplicate.
- Persistence measurements:
  - At 7, 14, 21, and 28 days, surfaces were washed, scraped, and biofilm dispersed for enumeration on selective Salmonella media.
  - Galleria mellonella infection assays performed on glycerol stocks recovered from surfaces; PCR confirmation of Salmonella (ttr gene) used retrospectively.
  - Control challenges included PBS and PBS-Glycerol to account for handling and glycerol toxicity.
- Galleria mellonella virulence:
  - Larvae infected with defined Salmonella inocula, incubated at 37°C, survival tracked for 72 h.
  - Negative controls and dose–response series established to relate virulence to inoculum concentration.
- Die-off rate analysis:
  - CFU counts log10-transformed; linear regression (log10 C = log10 C0 − k t) used to derive die-off rate constant k (d−1) and decimal reduction time t90.
  - ANOVA and Tukey tests used to compare k values across treatments; multifactor ANOVAs (2- and 3-way) to examine strain, temperature, and material effects.

## Data structure and key variables
- Core experimental factors:
  - Strain (bacterial strain)
  - Material (Glass, HDPE, or PP)
  - Temperature (20, 30, or 40 °C)
  - Time (Days; for persistence measurements)
  - Concentration (CFU/ml; for inocula and challenges)
  - Replicate (experimental replicate)
- Outcome measures:
  - Persistence: CFU/ml on surfaces over time
  - Die-off: k value (per day), D-value (days to kill 90%)
  - Galleria virulence: Survival percentage of larvae
  - Predicted vs. observed survival linkage via dose–response and regression analyses
- Data descriptors in files include detailed metadata and units (e.g., Time in days, Temperature in °C, Concentration in CFU/ml, Survival in %).

## Data quality and completeness
- Completeness indicators:
  - ND marks missing data where applicable.
  - Data checked for anomalies; upper/lower bound checks performed.
- Quality controls:
  - Extraction efficiency validated using a defined model organism (strain D23580) on multiple materials.
  - Confirmatory PCR (ttr gene) performed to verify Salmonella identity for Galleria challenges.
  - Natural biofilms generated on materials to benchmark extraction and recovery.
- Miscellaneous notes:
  - Minor typographical inconsistencies in file naming (e.g., “Viurlence”), but contents clearly mapped to virulence data.

## Intended use and data integration
- Purpose: Enable data-driven exploration of Salmonella adhesion, persistence, and virulence across materials and temperatures; support self-serve data products and cross-study analyses.
- How to combine data:
  - Link Persistence and Decline rate files by Strain, Material, Temperature, and Time.
  - Integrate Galleria virulence data with persistence outcomes via recovered CFU and timepoint data.
  - Use the Intercept/Slope/R2 and D-value data to reproduce or compare die-off modeling.
  - Refer to the water properties file for contextual environmental conditions affecting biofilm formation.
- Analytical approaches reflected in the dataset:
  - Log-linear die-off modeling with k and t90
  - ANOVA to assess effects of strain, temperature, material
  - Dose–response relationships for Galleria infection to relate virulence to recovered bacterial loads

## Responsibility and provenance
- Data collected and interpreted by Michael Ormsby.
- Related manuscript: Ormsby et al., Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles. Journal of Hazardous Materials, 2024.

## Miscellaneous notes for reuse
- Data provenance and context available within the accompanying manuscript citation and dataset descriptions.
- The data package provides a comprehensive set of variables and regression metrics to facilitate replication and secondary analyses focusing on Salmonella plastic persistence and virulence under environmental conditions.