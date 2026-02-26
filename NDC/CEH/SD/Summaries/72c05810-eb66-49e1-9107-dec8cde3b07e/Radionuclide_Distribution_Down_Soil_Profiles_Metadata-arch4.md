# Radionuclide_Distribution_Down_Soil_Profiles_metadata

## Overview
- Metadata for a dataset on radionuclide distribution (Cs-137 and Sr-90) in down soil profiles, including site locations, sampling details, and activity concentrations with uncertainties.
- Captures fire impact observations at sites (as of 8 October 2020) and links to a related dataset described as "Description of Trees."
- Includes indicators for measurements below minimum detectable activity and notes on sampling area.

## Data Schema and Key Variables
- Site_Identifier: numerical; same identifier used in the related trees dataset.
- Site_Latitude_WGS84_Decimal_Degrees: decimal degrees; GPS-derived latitude.
- Site_Longitude_WGS84_Decimal_Degrees: decimal degrees; GPS-derived longitude.
- Sampling_Point: numerical; sampling point identifier.
- Fire_Impact_At_Site: categorical; None, Slightly impacted, Heavily Impacted. Based on observations on 8 Oct 2020.
- Sampling_Date: date; format DD/MM/YYYY; date of soil and litter/ash sampling.
- Soil_Layer: depth in centimeters; layer of soil sampled.
- Litter/ash sampling area: 0.078 m^2 (area from which litter/ash was sampled).
- <_Identifier_Cs-137: flag indicating where Cs-137 activity concentration was below minimum detectable activity.
- Cs-137_Activity_Concentrati on_Dry_Mass_Bq_kg-1: Cs-137 activity concentration in dry mass (Bq kg-1).
- Cs-137_Activity_Concentrati on_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty on Cs-137 concentration (percentage).
- <_Identifier_Sr-90: flag indicating where Sr-90 activity concentration was below minimum detectable activity.
- Sr-90_Activity_Concentratio n_Dry_Mass_Bq_kg-1: Sr-90 activity concentration in dry mass (Bq kg-1).
- Sr-90_Activity_Concentratio n_Dry_Mass_Uncertainty_2_Sigma_%: 2-sigma uncertainty on Sr-90 concentration (percentage).
- Sample_Dry_Mass_kg_m-2: coding for sample dry mass; 1 indicates kg m-2, 2 indicates actual sample dry mass; ND indicates not determined.

## Data Quality and Metadata Notes
- Units and measurement methods explicitly stated: coordinates in decimal degrees from GPS (WGS84), date format, and soil layer depth in cm.
- Detection flags present for Cs-137 and Sr-90 to mark below-detection measurements.
- Uncertainties provided as 2-sigma values for both radionuclides.
- Explicit note on litter/ash sampling area, which influences mass-normalized concentrations.
- Some fields use coded indicators (e.g., <_Identifier_*) with ND (not determined) or n/a annotations, which require careful handling during analysis.

## Implications for Data Strategy and Use
- Supports end-to-end data stewardship: geolocated sampling data linked to radionuclide measurements with quality indicators and uncertainties.
- Facilitates cross-referencing with related datasets (e.g., Description of Trees) for holistic environmental assessment.
- Enables prioritization by identifying data gaps (below-detection markers, ND fields) and by understanding sampling effort (area, depth, date).
- Highlights the need for clear metadata standards around coded indicators (e.g., <_Identifier_* fields and Sample_Dry_Mass coding) to enhance discoverability and interoperability.

## Challenges and Considerations for Data Leaders
- Scattered metadata around detection flags and ambiguous coding (e.g., Sigma_%, 1 = ., 2 = concentration of Sr-90) may hinder quick interpretation; requires standardization.
- Access to underlying data (beyond metadata) may be constrained by data provenance and potential paywalls or data sharing limitations across datasets.
- Ensuring consistency in units and definitions across related datasets (e.g., linking Cs-137/Sr-90 measurements with tree data) to support coherent analyses.
- Managing gaps or not-determined values and clearly documenting their implications for downstream analyses and decision-making.