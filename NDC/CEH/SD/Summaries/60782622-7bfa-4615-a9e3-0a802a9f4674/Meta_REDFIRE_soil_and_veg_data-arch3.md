# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

- Purpose and scope
  - Provides a comprehensive dataset of radionuclide activity concentrations in soil and vegetation, and calculated dose rates, to support environmental health monitoring and policy evaluation.
  - Focuses on the Red Forest site in Chernobyl, Ukraine, with measurements collected in 2016 and 2017.

- Study site and sampling design
  - Plot-based data collection: each row includes Plot_number and Plot_location (with Northing and Easting).
  - Plots capture knowledge of local history and conditions: Plot_pine_forest_past_history (whether the area around the plot was/was not a pine forest before 1986) and Plot_burn_score_2016 (an objective burn status in September 2016).
  - Spatial context and quality control features: description fields and metadata notes to aid traceability.

- Measured variables and samples
  - Dose rates
    - Ambient_dose_rate_September_2016 (µSv/h)
    - Ambient_dose_rate_March_2017 (µSv/h)
    - Weighted_absorbed_internal_dose_rate and Weighted_absorbed_external_dose_rate (per isotope and per matrix; in µGy/h)
    - Total_weighted_absorbed_dose_rate (per isotope and per matrix; in µGy/h)
    - Total_grassy_vegetation_dose_rate, Total_tree_dose_rate, and Total_bacteria_dose_rate aggregates (µGy/h)
  - Vegetation samples
    - Grassy_vegetation_sample_FM_g (fresh mass)
    - Grassy_vegetation_sample_DM_g (dry mass) and DM_fraction (dry mass / fresh mass)
    - Other_vegetation_sample_FM_g and DM_g
    - Isotope activity concentrations in grassy vegetation (Bq/kg_DM and Bq/kg_FM) for Sr-90, Cs-137, Am-241, Pu-238/239/240
    - Uncertainties for activity concentrations (K=1.96) where provided
    - Predicted activity concentrations for Am-241 and Pu isotopes in grassy vegetation when measured values are unavailable
  - Tree (wood) samples
    - Activity concentrations in tree wood per DM and per FM for Sr-90, Cs-137, Am-241, Pu isotopes
    - Predicted values where direct measurements are unavailable
  - Soil samples
    - Activity concentrations in soil per DM for Sr-90, Cs-137, Am-241, Pu isotopes
    - Soil %DM (both March and September 2017)
    - Soil_pH_September_2017 (n/a in some entries)
    - Soil_LOI_September_2017 (Loss on Ignition)
  - Other measurements and derived metrics
    - Date_of_vegetation_and_soil_sampling (DD:MM:YY)
    - Soil properties such as DM fraction, pH, and LOI to support transfer and scaling calculations
  - Cross-isotope and cross-matrix relationships
    - Transfer-parameter-driven calculations (CR_wo_soil) used for Am-241 and Pu isotopes in grassy vegetation and Pinus sylvestris (wood)
    - Similar transfer-parameter approaches for Sr-90 and Cs-137 in tree material (from Ukrainian CEZ sites)

- Data completeness and quality notes
  - Many fields have n/a (data not available) entries, indicating incomplete data for certain plots or samples.
  - DM fraction for plot 11.3 was estimated from the average of 11.1 and 11.2 (not directly recorded).
  - Certain activity concentrations in grassy vegetation, tree wood, and some dose-rate figures are marked as predicted rather than measured.
  - Uncertainties are provided where available (K=1.96).

- Derived calculations and methodology
  - Internal and external dose-rate components are computed for grassy vegetation, tree wood, and other matrices, with total dose rates summarized per matrix and per isotope.
  - Weighted dose rates combine internal and external contributions to yield comprehensive exposure estimates for each ecological compartment.
  - The dataset integrates measured soil activity with vegetation and wood transfer parameters to estimate radionuclide uptake and resulting dose rates.

- Data provenance and references
  - Transfer-parameter bases and methodologies cited:
    - Am-241 and Pu isotopes in grassy vegetation and pine wood transfers from Beresford et al. 2020 (J Environ Radio, with DOI https://doi.org/10.1016/j.jenvrad.2018.02.007)
    - Sr-90 and Cs-137 tree transfer parameters from CEZ Ukrainian sites (source: https://doi.org/10.15407/jnpae2020.03.256)
  - These references underpin the predicted activity concentrations where direct measurements are unavailable.

- Relevance for monitoring frameworks
  - Demonstrates a structured approach to environmental health monitoring: multi-media (soil, grasses, trees), multi-isotope radiological assessment, and both measured and model-assisted (predicted) concentrations.
  - Includes explicit metadata elements (plot identifiers, coordinates, habitat history, burn status) and a clear timeline (2016–2017), aiding reproducibility and longitudinal assessment.
  - Highlights practical data governance considerations common in monitoring work: data gaps, reliance on metadata to verify data quality, and use of transfer-parameter models to fill gaps.
  - Provides a basis for policy-relevant interpretation of environmental radiological contamination and dose implications for vegetation and soil ecosystems, informing decision-making and future monitoring design.