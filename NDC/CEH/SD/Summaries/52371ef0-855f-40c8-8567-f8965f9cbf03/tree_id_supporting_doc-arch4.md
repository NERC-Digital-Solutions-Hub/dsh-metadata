# Local tree names, uses and species identification in Mozambique: supporting documentation

## Overview
- Dataset of local tree names, species identifications, and local uses from 17 villages across three Mozambican districts (Mabalane, Marrupa, Gurue).
- Collected in 2014–2015 as part of the ESPA-funded ACES project, examining ecosystem services and rural wellbeing.
- Data linked to forest plots, agricultural surveys, and household datasets to assess ecosystem service use and provision.

## Methods and data collection
- Data sources:
  - Seven villages in Mabalane (Gaza Province), ten in Marrupa (Niassa), ten in Gurue (Zambezia).
  - Local tree names gathered from forest plots and agricultural surveys within sampled villages.
- Name standardization and species identification:
  - All local names (including spellings and synonyms) grouped into standardized local names.
  - Field identifications used where possible; dried samples cross-validated by botanists in Maputo.
- Uses data collection:
  - Mixed methods: focus groups, village surveys, key informant interviews, transect walks, ad-hoc observations.
  - Use categories varied by district: Mabalane recorded broad uses (charcoal, firewood, construction, wild foods, traditional medicines); Marrupa recorded more specific uses; Gurue used tablets/ODK with semi-structured questions.
- Granularity and harmonization:
  - Data amalgamated to district level due to varying data intensity by village.
  - Local languages were consistent within districts, enabling transfer of names between villages in the same district.
- Data coverage and caveats:
  - Not all uses recorded for every species; some species not identified.
  - Differences in methodologies across districts noted in accompanying text and data descriptions.

## Data structure and content
- Single data file: tree_species_identification_and_uses.csv
- Key fields:
  - survey_id: 5 = Mabalane, 6 = Marrupa, 7 = Gurue
  - recorded_local_name: all recorded local names and synonyms
  - standardised_local_name: assigned standardized local name
  - species_name: identified genus and species
  - identification_notes: uncertainties in identification
  - specific_use: detailed local use where recorded
  - charcoal, firewood, construction, food, medicine, cultural b, hunting b: binary indicators of recorded uses
- Unidentified species are labeled as unknownX_location (location = district; gaza = Mabalane, niassa = Marrupa, gurue = Gurue)
- Missing data are represented as blanks; cultural and hunting uses not recorded in Mabalane (survey 5)

## Quality control and governance
- Quality assured by lead authors; field teams trained with translators; translations between local languages, Portuguese, and English performed.
- Preference given to field identifications over dried samples when uncertain; samples cross-validated by Maputo botanists when needed.
- Standardization of local names performed by the lead author to ensure consistency.
- Data variability acknowledged: differences may arise between sites due to evolving methods; district-level amalgamation limits village-level disaggregation.
- Data linked to other ACES datasets via survey_id to enable cross-dataset analyses (e.g., forest plots, agricultural surveys).

## Usage, limitations and context
- Intended to support assessment of ecosystem service use and provision from local woodlands and fields.
- Limitations:
  - District-level aggregation means per-village insights are limited.
  - Not all tree uses are comprehensively captured; some cultural or hunting uses are incomplete or absent in certain districts.
  - Some species remain unidentified, and data quality may vary by site due to methodological evolution.

## References and sources
- ESPA ACES project methodology and funding context
- Field guides and cross-validation references:
  - Coates Palgrave (2003); van Wyk & van Wyk (1997)
  - Woollen et al. (2016) on related ecosystem service considerations