# Local tree names, uses and species identification in Mozambique: supporting documentation

## Overview
- GIS-ready dataset documenting local tree names, species identification, and local uses across 17 villages in three Mozambican districts.
- Collected in Mabalane (Gaza Province), Marrupa (Niassa Province), and Gurue (Zambezia Province) during 2014–2015.
- Part of the ESPA-funded ACES project to understand how land-use changes affect ecosystem services and rural livelihoods.
- Data linked to forest plot and agricultural survey datasets (submitted separately) for integrated ecosystem service analyses.
- District-level aggregation: local uses are amalgamated to the district level; village-level disaggregation is not provided.

## Geographic and temporal coverage
- Districts and survey scope:
  - Mabalane District, Gaza Province: 7 villages (survey 5)
  - Marrupa District, Niassa Province: 10 villages (survey 6)
  - Gurue District, Zambezia Province: 10 villages (survey 7)
- Data collection periods:
  - Mabalane: May–September 2014
  - Marrupa: May–August 2015
  - Gurue: September–December 2015
- Languages: local names standardized within each district; cross-district consistency maintained through standardization.

## Data content and structure
- Core dataset: tree_species_identification_and_uses.csv
- Key fields:
  - survey_id: district identifier (5 = Mabalane, 6 = Marrupa, 7 = Gurue)
  - recorded_local_name: local tree name (all spellings/synonyms recorded)
  - standardised_local_name: standardized local name assigned
  - species_name: identified genus and species (where possible)
  - identification_notes: uncertainties in species identification
  - specific_use: detailed local use notes
  - charcoal, firewood, construction, food, medicine, cultural b, hunting b: binary indicators (yes or blank) for reported uses
- Data nuances:
  - When species were unidentified, names appear as unknownX_location (X = unique number; location indicates district)
  - Cultural and hunting uses not systematically recorded in Mabalane
  - Some fields blank where data were not recorded or not applicable
- Data linkage: survey_id links to other ACES datasets (forest plots, agricultural field surveys) for integrated analyses

## Collection methods and standardization
- Data collection approaches:
  - Focus group discussions, village surveys, key informant interviews, transect walks, ad-hoc observations
  - In Gurue, uses recorded with tablets/ODK using semi-structured questions
- Standardization and verification:
  - Lead author grouped local names and synonyms into standardized local names
  - Field identifications preferred over dried sample identifications when both were available
  - Samples collected and cross-validated by botanists in Maputo when identification was uncertain
  - Identification keys referenced: van Wyk and van Wyk 1997; Coates Palgrave 2003
- Quality assurance:
  - All data quality assured by first and second authors
  - Field teams trained; translators provided; Portuguese notes translated to English

## Implications for GIS work (data suitability and caveats)
- Strengths for GIS:
  - Standardized local names mapped to species where possible
  - Clear district-level aggregation supports regional mapping of species and uses
  - Linkage to other spatial datasets (forest plots, agricultural surveys) for ecosystem service analyses
- Limitations and uncertainties:
  - District-level amalgamation: village-level variation not captured spatially
  - Data collection intensity varied by district; some uses not recorded or incomplete
  - Some species identifications are uncertain or listed as unknown
  - Some recorded uses are “potential uses” rather than confirmed per village
- Practical cautions:
  - Treat district as the primary spatial unit; avoid assuming village-level granularity
  - Consider uncertainties in species identification and uses when performing overlays or modeling
  - Use data quality notes and unknown labels to assess confidence in mapped outputs

## Related datasets and references
- Linked ACES datasets: forest plots and agricultural field surveys (dataset descriptions submitted separately)
- ESPA ACES project context on ecosystem services and poverty alleviation
- Data documentation references:
  - Coates Palgrave (2003)
  - van Wyk and van Wyk (1997)
  - Woollen et al. (2016) on ecosystem services trade-offs
- Principal authors and affiliations: University of Edinburgh, Universidade Eduardo Mondlane, University of Zimbabwe, Universidade Lurio, Universidad Zambeze, among others

## Access and usage notes
- Data stored in the single spreadsheet: tree_species_identification_and_uses.csv
- Values may be blank where data were not recorded or not applicable
- Survey IDs (5, 6, 7) correspond to the three districts, enabling integration with district-level analyses and other ACES datasets