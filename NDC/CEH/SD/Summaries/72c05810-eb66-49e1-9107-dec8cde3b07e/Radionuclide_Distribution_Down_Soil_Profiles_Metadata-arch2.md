# Radionuclide_Distribution_Down_Soil_Profiles_metadata

## Overview
- Metadata for a dataset on radionuclide distribution in soil profiles, focusing on Cs-137 and Sr-90 activity concentrations (dry mass).
- Includes site identifiers, GPS coordinates, sampling details, date, fire impact observation, and sample area for litter/ash.
- Data are provided with activity concentrations in Bq/kg (dry mass) and 2-sigma uncertainties; some samples marked as below minimum detectable activity (MDL).
- Fire impact on trees at the sites observed on 8 October 2020.

## Data fields and meanings
- Site_Identifier: numerical; matches the site identifier used in related datasets (e.g., Description of Trees).
- Site_Latitude_WGS84_Decimal_Degrees: decimal degrees; GPS-based latitude (WGS84).
- Site_Longitude_WGS84_Decimal_Degrees: decimal degrees; GPS-based longitude (WGS84).
- Sampling_Point: numerical identifier for the sampling location within the site.
- Fire_Impact_At_Site: categorical descriptor of fire impact; values: None, Slightly impacted, Heavily Impacted.
- Sampling_Date: date of sampling in DD/MM/YYYY.
- Soil_Layer: depth of soil layer sampled (in cm).
- Litter/ash sampling area: area for litter/ash sampling given as 0.078 m^2.
- <_Identifier_Cs-137: marker indicating Cs-137 measurement below MDL (not applicable when not below MDL).
- Cs-137_Activity_Concentration_Dry_Mass_Bq_kg-1: Cs-137 activity concentration in dry mass (Bq/kg).
- Cs-137_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Cs-137 concentration (percent).
- <_Identifier_Sr-90: marker indicating Sr-90 measurement below MDL (not applicable when not below MDL).
- Sr-90_Activity_Concentration_Dry_Mass_Bq_kg-1: Sr-90 activity concentration in dry mass (Bq/kg).
- Sr-90_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Sr-90 concentration (percent).
- Sample_Dry_Mass_kg_m-2: per-area dry mass of the sample (kg/m^2); note: "ND" indicates not determined.
- ND: Not Determined (used where data are unavailable).

## Data quality and processing
- Data are intended to be verified, quality assured, cleaned, and transformed.
- Outputs are presented in standardized formats (e.g., reports, maps, charts) and stored/uploaded to appropriate data portals.
- The dataset supports cross-site comparisons and longitudinal monitoring of environmental radiological conditions.

## Practical notes for analysts
- Treat n/a and ND entries as missing data where appropriate.
- Use the <_Identifier_Cs-137 and <_Identifier_Sr-90 flags to handle non-detects correctly.
- Maintain consistent units (Bq/kg for Cs-137 and Sr-90; kg/m^2 for Sample_Dry_Mass; measurements are dry-mass based).
- Integrate with other environmental datasets to enhance dataset value and accessibility.