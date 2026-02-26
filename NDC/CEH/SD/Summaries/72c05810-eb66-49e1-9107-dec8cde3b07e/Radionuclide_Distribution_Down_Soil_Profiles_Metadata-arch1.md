# Radionuclide_Distribution_Down_Soil_Profiles_metadata

- Purpose and scope
  - Metadata for a dataset describing radionuclide distribution (Cs-137 and Sr-90) in down-soil profiles, with measurements by soil layer and dry mass basis.
  - Intended to support analysis of vertical distribution, potential correlations with site characteristics, and implications for environmental monitoring.

- Key dataset elements
  - Site information
    - Site_Identifier: numeric site ID (linked to a companion dataset "Description of Trees").
    - Site_Latitude_WGS84_Decimal_Degrees: latitude in decimal degrees (GPS WGS84).
    - Site_Longitude_WGS84_Decimal_Degrees: longitude in decimal degrees (GPS WGS84).
  - Sampling details
    - Sampling_Point: numeric sampling point identifier.
    - Sampling_Date: date of soil and litter/ash sampling (format DD/MM/YYYY); event observed on 8 Oct 2020.
    - Fire_Impact_At_Site: qualitative assessment of fire impact on trees at the site (None, Slightly impacted, Heavily Impacted) on 8 Oct 2020.
    - Soil_Layer: depth of soil layer sampled (in cm). Litter/ash also sampled from an area of 0.078 m^2.
  - Radionuclide measurements (dry mass basis)
    - <_Identifier_Cs-137: marker indicating Cs-137 activity concentration was below minimum detectable activity (MDL) – not applicable where not triggered.
    - Cs-137_Activity_Concentration_Dry_Mass_Bq_kg-1: activity concentration of Cs-137 in dry mass (Bq kg-1).
    - Cs-137_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Cs-137 concentration (percentage; units indicated as Bq kg-1 in the field name).
    - <_Identifier_Sr-90: marker indicating Sr-90 activity concentration below MDL.
    - Sr-90_Activity_Concentration_Dry_Mass_Bq_kg-1: activity concentration of Sr-90 in dry mass (Bq kg-1).
    - Sr-90_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_: 2-sigma uncertainty for Sr-90 concentration (Bq kg-1).
  - Sample mass and data completeness
    - Sample_Dry_Mass_kg_m-2: dry mass per unit area for the sample (kg m^-2); noted as “1 = kg m^-2” and “2 = Sample dry mass,” with some entries marked ND (not determined).

- Data quality notes and caveats
  - Some fields are marked as not applicable or not determined (ND), reflecting incomplete measurements or missing values.
  - MDL indicators (<_Identifier Cs-137 / <_Identifier Sr-90) flag instances where radionuclide levels were below detection limits.
  - Units and metadata are designed to support cross-dataset comparisons (e.g., association with the “Description of Trees” dataset) and future data linking.

- Potential analytical uses for analysts
  - Assess vertical distribution of Cs-137 and Sr-90 by soil depth and relate to soil layer characteristics.
  - Explore spatial patterns by site coordinates and correlate with fire impact severity.
  - Compute total activity per area using Cs-137/Sr-90 concentrations and corresponding sample_dry_mass values.
  - Integrate with other datasets (e.g., tree-related data) to study transfer and distribution pathways following a radiological event.
  - Handle detection limits and data gaps by using MDL markers and ND indicators in statistical models.