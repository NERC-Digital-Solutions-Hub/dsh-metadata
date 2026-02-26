# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates.

## Overview
- Metadata describing two CSV datasets from a reference site in the Chernobyl Exclusion Zone.
- Purpose: provide radionuclide and stable element data for biota and soil, plus estimated ambient dose rates to enable analysis of transfer and exposure.
- Datasets:
  - Biota_radionuclide_data.csv
  - Soil_radionuclide_data.csv
- Source: Beresford et al., published with the NERC Environmental Information Data Centre (DOI provided).

## Biota_radionuclide_data.csv – key content and structure
- Sample identifiers and taxa
  - Chornobyl_Center_ID: unique sample identifier (centre-specific).
  - Biota_latin_name: Latin species name.
  - Biota_Common_name: common name.
- Temporal and spatial context
  - Date_biota_sampled: date of sampling (dd/mm/yyyy).
  - Latitude and Longitude: decimal coordinates (WGS84).
- Biological metadata
  - Age_of_biota: SAD (sub-adult), Juv (juvenile), or adult.
  - Sex_of_biota: recorded sex when available.
  - Fresh_mass_of_biota_in_grams: fresh mass of the sample.
  - Individuals_in_sample: number of individuals in the sample (where applicable).
  - Trap: site trapping line (where applicable).
- Radionuclide activity concentrations (per fresh mass)
  - Cs-137_Bq_per_kg_FM
  - Sr-90_Bq_per_kg_FM
  - Am-241_Bq_per_kg_FM
  - Pu239_240_Bq_per_kg_FM
  - Pu-238_Bq_per_kg_FM
  - Units: Bq per kilogram (fresh mass).
- Concentration ratios (CR)
  - Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR
  - Pu-239_240_CR (unitless)
  - Each CR defined as the fresh-mass biota activity concentration divided by the soil dry-mass activity concentration.
- Notes
  - Some fields include explanatory notes or are listed as not available (n/a) in places.

## Soil_radionuclide_data.csv – key content and structure
- Sample and site identifiers
  - N: laboratory unique sample identifier.
  - GP_Point: inner sampling area or Pine Tree identifier (bulked samples where applicable).
- Spatial and temporal context
  - Latitude_WGS84, Longitude_WGS84: coordinates (WGS84).
  - Date_Soil_sampled: sampling date (dd/mm/yyyy).
- Ambient dose rates (site measurements)
  - Dose_rate_microSv_per_hour_measurement_1 through Dose_rate_microSv_per_hour_measurement_10
  - Measurements represent ambient dose rate in microsieverts per hour; multiple readings per site.
- Soil mass and concentration data
  - Dry_mass_of_soil_in_grams: dry mass analysed (grams).
  - Cs-137_Soil_Bq_per_sample_DM: Cs-137 activity per soil sample (Bq per dry mass).
  - Am-241_Soil_Bq_per_sample_DM: Am-241 activity per soil sample (Bq per dry mass).
  - Sr-90_Soil_Bq_per_sample_DM: Sr-90 activity per soil sample (Bq per dry mass).
  - Pu-239_240_Soil_Bq_per_sample_DM: Pu-239,240 activity per soil sample (Bq per dry mass).
  - Pu-238_Soil_Bq_per_sample_DM: Pu-238 activity per soil sample (Bq per dry mass).
  - Error fields (e.g., error_Cs-137_Bq_per_Sample_DM_P) indicate measurement uncertainty with a specified confidence level (e.g., P=0.95 for 95% CI).
- Concentration data per dry mass and per kilogram
  - Cs-137_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Pu-239_240_Soil_Bq_kg_DM, Pu-238_Soil_Bq_kg_DM
  - Bq per kilogram of dry soil mass.
- Notes on metadata fields
  - Many fields include explicit unit descriptions (Bq, grams, microsieverts/hour, etc.) and some fields are marked as not applicable or not available.
  - 95% confidence interval fields accompany per-sample measurements to denote uncertainty.

## Data quality and interpretation considerations
- The datasets include comprehensive metadata on column headings, units, sampling context, and measurement uncertainty.
- Data cover biota–soil comparisons via radionuclide concentrations and biota/soil concentration ratios (CRs), aiding transfer-factor analyses.
- Handling of missing or not-available values is required; some fields contain n/a entries.
- Dose-rate measurements are provided as multiple site readings, enabling assessment of spatial variability in ambient exposure.
- Uncertainty information (e.g., 95% CI) accompanies several soil measurements, important for risk assessment and model calibration.

## Potential analyses and uses for analysts
- Calculate relationships between soil activity and biota uptake using CRs and concentration data.
- Model radionuclide transfer pathways from soil to biota and predict dose rates at different sites or times.
- Map spatial patterns of radionuclide contamination using coordinate data and dose-rate readings.
- Compare Cs-137, Sr-90, Am-241, Pu-239/240, and Pu-238 profiles across biota species and soil samples.
- Assess temporal trends by comparing sampling dates and radionuclide concentrations (where longitudinal data exist).
- Integrate dataset metadata with external environmental or administrative boundary data for localized risk assessments.

## Access and provenance
- Data are deposited at the NERC Environmental Information Data Centre.
- DOI provided for reference and data access.
- Metadata defines column headings and units to enable reproducible analysis and data reuse.