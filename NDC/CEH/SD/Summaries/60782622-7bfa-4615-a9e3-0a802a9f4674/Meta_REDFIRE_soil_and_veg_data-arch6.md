# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

- Overview
  - A dataset of soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, collected in 2016–2017.
  - Includes plot-level metadata, ambient dose rates, sampling details, vegetation and soil measurements, radionuclide activity concentrations (Sr-90, Cs-137, Am-241, Pu isotopes), uncertainties, and derived dose-rate calculations for multiple matrices.

- Data structure and key variables
  - Plot and location metadata
    - Plot_number, Plot_location, Northing, Easting
    - Plot_pine_forest_past_history (whether area is/was pine forest before 1986)
    - Plot_burn_score_2016 (0–3 scale for burn status in Sept 2016)
  - Ambient dose rates
    - Ambient_dose_rate_September_2016_µSv_per_h
    - Ambient_dose_rate_March_2017_µSv_per_h
  - Sampling information
    - Date_of_vegetation_and_soil_sampling (DD:MM:YY)
  - Vegetation measurements
    - Grassy_vegetation_sample_FM_g (fresh mass, grassy vegetation)
    - Grassy_vegetation_sample_DM_g (dry mass, grassy vegetation)
    - Grassy_vegetation_sample_DM_fraction (DM/FW ratio; note for plot 11.3 DM_fraction estimated from 11.1–11.2)
    - Other_vegetation_sample_FM_g, Other_vegetation_sample_DM_g
  - Soil measurements
    - Soil_%_DM_in_March_2017, Soil_%_DM_in_September_2017
    - Soil_pH_September_2017
    - Soil_%_LOI_September_2017
  - Activity concentrations (various matrices and isotopes)
    - Grassy vegetation (DM and FM) for Sr-90, Cs-137; Cs-137 and Sr-90 uncertainties; Am-241 and Pu isotopes (DM and FM) with either measured or predicted values
    - Tree wood (FM) for Sr-90, Cs-137, Am-241, Pu isotopes with measured or predicted values
    - Soil (DM) for Sr-90, Cs-137, Am-241, Pu isotopes
    - Uncertainties for activity concentrations (e.g., Sr-90 grassy vegetation DM, Cs-137 grassy vegetation DM, Am-241, Pu isotopes, etc.)
  - Dose-rate calculations (microgray per hour, µGy/h)
    - Internal and external weighted dose rates for each isotope across grassy vegetation, tree wood, and soil
    - Total weighted absorbed dose rates for each matrix (grassy vegetation, tree, and other aggregates)
    - Total internal and external dose rates for each isotope and for combined matrices (e.g., total grassy vegetation, total tree, total bacteria)
    - Totals by matrix (e.g., Total_weighted_absorbed_dose_rate_grassy_vegetation_µGy_per_h)
  - Transfer and modeling notes
    - Am-241 and Pu isotopes in grassy vegetation and Pinus sylvestris (wood) modeled using CR wo-soil transfer parameters from Agrostis gigantea and Pinus sylvestris (wood) with sources cited (Beresford et al. 2020; table 4)
    - Sr-90 and Cs-137 tree transfer parameters (CR wo-soil) derived from CEZ site data and Ukrainian references
  - Data quality indicators
    - Many fields marked n/a (data not available)
    - Some values described as predicted rather than measured (e.g., certain tree wood isotope concentrations)
    - Notes indicate estimated values and transfer parameters used to derive some concentrations and dose rates

- Data quality and interpretation notes
  - Substantial missing data (n/a) across many variables, especially for some isotopes, matrices, and uncertainties
  - Some dry-mass fractions and predicted concentrations were inferred or estimated (not always directly measured)
  - Transfer parameter sources are cited, enabling reproducibility if transfer models are applied
  - Units include Bq/kg (dry or fresh mass), µSv/h (ambient dose rate), and µGy/h (absorbed dose rates)

- Potential use cases for Data Support
  - Self-serve exploration of how radionuclide concentrations relate to ambient and calculated dose rates across plots, vegetation types, and soils
  - Building dashboards comparing grassy vegetation, tree wood, and soil isotopic burdens and their contributions to total dose rates
  - Time-mocused analyses by aligning sampling date with ambient dose rates and soil/vegetation measurements
  - Data cleaning and integration tasks to handle missing values, reconcile DM/FM mass data, and standardize units
  - Reproducibility studies using the documented transfer parameter sources (Beresford et al. 2020; CEZ Ukrainian data) to reproduce or extend dose-rate calculations
  - Identification of data gaps to inform future sampling or data collection efforts

- Practical considerations for data work
  - Expect frequent missing values and some model-based (predicted) concentrations
  - Pay attention to DM vs FM mass distinctions when interpreting activity concentrations
  - Ensure proper application of transfer parameters and cited references when deriving unmeasured concentrations or dose rates
  - Consider separating ambient dose-rate context from calculated dose-rate outputs to support clear storytelling and risk communication

- Alignment with Data Support archetype
  - The dataset provides a rich, multi-matrix, multi-isotope resource ideal for data discovery, combination, and visualization
  - Supports creating user-friendly products (dashboards, reports) that enable stakeholders to explore environmental radiological data and derived dose implications
  - Highlights typical data challenges faced in non-specialist data ecosystems (patchy data, diverse formats, cross-matrix calculations) and underscores the need for data curation and clear documentation