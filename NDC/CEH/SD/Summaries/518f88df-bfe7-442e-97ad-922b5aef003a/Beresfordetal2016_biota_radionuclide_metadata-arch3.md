# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Purpose and scope
- Provides metadata and unit definitions for radionuclide data collected from vertebrate biota in the Chernobyl Exclusion Zone in 2018.
- Data are hosted by the NERC Environmental Information Data Centre and accompany the biota radionuclide dataset described by Gaschak et al. and colleagues.
- Enables interpretation, verification, and reuse of measurements of radionuclide activities in biota, including per-sample values, per-kg fresh weight concentrations, and soil-biomass concentration ratios.

## Data fields and structure (key columns and their meaning)
- Chornobyl_Center_ID: Laboratory sample identifier.
- Biota_latin_name: Latin species name; Biota_common_name: common species name.
- Date_sampled: Sampling date (dd/mm/yyyy).
- Site_Location_within_Chernobyl_exclusion_zone: Sampling site category within the zone (Low, Medium, High) as described in Beresford et al. 2008.
- Sex: Sex of the organism (female/male) or n/a if not recorded.
- Fresh_mass_of_biota_grams: Mass of the fresh biota sample (grams).
- Mass_of_biota_carcass_grams: Mass of the carcass portion used (grams); notes explain what was removed.
- Notes: Additional notes on preparation or handling.
- Radionuclide measurements (examples and units):
  - Sr-90_< and Cs-137_<: Below the limit of detection (LOD) indicator if present.
  - Sr-90_Bq_per_sample, Cs-137_Bq_per_sample, Pu-239_240_Bq_per_sample, Pu-238_Bq_per_sample: Activity per sample (Bq per sample).
  - error_Sr-90_Bq_per_Sample, error_Cs-137_Bq_per_Sample, error_Pu-239_240_Bq_per_Sample, error_Pu-238_Bq_per_Sample: Measurement error (Bq per sample); n/a if not reported.
  - Pu-238_<: LOD indicator for Pu-238 per sample.
- Concentration measures per unit mass:
  - Sr-90_Bq_per_kg_FW, Cs-137_Bq_per_kg_FW, Pu-239_240_Bq_per_kg_FW, Pu-238_Bq_per_kg_FW: Activity concentration per kilogram fresh weight (Bq/kg FW); Pu-238_< indicates below LOD.
- Concentration ratios:
  - Sr-90_Concentration_ratio, Cs-137_Concentration_ratio, Pu-239_240_Concentration_ratio, Pu-238_Concentration_ratio: Ratio of biota activity (Bq/kg FW) to soil activity (Bq/kg dry weight) for the respective radionuclide.
- Availability indicator notes:
  - Each < symbol denotes measurements below the detection limit where applicable.
  - n/a entries indicate missing or not applicable data.

## Data quality and metadata considerations
- LOD indicators (<) present for certain radionuclides and samples; explicit error terms provided where available.
- Some fields may be n/a when data are not recorded or not applicable (e.g., sex, errors).
- Metadata notes clarify preparation and analytical details; completeness of unit definitions is explicit to facilitate data integration.
- Data are intended to be publicly shared and traceable to source publications and dataset records.

## Governance and usage implications for monitoring frameworks
- Facilitates cross-study comparisons of radionuclide uptake across species, sites, and years by providing standardized units and clear metadata.
- Supports calculation of uptake patterns and environmental transfer via concentration ratios to soil.
- Highlights the need for consistent metadata (units, LOD reporting, date formats, site categorization) to ensure data can be reused in policy evaluation and future decision-making.
- Availability through a recognized data centre (NERC-Environmental Information Data Centre) aligns with data governance and openness, though some data-sharing barriers may arise if broader access controls apply.

## Source reference
- Metadata associated with: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P.; Beresford, N.A.; Barnett, C.L.; Wells, C.; Maksimenko, A.; Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a