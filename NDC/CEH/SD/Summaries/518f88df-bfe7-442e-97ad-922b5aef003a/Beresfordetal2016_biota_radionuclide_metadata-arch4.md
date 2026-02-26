# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Describes the column headings and units for the Biota_radionuclide_data.csv dataset and references accompanying Materials_and_methods_biota.rtf.
- Data represent radionuclide activity measurements in vertebrates from the Chernobyl Exclusion Zone in 2018.
- Dataset is part of the NERC Environmental Information Data Centre; DOI provided for access and citation.

## Data structure and key fields
- Identifiers and taxonomy
  - Chornobyl_Center_ID: Laboratory sample identifier.
  - Biota_latin_name: Latin species name.
  - Biota_common_name: Common species name.
- Sampling and site metadata
  - Date_sampled: Sampling date (dd/mm/yyyy).
  - Site_Location_within_Chernobyl_exclusion_zone: Sampling site location; categorized as Low, Medium, or High per Beresford et al. 2008.
  - Sex: Sex of the biota (female/male) or n/a if not recorded.
- Sample characteristics
  - Fresh_mass_of_biota_grams: Fresh mass of the biota sample (grams).
  - Mass_of_biota_carcass_grams: Mass of the carcass (grams) and notes on removals.
  - Notes: Notes on preparation or handling (where applicable).
- Radionuclide measurements (per sample)
  - Sr-90_< and Cs-137_<: Indicators that measurement is below the limit of detection (LOD) when present.
  - Sr-90_Bq_per_sample, Cs-137_Bq_per_sample: Activity per sample (BECQUEREL).
  - error_Sr-90_Bq_per_Sample, error_Cs-137_Bq_per_Sample: Measurement error per sample (Bq).
  - Pu-239_240_Bq_per_sample, Pu-238_Bq_per_sample: Activity for Pu-239/240 and Pu-238 per sample (Bq).
  - error_Pu-239_240_Bq_per_Sample, error_Pu-238_Bq_per_Sample: Associated errors (Bq).
  - Pu-238_<: Below-LOD indicator for Pu-238 per sample (not applicable to per-sample value).
- Concentration data (per kg fresh weight)
  - Sr-90_Bq_per_kg_FW, Cs-137_Bq_per_kg_FW, Pu-239_240_Bq_per_kg_FW, Pu-238_Bq_per_kg_FW: Activity concentration per kilogram fresh weight (Bq/kg FW); < indicates below LOD where applicable.
- Concentration ratios (biota vs soil)
  - Sr-90_Concentration_ratio, Cs-137_Concentration_ratio, Pu-239_240_Concentration_ratio, Pu-238_Concentration_ratio: Ratios of biota to soil activities (biota Bq/kg FW divided by soil Bq/kg dry weight); some entries may be n/a when not reported or not applicable.
  - Pu-238_<_Concentration_ratio: Below-LOD indicator for Pu-238 concentration ratio (if available).
- Data quality and handling notes
  - n/a indicates not available/unreported.
  - The dataset includes LOD indicators and per-sample errors where measured.

## Data quality, standards, and provenance
- Includes explicit LOD indicators (<) for several radionuclides to denote non-detect results.
- Uses consistent units: Bq per sample, Bq per kg fresh weight, and biota/soil concentration ratios with appropriate denominator units.
- Metadata references method documentation (Materials_and_methods_biota.rtf) for analytical procedures.
- Site descriptors reference Beresford et al. 2008 for site classification within the exclusion zone.

## Access, usage, and related resources
- Primary dataset: Biota_radionuclide_data.csv within the NERC Environmental Information Data Centre.
- Methods and context: Materials_and_methods_biota.rtf (linked within metadata).
- Site framework reference: Beresford et al. 2008 J Environ Radioact. 99, 1496-1502 for site location context.
- DOI: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a
- Notes on data interpretation
  - “n/a” used when data are not available.
  - “<” indicates left-censored data below detection limits.
  - Some concentration ratio fields may be unavailable or not reported.