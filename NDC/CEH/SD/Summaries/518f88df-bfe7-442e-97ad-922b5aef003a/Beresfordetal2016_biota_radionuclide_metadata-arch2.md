# Radionuclide data for vertebrates in the Chornobyl Exclusion Zone, 2018

## Overview
- Metadata describing radionuclide data for vertebrates collected in the Chornobyl Exclusion Zone in 2018.
- Source: Gaschak et al.; NERC Environmental Information Data Centre.
- Includes standardized field definitions, units, and data preparation notes to support environmental monitoring and policy scrutiny over time.

## Data schema and key fields
- Chornobyl_Center_ID: Laboratory sample identifier.
- Biota_latin_name: Latin scientific name of the species.
- Biota_common_name: Common name of the species.
- Date_sampled: Sample collection date (dd/mm/yyyy).
- Site_Location_within_Chernobyl_exclusion_zone: Sampling site tier (Low, Medium, High) as described in Beresford et al. 2008.
- Sex: Sex of the organism (female or male; n/a if not recorded).
- Fresh_mass_of_biota_grams: Fresh mass of the biota sample (grams).
- Mass_of_biota_carcass_grams: Mass of the carcass removed for analysis (grams).
- Notes: Preparation or handling notes for analysis.

## Radionuclide measurements and units
- Sr-90_<, Cs-137_<, Pu-238_<: Detection flag indicators (< indicates below LOD).
- Sr-90_Bq_per_sample, Cs-137_Bq_per_sample, Pu-239_240_Bq_per_sample, Pu-238_Bq_per_sample: Activity per sample (Bq).
- error_Sr-90_Bq_per_Sample, error_Cs-137_Bq_per_Sample, error_Pu-239_240_Bq_per_Sample, error_Pu-238_Bq_per_Sample: Measurement error per sample (Bq).
- Sr-90_Bq_per_kg_FW, Cs-137_Bq_per_kg_FW, Pu-239_240_Bq_per_kg_FW, Pu-238_Bq_per_kg_FW: Activity concentration per kilogram fresh weight (Bq/kg FW); < indicates below LOD where applicable.
- Pu-238_<, Pu-238_Bq_per_kg_FW: Pu-238 detection flag and concentration per kg FW.
- Sr-90_Concentration_ratio, Cs-137_Concentration_ratio, Pu-239_240_Concentration_ratio, Pu-238_Concentration_ratio: Biota-to-soil concentration ratios; units depend on the radionuclide (biota Bq/kg FW divided by soil Bq/kg dry weight, as specified).
- Notes on reporting: Where values are not reported, recorded as n/a.

## Data quality and preparation
- Data are organized with explicit detection flags (<) and n/a indicators to reflect detection limits and missing values.
- Notes include details on how biota were prepared (e.g., removal of parts for analysis).

## Dataset context and accessibility
- Source dataset: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018.
- DOI: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a
- Related materials: Materials_and_methods_biota.rtf provides methodological details.
- Purpose alignment: Supports environmental monitoring and assessment across time with standardized data formats suitable for reporting, maps, and charts.
- Portal and data storage: Datasets are prepared for storage and upload to appropriate data portals as part of standard monitoring workflows.

## Relevance to monitoring objectives
- Provides standardized, quality-assured radionuclide measurements in vertebrates to evaluate environmental health and policy performance over time.
- Enables cross-species, site, and temporal comparisons through consistent units, field names, and reporting conventions.

## Challenges and opportunities
- Challenge: Increasing the value of these datasets by integrating with additional relevant data sources to enable broader analyses.
- Challenge: Ensuring broad access to underlying data to support transparency and reuse.