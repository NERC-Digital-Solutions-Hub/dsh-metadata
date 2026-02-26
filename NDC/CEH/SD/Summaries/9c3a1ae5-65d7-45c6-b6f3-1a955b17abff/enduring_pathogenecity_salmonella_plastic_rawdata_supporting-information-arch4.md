# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

## What has been recorded and what form does the data take?
- Eight CSV data files recording Salmonella persistence, decline rates, virulence, and related metrics.
  - Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Viurlence_in_Galleria_mellonella_model.csv
  - Intercept_slope_and_R_squared_of_decline_rates.csv
  - Properties_of_water_for_biofilm_generation.csv
  - Inocula_used_in_galleria_challenge_control.csv
  - R_squared_Gradient_K_value_D_value.csv
  - Challenge_doses_Salmonella_in_Galleria_model.csv
- Column descriptions cover: Strain, Material, Replicate, Time, Temperature, Concentration (CFU/ml), Survival (actual/expected), Y-intercept, Slope, R-squared, Inocula details, timepoints, and related metadata.

## Where were the data collected?
- Scotland, UK.

## When were the data collected?
- Experiments conducted between June and December 2023.

## How were the data collected?
- Biofilm assay:
  - Salmonella strains cultured in LB, then exposed to fresh LB or surface water in 96-well plates at 20, 30, or 40 °C for 48 h.
  - Surface water sourced from Allan Water, Scotland.
  - Biofilms quantified by crystal violet method; experiments in biological triplicate.
- Persistence measurements:
  - 7, 14, 21, and 28 days after inoculation (DAI).
  - Biofilms scraped, dispersed, and enumerated on selective agar for Salmonella; glycerol stocks stored at -80 °C for later Galleria mellonella assays.
  - PCR validation using ttr gene to confirm Salmonella identity.
  - Extraction efficiency assessed with a controlled contamination on HDPE, PP, and glass surfaces.
- Galleria mellonella virulence assays:
  - 10 µl glycerol-stock injections into larvae, with controls (PBS, PBS-G), conducted in biological triplicate.
  - Survival tracked for 72 h at 37 °C; dose-response experiments using 10-fold dilutions of Salmonella (10^2 to 10^9 CFU).
- Die-off rate analysis:
  - CFU counts log10-transformed; linear regression to model log-linear die-off: log10(C) = log10(C0) − k t.
  - Calculations include decimal reduction times (t90) and ANOVA (k values); additional two- and three-way ANOVAs (strain, temperature, material) in SPSS.

## Why were the data collected?
- To study adherence and persistence of clinically relevant Salmonella spp. on plastic and glass under environmentally relevant temperatures.
- To fulfil UKRI NERC grant requirements for projects on microbial hitchhikers of marine plastics and related environmental contexts.

## Who was responsible for the collection and interpretation of data?
- Michael Ormsby.

## Completeness. Are any data absent from the dataset?
- Data were checked for anomalies; missing data recorded as "ND".

## Data file contents
- Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Levels of Salmonella persistence on plastic and glass at 20, 30, and 40 °C.
- Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Rates of decline (die-off) of Salmonella over time under different temperatures and materials.
- Viurlence_in_Galleria_mellonella_model.csv
  - Virulence data of strains after recovery from surfaces, in a Galleria mellonella infection model.
- Intercept_slope_and_R_squared_of_decline_rates.csv
  - Regression parameters (intercept, slope, R^2) for decline-rate models.
- Properties_of_water_for_biofilm_generation.csv
  - Characteristics of water used to generate natural biofilms.
- Inocula_used_in_galleria_challenge_control.csv
  - Concentrations of inocula used for Galleria mellonella challenges and controls.
- R_squared_Gradient_K_value_D_value.csv
  - Data on minimum inhibitory concentrations and related regression statistics (R^2, gradient, K value, D value).
- Challenge_doses_Salmonella_in_Galleria_model.csv
  - Salmonella inocula concentrations used for Galleria challenges.

## Miscellaneous
- Related manuscript: Ormsby MJ, White HL, Metcalf R, Oliver DM, Feasey NA, Quilliam RS. Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles. J Hazard Mater. 2024;461:132439.