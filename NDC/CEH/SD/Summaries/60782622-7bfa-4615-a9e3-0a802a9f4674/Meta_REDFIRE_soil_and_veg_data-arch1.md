# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- A dataset detailing soil and vegetation radionuclide activity concentrations and calculated dose rates across plots in the Red Forest, Chernobyl, during 2016–2017.
- Includes ambient dose rates, vegetation and soil sampling data, and derived dose-rate calculations for multiple radionuclides.

## Data scope and measurements
- Plot and location information
  - Plot_number, Plot_location, Northing, Easting
  - Plot_pine_forest_past_history (whether the area is currently or was pine forest prior to 1986)
  - Plot_burn_score_2016 (burn status: 1 none, 2 some burnt, 3 all burnt)
- Ambient dose rates
  - Ambient_dose_rate_September_2016_µSv_per_h
  - Ambient_dose_rate_March_2017_µSv_per_h
- Sampling details
  - Date_of_vegetation_and_soil_sampling
  - Grassy_vegetation_sample_FM_g, Grassy_vegetation_sample_DM_g
  - Grassy_vegetation_sample_DM_as_fraction
  - Other_vegetation_sample_FM_g, Other_vegetation_sample_DM_g, Other_vegetation_sample_DM_as_fraction
- Soil and vegetation composition
  - Soil_%_DM_in_March_2017, Soil_%_DM_in_September_2017
  - Soil_pH_September_2017
  - Soil_%_LOI_September_2017
- Activity concentrations (radionuclides)
  - Grassy vegetation (DM and FM where available)
    - Sr-90, Cs-137 activity concentrations (Bq/kg_DM and FM/DM context)
    - Uncertainties for Sr-90 and Cs-137 in grassy vegetation (K=1.96)
    - Am-241, Pu-238, Pu-239, Pu-240 concentrations (DM and FM context; many entries labeled as predicted)
  - Tree (deciduous) wood
    - Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240 concentrations (DM or FM context; many entries predicted)
  - Soils
    - Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240 concentrations (Bq/kg_DM)
- Derived dose-rate calculations
  - Weighted_absorbed_internal_dose_rate for Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240 to grassy vegetation, tree wood, bacteria (µGy/h; many entries marked as n/a)
  - Weighted_absorbed_external_dose_rate for the same isotopes and matrices (µGy/h; many entries marked as n/a)
  - Total_weighted_absorbed_dose_rate for each isotope and for combined grassy vegetation, tree, and overall (µGy/h; many entries marked as n/a)
  - Totals for internal + external dose rates by matrix (grassy vegetation, tree, bacteria) and overall
- Annotations and data notes
  - Some DM fractions and concentrations are estimated (e.g., plot 11.3 DM fraction from plots 11.1 and 11.2)
  - Several concentration values are labeled as predicted, derived from transfer parameters rather than direct measurement
  - Uncertainty values provided where applicable (K=1.96)
  - Specific transfer parameter sources noted in footnotes

## Methodology, assumptions, and data sources
- Transfer parameter approaches
  - Am-241 and Pu isotopes for grassy vegetation and Pinus sylvestris (wood) use site-specific CR wo-soil transfer parameters from Beresford et al. 2020 (and related Journal of Environmental Radioactivity reference).
  - Sr-90 and Cs-137 transfer parameters for deciduous trees (from CEZ site in Ukraine) used with measured soil DM concentrations.
- Data derivation
  - Internal and external dose rates calculated by combining activity concentrations with transfer parameters and geometry per matrix (grassy vegetation, tree wood, bacteria) where available
  - Some dose-rate values are not available (n/a) due to lack of data or because certain isotopes were not measured or not estimated for specific matrices
- Uncertainty handling
  - Uncertainties provided for grassy vegetation with Sr-90 and Cs-137 (K=1.96)
- Data provenance
  - Ambient dose rates and sampling dates are explicit; many vegetation and soil isotope concentrations rely on DM (dry mass) or FM (fresh mass) contexts
  - References and links provided for the transfer-parameter sources

## Data quality, gaps, and caveats
- Missing data
  - Numerous fields marked n/a (data not available) for several isotopes, matrices, and dose-rate components
- Estimations and predictions
  - Some activity concentrations and dose-rate components are predicted rather than experimentally measured
  - DM fractions and some concentration values are inferred or estimated (e.g., plot 11.3)
- Finite scale and scope
  - Local-scale study focused on plots within the Red Forest; generalisability may be limited to similar contexts
- Potential biases
  - Use of transfer parameters from specific sites may introduce site-specific biases when extrapolating to other plots or species

## Potential analyses and applications
- Correlation and regression analyses linking ambient dose rates with vegetation/soil activity concentrations and dose-rate estimates
- Comparison of grassy vegetation versus tree wood uptake and their contributions to internal and external dose rates
- Assessment of the impact of pine forest history and burn status on radionuclide distribution and dose rates
- Sensitivity analyses around the predicted concentrations and transfer-parameter assumptions
- Environmental risk assessment and dose reconstruction for flora, with potential extension to ecological pathways

## Key references and data notes
- Transfer parameter sources:
  - Am-241 and Pu isotopes for grassy vegetation and pine wood: Beresford et al. 2020 (and related J Environ Radioact reference)
  - Sr-90 and Cs-137 transfer parameters for deciduous trees: CEZ Ukrainian site; referenced publication links provided
- Additional notes:
  - Data entries marked as “n/a” indicate not applicable or missing
  - Asterisks and hashes reference methodological notes about using specific site data and literature for transfer parameters