# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

## Overview
- A dataset describing the persistence, decline rates, and virulence of Salmonella spp. recovered from plastic and glass under environmentally relevant conditions.
- Data collected in Scotland, UK, between June and December 2023 to study adherence, persistence, and pathogenic potential using a Galleria mellonella infection model.
- Associated with UKRI NERC grants investigating microbial hitchhikers on plastics; linked to a manuscript in J Hazard Materials (2024).

## Data files
- Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Levels of Salmonella persistence on plastic and glass at 20, 30, and 40 °C over time.
- Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv
  - Die-off rates (k) and related metrics derived from log-linear decline models.
- Viurlence_in_Galleria_mellonella_model.csv
  - Virulence outcomes for Salmonella strains recovered from materials in the Galleria mellonella infection model.
- Intercept_slope_and_R_squared_of_decline_rates.csv
  - Regression parameters (intercept, slope, R^2) for decline-rate analyses.
- Properties_of_water_for_biofilm_generation.csv
  - Characteristics of water used to generate natural biofilms on test materials.
- Inocula_used_in_galleria_challenge_control.csv
  - Concentrations of controls used for Galleria mellonella challenges.
- R_squared_Gradient_K_value_D_value.csv
  - Data related to minimum inhibitory concentrations of E. coli isolated from plastic samples.
- Challenge_doses_Salmonella_in_Galleria_model.csv
  - Salmonella challenge concentrations used for Galleria mellonella survival experiments.

## Collection context
- Location: Scotland, UK.
- Timeframe: Experiments conducted from June to December 2023.
- Study aim: Assess the ability of clinically relevant human pathogenic Salmonella spp. to adhere to and persist on plastic and glass under varying temperatures, and to evaluate virulence after recovery via a Galleria mellonella model.
- Data scope: Includes both persistence on abiotic surfaces and virulence outcomes post-recovery, plus derived statistical parameters.

## Methods and analysis
- Biofilm generation and quantification:
  - Salmonella strains grown in LB, then exposed to fresh LB or surface water in 96-well plates; incubated at 20, 30, or 40 °C for 48 h.
  - Biofilms quantified by crystal violet assay; experiments in biological triplicate.
- Persistence assays:
  - At 7, 14, 21, and 28 days after inoculation, surfaces sampled and Salmonella enumerated on selective agar (Bismuth sulphite).
  - Samples stored for Galleria mellonella infection assays; PCR validation performed on isolates (ttr gene targeted).
- Galleria mellonella virulence assays:
  - Larvae challenged with Salmonella glycerol stocks; controls included PBS and PBS-G (glycerol).
  - Infections conducted with varying inocula to relate dose to larval survival over 72 h; experiments in biological triplicate.
- Data transformation and modeling:
  - Die-off rates calculated from log10 CFU counts using a log-linear model: log10(C) = log10(C0) − k t.
  - Decimal reduction times (t90) derived from decline rates.
  - Statistical analyses included ANOVA (for k values) and Tukey post-hoc tests; two- and three-way ANOVAs to assess interactions between strain, temperature, and material.
- Quality controls and validation:
  - PCR confirmation of Salmonella identity; extraction efficiency checks using a standardized model biofilm on different materials (HDPE, PP, glass).
  - Inocula and controls thoroughly documented to ensure reproducibility.

## Metadata and data quality
- Data are stored as eight CSV files with explicit variable descriptions and units.
- Key variables documented: Strain, Material (Glass, HDPE, PP), Replicate, Time (Days), Temperature (20, 30, 40 °C), Concentration (CFU/ml), survival metrics, and derived statistics (Y-intercept, Slope, Rsquared, K, D-value).
- Completeness:
  - Data were checked for anomalous values; missing data are marked as ND.
- Documentation detail:
  - Comprehensive column descriptions and unit definitions accompany the datasets to support reuse and interpretation.
- Related data points:
  - Includes data for water properties, inocula, and challenge doses to enable full replication of experimental design.

## Provenance and governance
- Data collection and interpretation credited to Michael Ormsby.
- Data tied to a specific manuscript: Ormsby MJ, White HL, Metcalf R, Oliver DM, Feasey NA, Quilliam RS. Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles. J Hazard Mater. 2024;461:132439.
- Data sharing and reuse context:
  - Datasets are linked to the manuscript and intended for broader dissemination via relevant data portals; licensing details are not specified in the provided text.

## Usage notes and caveats
- The dataset combines raw measurements (persistence counts, biofilm/virulence data) with derived statistics (k, t90, regression parameters).
- The presence of ND entries indicates gaps or missing measurements that may require clarification before re-analysis.
- Results are contextualized within a broader study of Salmonella persistence on plastics and glass under environmental exposure and environmental waste scenarios; consider aligning reuse with the accompanying manuscript for interpretive guidance.