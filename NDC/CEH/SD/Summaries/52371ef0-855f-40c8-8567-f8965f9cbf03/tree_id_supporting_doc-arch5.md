# Local tree names, uses and species identification in Mozambique: supporting documentation

## Overview
- Dataset documenting local tree names, species identification, and local uses across 17 villages in three Mozambican districts (Mabalane in Gaza, Marrupa in Niassa, Gurue in Zambezia).
- Collected as part of the ESPA-funded ACES project (2014–2015) to understand ecosystem services and rural well-being.
- Data linked to forest plots, agricultural surveys, and household datasets to assess ecosystem service use and provision.
- Aims to reflect local knowledge and governance of tree resources, with data quality assurance by project authors and local collaborators.

## Dataset scope and contents
- Variables capture:
  - Local names (including all spellings and synonyms)
  - Standardised local names
  - Identified genus/species
  - Uncertainties in identification
  - Recorded uses (detailed where collected): charcoal, firewood, construction, food, medicine, cultural uses, hunting uses
- District-level amalgamation: data are not disaggregated to individual villages; district-level summaries reflect varying data collection intensities and local languages.
- Data not always complete: some uses not recorded; some species unidentified; certain cultural/hunting data missing in Mabalane.

## Data structure and access
- Dataset: tree_species_identification_and_uses.csv
- Key fields per district (survey_id):
  - survey_id (5 = Mabalane, 6 = Marrupa, 7 = Gurue)
  - recorded_local_name (all spellings/synonyms)
  - standardised_local_name (assigned local name)
  - species_name (identified genus/species)
  - identification_notes (uncertainties)
  - specific_use (detailed uses)
  - charcoal, firewood, construction, food, medicine, cultural b, hunting b (binary yes/blank for record/unknown)
- Unidentified species labeled as unknownX_location (location = district)
- Data linked to other ACES datasets via survey_id

## Methodology and standardization
- Data collected through:
  - Focus group discussions, village surveys, key informant interviews, transect walks, and ad-hoc observations
  - Gurue district used tablets with Open Data Kit (ODK) for local use data
- Standardization process:
  - All local names grouped into standardized forms
  - Field identifications prioritized over dried samples when available
  - Dried samples sent to Maputo for botanist cross-validation when uncertain
  - Local names designed to be transferable within districts
- Identification support:
  - Field identifications cross-validated with field guides and botanists
  - If uncertain, samples used to confirm species

## Quality control and uncertainties
- QA performed by first and second authors
- Field teams trained; translators used for language consistency
- Translations from local language to Portuguese/English; English translations reviewed by lead author
- Unknown species labeled systematically (unknownX_location)
- Some categories (cultural/hunting uses) were not collected in all districts (e.g., not collected in Mabalane)

## Data governance, interoperability, and provenance
- Data collected and curated to support interoperability with forest plot and agricultural survey datasets
- Standardized naming and detailed metadata support discoverability and potential reuse
- Project context and methodologies documented; references include Coates Palgrave field guides and prior ESPA/NERC-supported work
- Provisions for differing methodologies across sites acknowledged in dataset descriptions

## Limitations and considerations for use
- Not disaggregated to the village level; district-level aggregations may obscure local variation
- Data collection intensity varied by district, affecting completeness of certain uses
- Methods evolved over the project, so cross-site comparability may be limited
- Some species identifications remain uncertain or unnamed; interpret uses as potential rather than site-specific
- Some use categories not recorded in certain districts (e.g., cultural/hunting uses in Mabalane)