# Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles

- Purpose of data
  - Examine adherence to and persistence of clinically relevant pathogenic Salmonella spp. on plastic and glass under environmentally relevant temperatures.
  - Assess virulence of recovered strains using a Galleria mellonella infection model.
  - Align with UKRI/NERC grant requirements on microbial hitchhikers in plastics.

- Study setting and timeframe
  - Location: Scotland, United Kingdom.
  - Experimental period: June to December 2023.

- Data collected and formats
  - Eight CSV files capturing: 
    - Persistence of Salmonella on plastic and glass at different temperatures.
    - Decline rates of Salmonella on these materials across temperatures.
    - Virulence in Galleria mellonella model.
    - Intercept, slope and R-squared values for decline rates.
    - Properties of water used for biofilm generation.
    - Inocula used in Galleria challenge controls.
    - R-squared/Gradient/K-value/Decline relationships for NER/related metrics.
    - Challenge doses of Salmonella in the Galleria model.
  - Data types include: bacterial counts (CFU/ml), survival percentages in larvae, time (days), temperatures (20/30/40 °C), materials (Glass, HDPE, PP), replicates, and concentration units.

- Methods overview (key procedures)
  - Biofilm assay: Salmonella strains grown in LB, exposed to surface water from Allan Water, incubated at 20/30/40 °C for 48 h; biofilms quantified by crystal violet.
  - Persistence assay: at 7/14/21/28 days, biofilms scraped, bacteria enumerated on selective agar; glycerol stocks prepared for Galleria tests; PCR confirms Salmonella identity (ttr gene).
  - Extraction control: assess extraction efficiency using known CFU on HDPE, PP, and glass.
  - Galleria mellonella virulence assay: larvae infected with Salmonella glycerol stocks; survival tracked for 72 h; negative controls include PBS and PBS-Glycerol.
  - Dose–response: pure culture dilutions from 10^2 to 10^9 CFU used to establish infectious-dose relationships.
  - Die-off modeling: log10 CFU/ml transformed; linear regression to derive die-off rate constant k (d^-1); decimal reduction time t90 calculated; ANOVA and Tukey tests for treatment effects; multi-way ANOVA for strain × temperature × material effects.
  - Regression and metrics: models described by log10(C) = log10(C0) − k t; outputs include Y-intercept, slope, R^2, and D-values.

- Data completeness and quality
  - Data checked for anomalies; missing values marked as ND (not determined).

- Responsible party and interpretation
  - Data collection and interpretation led by Michael Ormsby.
  - Data linked to the manuscript: Ormsby et al., Enduring pathogenicity of African strains of Salmonella on plastics and glass in simulated peri-urban environmental waste piles (J Hazard Mater, 2024).

- Data file contents at a glance
  - Persistence_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv: levels of persistence on plastic vs. glass across temperatures.
  - Decline_rates_of_Salmonella_on_plastic_and_glass_at_different_temperatures.csv: rates of decline over time on materials at varying temperatures.
  - Viurlence_in_Galleria_mellonella_model.csv: virulence measures of strains after recovery from materials.
  - Intercept_slope_and_R_squared_of_decline_rates.csv: regression parameters for decline-rate fits.
  - Properties_of_water_for_biofilm_generation.csv: characteristics of water used to generate natural biofilms.
  - Inocula_used_in_galleria_challenge_control.csv: concentrations used as inocula for controls in Galleria challenges.
  - R_squared_Gradient_K_value_D_value.csv: regression outputs related to minimum inhibitory concentrations and related metrics.
  - Challenge_doses_Salmonella_in_Galleria_model.csv: Salmonella concentrations used for Galleria challenge.
  
- Relevance and provenance
  - Data support the study on persistence and pathogenic potential of Salmonella on common plastics and glass under realistic environmental conditions.
  - Associated with the manuscript topic and funded under specific NERC grants addressing microbial hitchhikers in peri-urban waste environments.