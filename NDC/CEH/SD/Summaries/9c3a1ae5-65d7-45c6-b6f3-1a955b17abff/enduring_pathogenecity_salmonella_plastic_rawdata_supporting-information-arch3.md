# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

## Purpose and data structure
- Study data record the ability of clinically relevant Salmonella spp. to adhere to, persist on, and cause virulence after recovery from plastic and glass surfaces under environmentally relevant temperatures.
- Data are organized into eight CSV files covering: persistence on plastic/glass at不同 temperatures, decline rates, virulence in a Galleria mellonella model, regression metrics (intercept, slope, R²), properties of water used for biofilm generation, inocula for Galleria challenges, gradient/K-values and D-values, and challenge doses.

## Data collection location and timing
- Location: Scotland, United Kingdom.
- Timeframe: Experiments conducted from June to December 2023.

## Methods and experimental design
- Biofilm generation and quantification:
  - Salmonella strains cultured in LB (37 °C), then inoculated into fresh LB or surface water ( Allan Water) in 96-well plates.
  - Incubation at 20, 30, or 40 °C for 48 h.
  - Biofilms quantified by crystal violet method; experiments conducted in biological triplicate.
- Persistence assessment:
  - At 7, 14, 21, and 28 days after inoculation, surfaces were scraped, biofilm dispersed in PBS, and serial dilutions plated on selective Bismuth sulphite agar for Salmonella enumeration.
  - Remaining suspension stored with glycerol for later Galleria infections.
  - Confirmatory PCR (ttr gene) performed to validate Salmonella identity from glycerol stocks.
- Extraction efficiency check:
  - Natural biofilms formed on HDPE, PP, and glass; CFU recovery evaluated to ensure comparable extraction across materials.
- Galleria mellonella virulence assay:
  - Larvae challenged with glycerol-stock Salmonella; controls included PBS and PBS-G (glycerol) to account for procedural toxicity.
  - Dose-ranging: 10^2 to 10^9 CFU; survival monitored for 72 h.
  - Experiments conducted in biological triplicate.
- Inocula and controls:
  - Inoculum controls and LD/ dose series prepared from pure cultures; larvae infected via hemocoel injection.
- Die-off rate analysis:
  - CFU counts log10-transformed; linear regression to model die-off over time.
  - Model: log10(C) = log10(C0) − k t, with k as die-off rate constant (d^-1) and t90 derived from k.
  - ANOVA used to test treatment effects on k; Tukey tests for pairwise comparisons.
  - Two- and three-way ANOVAs (strain, temperature, material) to analyze combined effects.

## Why the data were collected
- To evaluate adherence, persistence, and pathogenic potential of Salmonella spp. on plastics and glass under environmentally relevant temperatures.
- To satisfy UKRI/NERC funding requirements for projects on microbial hitchhikers of marine plastics and related environmental processes.

## Data stewardship and attribution
- Data collection and interpretation led by Michael Ormsby.
- Completeness: missing data flagged as “ND”; data checked for anomalies and upper/lower bounds.
- Metadata and data descriptions are included within the data files to support reuse and verification.

## Data files and contents
- Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv (14 KB): levels of persistence on plastic and glass at 20, 30, and 40 °C.
- Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv (3 KB): rate of decline (die-off) over time for each condition.
- Viurlence_in_Galleria_mellonella_model.csv (7–9 KB): virulence outcomes of Salmonella recovered from surfaces in the Galleria model.
- Intercept_slope_and_R_squared_of_decline_rates.csv (1 KB): regression parameters for die-off rate fits.
- Properties_of_water_for_biofilm_generation.csv (2 KB): characteristics of water used to generate natural biofilms.
- Inocula_used_in_galleria_challenge_control.csv (5 KB): concentrations and details of inocula used as controls for Galleria challenges.
- R_squared_Gradient_K_value_D_value.csv (7 KB): regression metrics including gradient (slope), R², K (day^-1), and D-values; includes data on E. coli MICs isolated from plastic.
- Challenge_doses_Salmonella_in_Galleria_model.csv (3 KB): Salmonella challenge concentrations used for Galleria infections.
- Each file includes: strain, material (Glass, HDPE, PP), replicate, time, temperature (20/30/40 °C), concentration (CFU/ml), survival metrics, and associated statistical descriptors (intercepts, slopes, R², D-values) as applicable.

## Related publication
- This dataset supports the manuscript: Ormsby MJ, White HL, Metcalf R, Oliver DM, Feasey NA, Quilliam RS. Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles. J Hazard Mater. 2024;461:132439. DOI: 10.1016/j.jhazmat.2023.132439.