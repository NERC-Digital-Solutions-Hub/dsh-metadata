# Radionuclide_Distribution_Down_Soil_Profiles_metadata

- Purpose: Metadata describing radionuclide distribution in down soil profiles, including sampling details and measured activities for Cs-137 and Sr-90.

- Spatial information:
  - Site_Identifier: Numerical ID used across datasets (also tied to the file "Description of Trees").
  - Site_Latitude_WGS84_Decimal_Degrees: Latitude in decimal degrees, GPS-measured (WGS84).
  - Site_Longitude_WGS84_Decimal_Degrees: Longitude in decimal degrees, GPS-measured (WGS84).

- Sampling and context:
  - Sampling_Point: Numerical sampling point identifier.
  - Fire_Impact_At_Site: Categorical impact on trees at the site (None, Slightly impacted, Heavily Impacted).
  - Sampling_Date: Date of sampling in DD/MM/YYYY.
  - Soil_Layer: Depth of soil layer sampled (cm); note that litter/ash was also sampled from a defined area (0.078 m^2).

- Detection and markers:
  - <_Identifier_Cs-137: Marker indicating Cs-137 measurement below minimum detectable activity (MDA).
  - Cs-137_Activity_Concentration_Dry_Mass_Bq_kg-1: Cs-137 activity concentration on a dry mass basis (Bq kg-1).
  - Cs-137_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Cs-137 concentration.
  - <_Identifier_Sr-90: Marker indicating Sr-90 measurement below MDA.
  - Sr-90_Activity_Concentration_Dry_Mass_Bq_kg-1: Sr-90 activity concentration on a dry mass basis (Bq kg-1).
  - Sr-90_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Sr-90 concentration.

- Sample mass details:
  - Sample_Dry_Mass_kg_m-2: Represents sample dry mass with two coded entries:
    - 1 = kg m^-2
    - 2 = Sample dry mass
  - ND: Not determined (for cases where data are not available).

- Units and conventions:
  - Decimal degrees (DD) for coordinates.
  - Bq kg^-1 for radionuclide activity concentration on a dry-mass basis.
  - cm for soil layer depth.
  - Area for litter/ash sampling specified (0.078 m^2).
  - n/a / ND usage indicates not applicable or not determined.

- Data integration notes:
  - Cs-137 and Sr-90 measurements may include detection flags (< MDA) and associated uncertainties, enabling GIS users to map both detected values and non-detects.
  - Site identifier consistency with the related "Description of Trees" dataset facilitates cross-dataset spatial analyses.