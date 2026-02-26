# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Summary of purpose and scope
- Provides column headings and measurement units for radionuclide data collected from vertebrates in the Chernobyl Exclusion Zone (2018).
- Associated dataset: Biota_radionuclide_data.csv.
- Related documentation: Materials_and_methods_biota.rtf.
- Data are stored and citable via the NERC Environmental Information Data Centre (DOI provided).

## Dataset structure and key fields
- Chornobyl_Center_ID: Laboratory sample identifier.
- Biota_latin_name: Latin scientific name of species.
- Biota_common_name: Common name of species.
- Date_sampled: Sampling date (format: dd/mm/yyyy).
- Site_Location_within_Chernobyl_exclusion_zone: Sampling site category within CZ; values include Low, Medium, High (as described in Beresford et al. 2008).
- Sex: Sex of the biota (female or male); n/a if not recorded.
- Fresh_mass_of_biota_grams: Fresh mass of the biota in grams.
- Mass_of_biota_carcass_grams: Mass of the carcass, indicating portions removed prior to analysis.
- Notes: Preparation or processing notes for analysis (where applicable).

## Radionuclide measurements (per sample and per fresh weight)
- Sr-90_< and Cs-137_<, Pu-238_<: Indicators that the activity/concentration was below the limit of detection (LOD); the "<" symbol denotes non-detects.
- Sr-90_Bq_per_sample, Cs-137_Bq_per_sample, Pu-239_240_Bq_per_sample, Pu-238_Bq_per_sample: radionuclide activity per sample (Bq per sample).
- error_Sr-90_Bq_per_Sample, error_Cs-137_Bq_per_Sample, error_Pu-239_240_Bq_per_Sample, error_Pu-238_Bq_per_Sample: measurement error on the per-sample activity (Bq per sample); n/a where not reported.
- Sr-90_Bq_per_kg_FW, Cs-137_Bq_per_kg_FW, Pu-239_240_Bq_per_kg_FW, Pu-238_Bq_per_kg_FW: radionuclide activity concentration per kilogram of fresh weight (Bq per kg FW); n/a where not reported.
- Pu-238_<: below-LOD indicator for Pu-238 concentration per sample.
- Pu-238_Bq_per_kg_FW, Sr-90_Bq_per_kg_FW, etc.: per-kg fresh weight concentration values (Bq/kg FW) where available.

## Concentration ratios (biota to soil)
- Sr-90_Concentration_ratio, Cs-137_Concentration_ratio, Pu-239_240_Concentration_ratio, Pu-238_Concentration_ratio: ratios of biota activity concentration (Bq/kg FW) to soil activity concentration (Bq/kg dry weight).
- Availability notes: some entries may be n/a if data are missing.
- Pu-238_Concentration_ratio, Pu-238_Concentration_ratio (weight): ratios for Pu-238 where applicable; some fields marked n/a when not available.

## Data quality, handling, and conventions
- n/a indicates not available or not reported.
- "<" denotes detection-limit limitations for the corresponding measurement.
- Date and site classifications follow defined formats and schemes (e.g., site categories based on Beresford et al. 2008).
- Units used:
  - Bq per sample for activity per sample.
  - Bq per kg fresh weight for concentration per unit biota mass.
  - Ratios are unitless (biota concentration divided by soil concentration).

## Provenance and usage notes
- Data prepared for environmental radiological assessment of radionuclide transfer to vertebrates in the Chernobyl Exclusion Zone.
- Useful for identifying species- and site-specific patterns, comparing with soil concentrations, and supporting transfer-factor analyses.
- Metadata file aims to enable data discovery, interpretation, and reproducibility; researchers may consult Materials_and_methods_biota.rtf for methodological details.

## Reference and access
- Source dataset: Biota_radionuclide_data.csv.
- Data centre: NERC Environmental Information Data Centre.
- DOI: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a.