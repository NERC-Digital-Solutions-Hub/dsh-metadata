# Radionuclide_Distribution_Down_Soil_Profiles_metadata

- Overview
  - Metadata file describing radionuclide distribution in down soil profiles, including site information, sampling details, and measured Cs-137 and Sr-90 activity concentrations with uncertainties.

- Key identifiers and cross-references
  - Site_Identifier: numerical identifier; cross-referenced with related dataset described as "Description of Trees".
  - Sampling_Point: numerical identifier for the sampling location within a site.

- Geolocation and site observations
  - Site_Latitude_WGS84_Decimal_Degrees: latitude in decimal degrees (GPS, WGS84).
  - Site_Longitude_WGS84_Decimal_Degrees: longitude in decimal degrees (GPS, WGS84).
  - Fire_Impact_At_Site: observed fire impact on trees at the site as of 8 October 2020; categories include None, Slightly impacted, Heavily Impacted.

- Sampling details
  - Sampling_Date: date of soil and litter/ash sampling (DD/MM/YYYY).
  - Soil_Layer: depth of soil sampled (in cm).
  - Litter/ash sampling area: 0.078 m^2.
  - <_Identifier_Cs-137: marker indicating where Cs-137 activity concentration was below minimum detectable activity.
  - <_Identifier_Sr-90: marker indicating where Sr-90 activity concentration was below minimum detectable activity.
  - Sample_Dry_Mass_kg_m-2: dry mass per unit area (kg/m^2); notes indicate possible non-determinacy (ND) for some entries.

- Radionuclide measurements
  - Cs-137_Activity_Concentration_Dry_Mass_Bq_kg-1: activity concentration of Cs-137 in dry mass (Bq/kg).
  - Cs-137_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty on Cs-137 concentration (percent).
  - Sr-90_Activity_Concentration_Dry_Mass_Bq_kg-1: activity concentration of Sr-90 in dry mass (Bq/kg).
  - Sr-90_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty on Sr-90 concentration (percent).

- Data quality and formatting notes
  - Some fields are marked as Not applicable (Not applicable) or ND (not determined), and below-detection markers indicate when concentrations are below MDAs.
  - Units used include Bq kg-1 for activity concentration, cm for soil depth, and kg/m^2 for dry mass per area.
  - Coordinates are provided with GPS measurements (WGS84) to enable precise site localization.

- Relevance for monitoring frameworks
  - Provides a standardized schema for recording radionuclide distributions by soil layer, enabling comparisons across sites and over time.
  - Supports data governance through explicit metadata on data provenance, measurement methods (GPS, depth, area sampled), and uncertainty.
  - Facilitates risk assessment and policy evaluation by linking site observations (e.g., fire impact) with quantitative radionuclide measurements and their uncertainties.