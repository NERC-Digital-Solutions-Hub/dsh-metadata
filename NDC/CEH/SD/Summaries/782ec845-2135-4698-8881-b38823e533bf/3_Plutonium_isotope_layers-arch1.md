# Dataset: Soil Core Sampling and Radionuclide Activity Concentrations

- Purpose and scope
  - Captures per-sample data from 37 mm diameter soil cores with depth-layer measurements.
  - Records radionuclide activity concentrations (137Cs, 90Sr, 238Pu, 239+240Pu) in soil dry matter plus their relative uncertainties (95% CI).
  - Includes sampling depth structure, core dimensions, sampling area, and measurement dates.

- Key identifiers
  - Code_of_the_sample: Database serial number – unique ID.
  - Identifier_of_the_sample: UIAR unique label – chemical analysis number.
  - Dates_of_the_activity_measurements: Date of measurement (long date format). Units: dd-mmm-yy.

- Sampling geometry and depth
  - Sampling_area_m2: Size of the area sampled. Units: square metres.
  - The_top_border_of_a_layer_cm and The_bottom_border_of_a_layer_cm:
    - Layering scheme for 30 cm cores: 0-2, 2-4, 4-6, 6-8, 8-10, 10-15, 15-20, 20-25, 25-30 cm.
    - Note: One site sampled to 110 cm with core sectioned into 10 cm slices.
  - Mass_of_the_layer_kg: Mass of each layered sample from the 37 mm diameter core. Units: kilogram.

- Measured variables (per layer)
  - Activity_concentration_137Cs_Bqkg: 137Cs activity concentration (Bq/kg, soil dry matter).
  - Relative_uncertainty_of_specific_activity_of_137Cs_%: Uncertainty of 137Cs determination (95% CI, percent).
  - Activity_concentration_90Sr_Bqkg: 90Sr activity concentration (Bq/kg, soil dry matter).
  - Relative_uncertainty_of_specific_activity_of_90Sr_%: Uncertainty of 90Sr determination (95% CI, percent).
  - Activity_concentration_238Pu_Bqkg: 238Pu activity concentration (Bq/kg, soil dry matter).
  - Relative_uncertainty_of_specific_activity_of_238Pu_%: Uncertainty of 238Pu determination (95% CI, percent).
  - Activity_concentration_239_240Pu_Bqkg: 239+240Pu activity concentration (Bq/kg, soil dry matter).
  - Relative_uncertainty_of_specific_activity_of_239_240Pu_%: Uncertainty of 239+240Pu determination (95% CI, percent).

- Additional considerations
  - Core details: 37 mm diameter; depth layering as described; some sites extend beyond 30 cm (up to 110 cm) with 10 cm slices.
  - Uncertainties are provided for each radionuclide concentration, enabling uncertainty propagation in analyses.
  - Data fields may include blank units or notes where appropriate.

- Potential analytical uses for analysts
  - Construct vertical profiles of radionuclide activity by depth and layer.
  - Compare concentrations across radionuclides and assess relative abundances.
  - Link activity data with layer mass to derive standardized metrics (e.g., Bq/kg per layer).
  - Propagate measurement uncertainties into model fits and predictions.
  - Assess data quality and consistency across sites, depths, and sampling events.