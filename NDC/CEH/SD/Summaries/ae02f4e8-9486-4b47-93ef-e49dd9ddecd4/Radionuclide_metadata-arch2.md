# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates.

## Overview
- Metadata accompanying a dataset describing radionuclide and stable element data, and estimated dose rates for a reference site in the Chernobyl Exclusion Zone.
- Two primary data files: Biota_radionuclide_data.csv and Soil_radionuclide_data.csv.
- Purpose aligned with environmental monitoring: enabling consistent assessment of environmental health and potential policy performance over time.

## Data Files and Structure
- Biota_radionuclide_data.csv
  - Identifiers: Chornobyl_Center_ID (sample identifier), Latitude, Longitude, Date_biota_sampled.
  - Biological information: Biota_latin_name, Biota_Common_name, Age_of_biota, Sex_of_biota, Fresh_mass_of_biota_in_grams, Individuals_in_sample.
  - Radionuclide measurements (fresh mass): Cs-137_Bq_per_kg_FM, Sr-90_Bq_per_kg_FM, Am-241_Bq_per_kg_FM, Pu239_240_Bq_per_kg_FM, Pu-238_Bq_per_kg_FM.
  - Derived metrics: Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR (concentration ratios relative to soil dry mass).
- Soil_radionuclide_data.csv
  - Site and sampling details: N (laboratory sample identifier), GP_Point (sampling area), Latitude_WGS84, Longitude_WGS84, Date_Soil_sampled, Dose_rate_microSv_per_hour_measurement_1…_10.
  - Mass and concentration data: Dry_mass_of_soil_in_grams, Cs-137_Soil_Bq_per_sample_DM, Am-241_Soil_Bq_per_sample_DM, Sr-90_Soil_Bq_per_sample_DM, Pu-239_240_Soil_Bq_per_sample_DM, Pu-238_Soil_Bq_per_sample_DM.
  - Per-sample reporting: error_Cs-137_Bq_per_Sample_DM_P, error_Am-241_Bq_per_Sample_DM_P, error_Sr-90_Bq_per_Sample_DM_P, error_Pu-239_240_Bq_per_Sample_DM_P, error_Pu-238_Bq_per_Sample_DM_P (all expressed with 95% confidence where noted).
  - Dry mass and per-kilogram measurements: Cs-137_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Pu-239_240_Soil_Bq_kg_DM, Pu-238_Soil_Bq_kg_DM.

## Key Variables (Biota)
- Sample identifiers and location: Chornobyl_Center_ID, Latitude, Longitude.
- Biological metadata: Biota_latin_name, Biota_Common_name, Date_biota_sampled, Age_of_biota, Sex_of_biota, Fresh_mass_of_biota_in_grams, Individuals_in_sample.
- Radionuclide concentrations (fresh mass basis): Cs-137_Bq_per_kg_FM, Sr-90_Bq_per_kg_FM, Am-241_Bq_per_kg_FM, Pu239_240_Bq_per_kg_FM, Pu-238_Bq_per_kg_FM.
- Concentration Ratios (CR): Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR (biota fresh mass activity relative to soil dry mass activity).

## Key Variables (Soil)
- Sample and site metadata: N, GP_Point, Latitude_WGS84, Longitude_WGS84, Date_Soil_sampled.
- Dose rates: Dose_rate_microSv_per_hour_measurement_1 through _10 (ambient dose rates at the site).
- Soil mass and concentration metrics: Dry_mass_of_soil_in_grams, Cs-137_Soil_Bq_per_sample_DM, Am-241_Soil_Bq_per_sample_DM, Sr-90_Soil_Bq_per_sample_DM, Pu-239_240_Soil_Bq_per_sample_DM, Pu-238_Soil_Bq_per_sample_DM.
- Uncertainty reporting (per-sample): error_Cs-137_Bq_per_Sample_DM_P, error_Am-241_Bq_per_Sample_DM_P, error_Sr-90_Bq_per_Sample_DM_P, error_Pu-239_240_Bq_per_Sample_DM_P, error_Pu-238_Bq_per_Sample_DM_P.
- Per-kilogram measurements: Cs-137_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Pu-239_240_Soil_Bq_kg_DM, Pu-238_Soil_Bq_kg_DM.

## Data Quality, Standards, and Access
- Columns include explicit explanations, units, and notes to support consistent interpretation.
- Measurements include units in Bq per kg fresh mass (biota) or Bq per sample dry mass / Bq per kg dry mass (soil), and ambient dose rates in microsieverts per hour.
- Some fields include confidence intervals or probability (e.g., error_..._P=0.95) indicating statistical uncertainty.
- Data management guidance emphasizes QA: verification, cleaning, transformation, and storage; outputs can be formatted as reports, maps, and charts, with storage/upload to appropriate data portals.

## Relevance for Analysts Monitoring the Environment
- Provides a standardized, traceable dataset to assess environmental radiological health and potential exposure pathways in the Chernobyl Exclusion Zone.
- Facilitates cross-site and temporal comparisons through consistent column definitions and units.
- Supports risk assessment, environmental monitoring programs, and policy evaluation by delivering quantified radionuclide concentrations and dose-rate estimates in both biota and soil, with accompanying uncertainty metrics.
- Aligns with challenges of increasing dataset value by integrating these data with other environmental layers and ensuring open access to underlying data for broader analysis.