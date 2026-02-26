# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a Biota_radionuclide_data.csv.; Please also see Materials_and_methods_biota.rtf Notes : n/a means not available

## Overview
- Purpose: Metadata and column definitions for the radionuclide data on vertebrates in the Chernobyl Exclusion Zone (2018).
- Source: Gaschak et al.; NERC Environmental Information Data Centre.
- Data file: Biota_radionuclide_data.csv.
- Related methods: Materials_and_methods_biota.rtf.
- Notation: n/a indicates not available.
- Date format: dd/mm/yyyy for Date_sampled.
- Site context: Site_Location_within_Chernobyl_exclusion_zone uses Low/Medium/High values described in Beresford et al. 2008.

## Key columns and meanings
- Chornobyl_Center_ID
  - Laboratory sample Identifier.
- Biota_latin_name
  - Latin scientific name of the species.
- Biota_common_name
  - Common name of the species.
- Date_sampled
  - Date when the biota was sampled (dd/mm/yyyy).
- Site_Location_within_Chernobyl_exclusion_zone
  - Sampling site within the exclusion zone; values: Low, Medium, High (as described in Beresford et al. 2008).
- Sex
  - Sex of the biota; values: female, male, or n/a if not recorded.
- Fresh_mass_of_biota_grams
  - Mass of the fresh biota sample (grams).
- Mass_of_biota_carcass_grams
  - Mass of the biota carcass (grams; notes may indicate what was removed).
- Notes
  - Preparation or handling notes (where applicable).
- Sr-90_< 
  - Indicates if Sr-90 activity is below the limit of detection (LOD) with a "<" symbol; otherwise blank.
- Sr-90_Bq_per_sample
  - Sr-90 activity per sample (Bq per sample).
- error_Sr-90_Bq_per_Sample
  - Uncertainty on Sr-90 activity per sample (Bq per sample); n/a if not reported.
- Cs-137_< 
  - Indicates if Cs-137 activity is below LOD (<).
- Cs-137_Bq_per_sample
  - Cs-137 activity per sample (Bq per sample).
- error_Cs-137_Bq_per_Sample
  - Uncertainty on Cs-137 activity per sample (Bq per sample); n/a if not reported.
- Pu-239_240_Bq_per_sample
  - Pu-239/240 activity per sample (Bq per sample); n/a if not reported.
- error_Pu-239_240_Bq_per_Sample
  - Uncertainty on Pu-239/240 activity per sample (Bq per sample); n/a if not reported.
- Pu-238_< 
  - Indicates if Pu-238 activity is below LOD (<).
- Pu-238_Bq_per_sample
  - Pu-238 activity per sample (Bq per sample).
- error_Pu-238_Bq_per_Sample
  - Uncertainty on Pu-238 activity per sample (Bq per sample); n/a if not reported.
- Sr-90_Bq_per_kg_FW
  - Sr-90 activity concentration per kg fresh weight (Bq/kg FW).
- Cs-137_Bq_per_kg_FW
  - Cs-137 activity concentration per kg fresh weight (Bq/kg FW).
- Pu-239_240_Bq_per_kg_FW
  - Pu-239/240 activity concentration per kg fresh weight (Bq/kg FW); n/a if not reported.
- Pu-238_< 
  - Indicates if Pu-238 concentration is below LOD (<); note pertains to per kg FW context.
- Pu-238_Bq_per_kg_FW
  - Pu-238 concentration per kg fresh weight (Bq/kg FW); n/a if not reported.
- Pu-238_Concentration_ratio
  - Ratio of Biota Pu-238 (Bq/kg FW) to Soil Pu-238 (Bq/kg dry).
- Pu-239_240_Concentration_ratio
  - Ratio of Biota Pu-239/240 (Bq/kg FW) to Soil Pu-239/240 (Bq/kg dry).
- Pu-238_<, available)
  - Indicates Pu-238 concentration below LOD; weight context only.
- Pu-238_Concentration_ratio
  - Pu-238 biota to soil concentration ratio (biota Bq/kg FW divided by soil Bq/kg dry).
- Sr-90_Concentration_ratio
  - Ratio of Sr-90 in biota (Bq/kg FW) to Sr-90 in soil (Bq/kg dry).
- Cs-137_Concentration_ratio
  - Ratio of Cs-137 in biota (Bq/kg FW) to Cs-137 in soil (Bq/kg dry).
- Pu-239_240_Concentration_ratio
  - Ratio of Pu-239/240 in biota (Bq/kg FW) to Pu-239/240 in soil (Bq/kg dry).

## Data formats, units, and interpretation
- Units:
  - Bq_per_sample: becquerels per sample.
  - Bq_per_kg_FW: becquerels per kilogram of fresh weight.
  - Ratios are biota Bq/kg FW divided by soil Bq/kg dry.
- LOD indicators:
  - A leading "<" in a column denotes the value is below the detection limit.
- Missing values:
  - Represented as n/a (not available) where data are not reported.
- Measurement context:
  - Isotopes included: Sr-90, Cs-137, Pu-239/240, Pu-238.
  - Both raw per-sample measurements and concentration-normalized values are provided.
  - Error columns accompany activity measurements where available.
- Site context:
  - Site location references Beresford et al. 2008 for zone descriptions.

## How to use and reuse
- Data products supported:
  - Enables unit-consistent aggregation and comparison across species and sites (biota vs soil concentrations and ratios).
- Best practices:
  - Use the dedicated per-sample and per-kg_FW columns together with their error terms for uncertainty-aware analyses.
  - Handle n/a and "<" indicators explicitly when filtering or summarizing.
  - Join with species metadata (from Biota_latin_name and Biota_common_name) and site metadata (Site_Location_within_Chernobyl_exclusion_zone) for contextual analyses.
- Related documentation:
  - Materials_and_methods_biota.rtf provides sampling, preparation, and analysis methods.

## Access points and references
- Data file: Biota_radionuclide_data.csv
- Metadata documentation: This file (the current document)
- Related methods: Materials_and_methods_biota.rtf
- DOI for the dataset: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a