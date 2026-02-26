# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

## Overview
- A study evaluating whether clinically relevant Salmonella spp. can adhere to and persist on plastic and glass under environmentally relevant temperatures and conditions, and the virulence of recovered strains using a Galleria mellonella infection model.
- Data support the UKRI-NERC grants on microbial hitchhikers in the plastisphere and related projects.
- Data collected in Scotland, UK, with experiments conducted between June and December 2023.

## Data collected and scope
- Eight CSV files capturing multiple experimental facets:
  - Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Viurlence_in_Galleria_mellonella_model.csv
  - Intercept_slope_and_R_squared_of_decline_rates.csv
  - Properties_of_water_for_biofilm_generation.csv
  - Inocula_used_in_galleria_challenge_control.csv
  - R_squared_Gradient_K_value_D_value.csv
  - Challenge_doses_Salmonella_in_Galleria_model.csv

## Study location and timing
- Data collected in Scotland, UK.
- Experimental period: June–December 2023.

## Experimental design and data collection methods
- Biofilm generation and quantification:
  - Salmonella strains grown in LB, inoculated into 96-well plates with LB or surface water (from Allan Water).
  - Surfaces: glass, HDPE, and PP (polypropylene).
  - Temperatures: 20, 30, and 40 °C; duration: 48 hours.
  - Biofilms quantified by crystal violet staining; experiments run in biological triplicate.
- Persistence assessment:
  - Sampling at 7, 14, 21, and 28 days after inoculation.
  - Surface scraping and suspension in PBS; serial dilutions and plating on selective agar (Bismuth sulphite) for CFU enumeration.
  - Glycerol stocks stored at -80 °C for later Galleria mellonella assays; confirmatory PCR on isolates using ttr gene as a Salmonella marker.
- Extraction efficiency and controls:
  - Natural biofilms formed on materials to test extraction efficiency with a known strain (D23580).
  - Additional controls including inocula recovered from glycerol stocks.
- Galleria mellonella virulence assays:
  - Larvae challenged with glycerol stocks or pure cultures across a range of doses (10^2 to 10^9 CFU).
  - Negative controls: PBS alone; PBS with 40% glycerol (PBS-G).
  - Survival monitored for 72 hours; experiments in biological triplicate.
  - Dose–survival relationships generated to compare infectious doses with recovered concentrations.
- Data analysis:
  - Die-off modelling: log10 CFU/ml transformed; linear regression to describe decline (log-linear model; C0, k; k is die-off rate in day^-1), and calculation of decimal reduction times (t90).
  - Statistical analyses: ANOVA to test effects of treatment on k; Tukey post-hoc tests; two- and three-way ANOVAs for interactions among strain, temperature, and material.
  - Regression outputs include intercepts, slopes, R^2 values, and related parameters.

## Data files contents (highlights)
- Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Levels of Salmonella persistence on plastic and glass at 20, 30, and 40 °C.
- Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Die-off rates (k values) and related decline-rate metrics across materials and temperatures.
- Viurlence_in_Galleria_mellonella_model.csv
  - Virulence metrics (survival) of Salmonella recovered from surfaces in the Galleria model.
- Intercept_slope_and_R_squared_of_decline_rates.csv
  - Regression parameters describing decline rate fits (intercept, slope, R^2) for each condition.
- Properties_of_water_for_biofilm_generation.csv
  - Characteristics of the surface water used for biofilm growth.
- Inocula_used_in_galleria_challenge_control.csv
  - Concentrations and details of inocula used as controls in Galleria challenges.
- R_squared_Gradient_K_value_D_value.csv
  - Data on regression-derived metrics including gradient, K (per day), and D-values; also notes on minimum inhibitory concentrations of E. coli isolated from plastic (contextual for related analyses).
- Challenge_doses_Salmonella_in_Galleria_model.csv
  - Salmonella challenge concentrations used for Galleria challenges.

## Completeness and data quality
- Data checked for anomalies; missing data is labeled as ND.
- Documentation provides detailed column descriptions and units for reproducibility.

## Provenance and relation to the manuscript
- Data linked to the manuscript: Ormsby MJ, White HL, Metcalf R, Oliver DM, Feasey NA, Quilliam RS. Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles. J Hazard Mater. 2024;461:132439.
- Principal data collector and interpreter: Michael Ormsby.
- Data intended to support open data reuse and transparency for environmental health monitoring of microbial hitchhikers on plastics.