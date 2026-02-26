# Local tree names, uses and species identification in Mozambique: supporting documentation

## Overview
- Dataset of local tree names, species identifications, and local uses across 17 villages in three Mozambican districts (Mabalane, Marrupa, Gurue).
- Collected in 2014–2015 as part of the ESPA-funded ACES project, which studies how changing land use affects ecosystem services and rural wellbeing.
- Data are linked to forest plots, agricultural surveys, and household datasets to assess ecosystem service use and provision from local woodlands and fields.
- Local names were standardized and species identifications validated in the field and by botanists; some uses and identifications vary by district due to evolving methods.

## Data collection and methods
- Sites: 7 villages in Mabalane (Gaza Province), 10 villages in Marrupa (Niassa Province), 10 villages in Gurue (Zambezia Province).
- Timeframe: Mabalane (May–Sep 2014), Marrupa (May–Aug 2015), Gurue (Sep–Dec 2015).
- Data sources: forest plots and agricultural field surveys within sampled villages; field identifications and, when uncertain, dried samples sent to Maputo for cross-validation by botanists.
- Local name standardization: all recorded spellings/synonyms grouped; a standard local name assigned.
- Uses data collection: focus group discussions, village surveys, key informant interviews, transect walks, ad-hoc observations; Gurue used tablets/ODK for data capture.
- Level of aggregation: uses are recorded at the district level (not village-level); within-district languages were consistent to allow transferability of local names.

## Data structure and content
- File: tree_species_identification_and_uses.csv
- Key fields:
  - survey_id: 5 = Mabalane, 6 = Marrupa, 7 = Gurue
  - recorded_local_name: local tree name as recorded (includes synonyms)
  - standardised_local_name: assigned standardized local name
  - species_name: identified genus and species
  - identification_notes: uncertainties in identification
  - specific_use_a: detailed recorded uses (district-dependent)
  - charcoal, firewood, construction, food, medicine, cultural_b, hunting_b: binary indicators (yes/no or blank) for recorded uses
- Notes:
  - When species are unidentified, labeled as 'unknownX_location' (location = district; X = unique number)
  - Cultural and hunting uses not recorded in Mabalane (5) and thus left blank there
  - Data missing in fields are represented by blanks
- Data linkage: survey_id connects to other ACES datasets (forest plots, agricultural surveys); district-level categorization corresponds to the study districts (5, 6, 7)

## Quality control
- Data quality assurance performed by the first and second authors.
- Field teams trained; translators used to bridge local languages to Portuguese/English.
- In cases of multiple identifications for the same local name, the field identification was preferred over dried samples when possible.
- Uncertain identifications labeled as 'unknown'; standardization of local names performed consistently by the lead author.

## Limitations and caveats
- Methods evolved across sites, so data may vary slightly between districts.
- Data are not disaggregated to the village level; district-level aggregation means some specificity is lost.
- Not all uses for every species were recorded; some species remained unidentified.
- Mabalane data lack detailed cultural and hunting use data and certain use categories.
- Diversity in data collection intensity across villages may affect the completeness of use records.

## Usage and context
- Purpose: enable analysis of how local tree species and their uses contribute to ecosystem services and human wellbeing, within the ACES framework.
- Integration: designed to be combined with forest plots and agricultural surveys to assess ecosystem service provisioning and potential trade-offs (e.g., charcoal production vs. other services).
- Supported by references and taxonomic keys for identification (e.g., Coates Palgrave, van Wyk and van Wyk) and linked to broader ACES outputs (e.g., Woollen et al. 2016 on charcoal production and ecosystem services).

## Access and references
- Data product: single spreadsheet (tree_species_identification_and_uses.csv) with accompanying metadata.
- Funding and project context: ESPA ACES project, funded by UK research councils and DFID.
- Key references for methods and taxonomy:
  - Coates Palgrave (2003)
  - van Wyk & van Wyk (1997)
  - Woollen et al. (2016) on charcoal production and ecosystem services
- Dataset authors and institutional affiliations: multiple Mozambican and international institutions, with fieldwork conducted in Mozambique and Maputo-based botanical validation.