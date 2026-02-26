# Dataset schema for soil core sampling and radionuclide activity concentrations

## Overview
- Defines a data dictionary for a soil core sampling dataset focusing on radionuclide activity concentrations.
- Includes identifiers, sampling metadata, layer segmentation, sample mass, and measured activities with uncertainties.

## Data schema (key fields)
- Code_of_the_sample: Database serial number – unique ID.
- Identifier_of_the_sample: UIAR unique label – chemical analysis number.
- Dates_of_the_activity_measurements: Date of measurement (long date format). Units: dd-mmm-yy.
- Sampling_area_m2: Size of the area sampled. Units: square metres.
- The_top_border_of_a_layer_cm: Top border of a layer (layers defined as 0-2, 2-4, 4-6, 6-8, 8-10, 10-15, 15-20, 20-25, 25-30 cm; one site to 110 cm with 10 cm slices). Units: descriptive text.
- The_bottom_border_of_a_layer_cm: Bottom border of a layer (same layering scheme). Units: descriptive text.
- Mass_of_the_layer_kg: Sample mass of each layer of a 37 mm diameter core. Units: kilogram.
- Activity_concentration_137Cs_Bqkg: Activity concentration in soil dry matter for 137Cs. Units: becquerel per kilogram.
- Relative_uncertainty_of_specific_activity_of_137Cs_%: Relative uncertainty of determination (95% confidence interval). Units: percentage.
- Activity_concentration_90Sr_Bqkg: Activity concentration in soil dry matter for 90Sr. Units: becquerel per kilogram.
- Relative_uncertainty_of_specific_activity_of_90Sr_%: Relative uncertainty of determination (95% CI). Units: percentage.
- Activity_concentration_238Pu_Bqkg: Activity concentration in soil dry matter for 238Pu. Units: becquerel per kilogram.
- Relative_uncertainty_of_specific_activity_of_238Pu_%: Relative uncertainty of determination (95% CI). Units: percentage.
- Activity_concentration_239_240Pu_Bqkg: Activity concentration in soil dry matter for 239/240Pu. Units: becquerel per kilogram.
- Relative_uncertainty_of_specific_activity_of_239_240Pu_%: Relative uncertainty of determination (95% CI). Units: percentage.

## Sampling details
- Core diameter: 37 mm.
- Layering scheme: 0-2 cm, 2-4 cm, 4-6 cm, 6-8 cm, 8-10 cm, 10-15 cm, 15-20 cm, 20-25 cm, 25-30 cm; one site extended to 110 cm with 10 cm slices.

## Measurements and data quality
- Date format: dd-mmm-yy.
- Each radionuclide concentration is given in Bq/kg (soil dry matter) with corresponding percentage uncertainty (95% CI).

## Data management and accessibility
- Data are to be verified, quality assured, cleaned, and transformed.
- Outputs are presented as reports, maps, and charts.
- Datasets should be stored and uploaded to appropriate portals for accessibility and reuse.

## Relevance to environmental monitoring goals
- Promotes standardized, transparent reporting of radionuclide concentrations in soil.
- Supports assessment of environmental health and policy performance over time through consistent formats and units.

## Challenges for Analysts Monitoring the Environment
- Increasing the value of datasets by combining them with other relevant data (avoiding single-use data).
- Enabling access to the underlying data used to create final outputs.