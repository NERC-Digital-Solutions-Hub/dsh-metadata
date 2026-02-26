# Dataset Schema for Soil Core Sampling and Radioisotope Activity Concentrations (137Cs, 90Sr, Pu)

- Overview
  - Data dictionary for environmental monitoring of radionuclide activity in soil cores.
  - Records include unique sample identifiers, sampling details, depth layering, masses, and activity concentrations with uncertainties.

- Data fields and structure
  - Code_of_the_sample: Database serial number (unique ID).
  - Identifier_of_the_sample: UIAR unique label (chemical analysis number).
  - Dates_of_the_activity_measurements: Date of measurement (dd-mmm-yy format).
  - Sampling_area_m2: Size of the area sampled (square metres).
  - The_top_border_of_a_layer_cm / The_bottom_border_of_a_layer_cm: Depth bounds of each soil layer (cm). Core design uses 30 cm segments with layers such as 0-2, 2-4, 4-6, 6-8, 8-10, 10-15, 15-20, 20-25, 25-30 cm; one site extends to 110 cm with 10 cm slices.
  - Mass_of_the_layer_kg: Mass of each layer (kg) for a 37 mm diameter core.
  - Activity_concentration_137Cs_Bqkg: 137Cs activity concentration in soil dry matter (Bq/kg).
  - Relative_uncertainty_of_specific_activity_of_137Cs_%: Relative uncertainty of 137Cs determination (percent, 95% CI).
  - Activity_concentration_90Sr_Bqkg: 90Sr activity concentration (Bq/kg).
  - Relative_uncertainty_of_specific_activity_of_90Sr_%: Relative uncertainty of 90Sr determination (percent, 95% CI).
  - Activity_concentration_238Pu_Bqkg: 238Pu activity concentration (Bq/kg).
  - Relative_uncertainty_of_specific_activity_of_238Pu_%: Relative uncertainty of 238Pu determination (percent, 95% CI).
  - Activity_concentration_239_240Pu_Bqkg: Activity concentration of 239+240Pu (Bq/kg).
  - Relative_uncertainty_of_specific_activity_of_239_240Pu_%: Relative uncertainty of 239+240Pu determination (percent, 95% CI).

- Sampling design and depth
  - Cores are primarily 30 cm in length and sectioned into defined layers; one site includes sampling to 110 cm with 10 cm slices.
  - Layer definitions and depth bounds are explicitly captured for traceability and comparability.

- Measurements and units
  - Activity concentrations are reported as bequerel per kilogram (Bq/kg) for each radionuclide.
  - Uncertainty values are provided as percentages (relative uncertainty) at 95% confidence interval.

- Metadata and data quality considerations
  - Some fields include blanks for units or notes, indicating potential gaps in metadata.
  - Emphasis on documenting measurement dates and ensuring consistent units and layer definitions to support data reuse and comparability.

- Governance, sharing, and reuse considerations
  - The dataset is designed to be interoperable with clear identifiers and measurement records, supporting data sharing and provenance.
  - Metadata completeness and standardization (e.g., layer boundaries, core geometry, and date formats) are important for transparency and integrity.

- Practical implications for monitoring frameworks
  - Provides a structured template for recording core sampling data and radionuclide analyses, enabling trend analysis and policy-relevant evaluation.
  - The inclusion of uncertainties supports uncertainty-aware interpretation and decision-making.