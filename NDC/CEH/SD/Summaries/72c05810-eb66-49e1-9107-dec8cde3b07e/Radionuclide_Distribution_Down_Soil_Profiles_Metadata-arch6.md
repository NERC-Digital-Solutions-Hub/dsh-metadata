# Radionuclide_Distribution_Down_Soil_Profiles_metadata

## Overview
- Metadata describing a dataset on radionuclide distribution in down-soil profiles, focusing on Cs-137 and Sr-90 activity concentrations (dry mass, Bq/kg).
- Sampling date: 08 October 2020.
- Spatial context: site identifier, latitude, and longitude (WGS84 decimal degrees).
- The site identifier is the same as used in the related dataset described as "Description of Trees."

## Key fields and meanings
- Site_Identifier: numerical site ID (links to related datasets).
- Site_Latitude_WGS84_Decimal_Degrees: site latitude in decimal degrees (GPS, WGS84).
- Site_Longitude_WGS84_Decimal_Degrees: site longitude in decimal degrees (GPS, WGS84).
- Sampling_Point: numerical sampling point identifier.
- Fire_Impact_At_Site: observed fire impact on trees at the site (None, Slightly impacted, Heavily Impacted).
- Sampling_Date: date of soil and litter/ash sampling (DD/MM/YYYY).
- Soil_Layer: depth of soil layer sampled (cm); litter/ash sampled from an area of 0.078 m².
- <_Identifier_Cs-137: marker indicating Cs-137 measurement below minimum detectable activity (MDL); n/a when not applicable.
- Cs-137_Activity_Concentration_Dry_Mass_Bq_kg-1: Cs-137 activity concentration in dry mass (Bq/kg).
- Cs-137_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Cs-137 concentration (percent).
- <_Identifier_Sr-90: marker indicating Sr-90 measurement below MDL; n/a when not applicable.
- Sr-90_Activity_Concentration_Dry_Mass_Bq_kg-1: Sr-90 activity concentration in dry mass (Bq/kg).
- Sr-90_Activity_Concentration_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty for Sr-90 concentration (percent).
- Sample_Dry_Mass_kg_m-2: information about sample dry mass per area; two subcomponents listed as 1 = kg/m² and 2 = actual sample dry mass; ND indicates not determined.

## Data quality and interpretation notes
- Some measurements may be below detection (indicated by the <_Identifier fields).
- Uncertainties are provided as 2-sigma percentages for both Cs-137 and Sr-90.
- Units are consistently in Bq/kg dry mass for radionuclide concentrations; soil depth in cm; area sampling defined as 0.078 m².
- Data may come in multiple formats; ensure consistent interpretation across related datasets (e.g., the referenced "Description of Trees").

## How to use for data exploration and products
- Enable spatial mapping of radionuclide concentrations by site coordinates and sampling points.
- Analyze vertical distribution by soil_layer to study down-profile trends for Cs-137 and Sr-90.
- Compare concentrations with fire impact status to explore potential correlations.
- Use 2-sigma uncertainties to inform error bars in dashboards or reports.
- Integrate with related datasets (e.g., Trees) via Site_Identifier for richer site context.

## Limitations and recommendations
- MDL indicators mean some values are nondetects; handle these appropriately in analyses (e.g., censoring or imputation).
- ND (not determined) entries require careful handling in downstream calculations.
- Verify units and coordinate formats when merging with other datasets to maintain consistency across analyses.