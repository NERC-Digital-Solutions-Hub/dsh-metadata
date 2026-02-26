# Metadata (an explanation of column headings and units) for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERC-Environmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7-442e-97ad-922b5aef003a

## Overview
- Describes column headings, meanings, and measurement units for the Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018 dataset.
- Dataset file: Biota_radionuclide_data.csv; related materials: Materials_and_methods_biota.rtf.
- Indicates how nondetects and missing data are recorded, and how data were prepared and annotated.
- Source and context: archived in NERC-Environmental Information Data Centre; site classifications reference Beresford et al. 2008.

## Data schema and key fields
- Chornobyl_Center_ID: Laboratory sample identifier.
- Biota_latin_name: Latin scientific name of the species.
- Biota_common_name: Common name of the species.
- Date_sampled: Sampling date (dd/mm/yyyy).
- Site_Location_within_Chernobyl_exclusion_zone: Sampling site category (Low, Medium, High) per Beresford et al. 2008.
- Sex: Sex of the biota (female or male); n/a if not recorded.
- Fresh_mass_of_biota_grams: Mass of fresh biota sample (grams).
- Mass_of_biota_carcass_grams: Mass of carcass removed (grams); notes indicate details on removals.
- Notes: Preparation and handling notes for analysis.
- Radionuclide measurements:
  - Sr-90_< and Sr-90_Bq_per_sample and error_Sr-90_Bq_per_Sample
  - Sr-90_Bq_per_kg_FW and Sr-90_Concentration_ratio
  - Cs-137_< and Cs-137_Bq_per_sample and error_Cs-137_Bq_per_Sample
  - Cs-137_Bq_per_kg_FW and Cs-137_Concentration_ratio
  - Pu-239_240_Bq_per_sample and error_Pu-239_240_Bq_per_Sample
  - Pu-239_240_Bq_per_kg_FW and Pu-239_240_Concentration_ratio
  - Pu-238_< and Pu-238_Bq_per_sample and error_Pu-238_Bq_per_Sample
  - Pu-238_Bq_per_kg_FW and Pu-238_Concentration_ratio
- Units:
  - Bq_per_sample: becquerels per individual sample.
  - Bq_per_kg_FW: becquerels per kilogram fresh weight.
  - Concentration_ratio: biota Bq per kg FW divided by soil Bq per kg dry weight.
- Detection and missing data:
  - "<" indicates activity/concentration below the limit of detection (LOD) where applicable.
  - n/a indicates not available for missing values or not applicable.

## Measurement conventions and data quality
- Non-detects denoted with "<" in corresponding columns.
- Error columns provided for some measurements; if error not reported, marked as n/a.
- Notes explain biota preparation and any data caveats; some fields explicitly state when values are not reported.
- Data are tied to specific sampling sites within the Chernobyl Exclusion Zone and to site classifications from Beresford et al. 2008.

## Data provenance and metadata quality
- Metadata clarifies the meaning of each column, expected units, and how derived fields (e.g., concentration ratios) are computed.
- References to related methods document (Materials_and_methods_biota.rtf) and baseline site descriptions (Beresford et al. 2008) support reproducibility and data reuse.
- Clearly states where data are complete, partial, or missing, aiding data governance and governance risk assessment.

## Data governance and sharing considerations
- Dataset is intended for sharing via the NERC Environmental Information Data Centre with standardized column definitions and units.
- Highlights the need for consistent handling of non-detects, missing values, and preparation notes to ensure usability by data creators and data users.
- For reuse, users should consult the related Materials_and_methods_biota.rtf and Beresford 2008 site classifications to interpret site context and methodologies.

## Related materials and references
- Materials_and_methods_biota.rtf (preparation and methods for biota radionuclide analysis).
- Beresford et al. 2008 (J Environ Radioact., site classifications within the Chernobyl Exclusion Zone).