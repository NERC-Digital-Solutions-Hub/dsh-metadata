# Code_of_the_sample, Explanation = Database serial number - unique ID.

## Overview
- Data dictionary for a soil core sampling dataset with radiological analyses.
- Core details: 37 mm diameter, sectioned into layers with defined top and bottom borders; multiple isotopes measured per layer.
- One site example mentioned: core sampled to 110 cm, sectioned into 10 cm slices.
- Data products likely to support self-serve analysis of layer-specific activity concentrations.

## Fields and schema (key items)

- Code_of_the_sample
  - Explanation: Database serial number - unique ID
  - Units: None
  - Notes: None
- Identifier_of_the_sample
  - Explanation: UIAR unique label - chemical analysis number
  - Units: None
  - Notes: None
- Dates_of_the_activity_measurements
  - Explanation: Date of measurement (long date format)
  - Units: dd-mmm-yy
  - Notes: None
- Sampling_area_m2
  - Explanation: Size of the area sampled
  - Units: square metres
  - Notes: None

- The_top_border_of_a_layer_cm
  - Explanation: 30cm cores were sectioned into layers (0-2, 2-4, 4-6, 6-8, 8-10, 10-15, 15-20, 20-25 and 25-30 cm). One site was sampled to 110 cm and the core was sectioned into 10 cm slices.
  - Units: cm
  - Notes: 30cm cores described; layering scheme detailed

- The_bottom_border_of_a_layer_cm
  - Explanation: 30cm cores were sectioned into layers (0-2, 2-4, 4-6, 6-8, 8-10, 10-15, 15-20, 20-25 and 25-30 cm). One site was sampled to 110 cm and the core was sectioned into 10 cm slices.
  - Units: cm
  - Notes: 30cm cores described; layering scheme detailed

- Mass_of_the_layer_kg
  - Explanation: Sample mass of each layer of 37mm diameter core
  - Units: kilogram
  - Notes: None

- Activity_concentration_137Cs_Bqkg
  - Explanation: Activity concentration in soil dry matter 137Cs
  - Units: bequerel per kilogram
  - Notes: None

- Relative_uncertainty_of _specific_activity_of_137Cs_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percentage
  - Notes: None

- Activity_concentration_90Sr_Bqkg
  - Explanation: Activity concentration in soil dry matter 90Sr
  - Units: bequerel per kilogram
  - Notes: None

- Relative_uncertainty_of _specific_activity_of_90Sr_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percentage
  - Notes: None

- Activity_concentration_238Pu_Bqkg
  - Explanation: Activity concentration in soil dry matter 238Pu
  - Units: bequerel per kilogram
  - Notes: None

- Relative_uncertainty_of _specific_activity_of_238Pu_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percentage
  - Notes: None

- Activity_concentration_239_240Pu_Bqkg
  - Explanation: Activity concentration in soil dry matter 239Pu and 240Pu
  - Units: bequerel per kilogram
  - Notes: None

- Relative_uncertainty_of _specific_activity_of_239_240Pu_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval)
  - Units: percentage
  - Notes: None

## How the data supports the Data Support aims

- Enables end users to explore layer-by-layer radiological activity (137Cs, 90Sr, 238Pu, 239/240Pu) with associated uncertainties.
- Facilitates data cleaning, integration with site-level metadata (e.g., sampling_area_m2, dates), and creation of dashboards or pivot-table style reports for self-serve analysis.
- Clear unit definitions (Bq/kg for activities, kg for layer mass, cm for layer borders, and percentage for uncertainty) support consistent transformation and comparison across datasets.
- The layered structure (top/bottom borders, layer mass, and isotope activities) supports aggregations by depth range and site, enabling broader analyses and stakeholder communication.