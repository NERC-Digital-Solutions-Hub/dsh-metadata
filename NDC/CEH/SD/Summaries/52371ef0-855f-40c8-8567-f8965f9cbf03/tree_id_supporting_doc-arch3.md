# Local tree names, uses and species identification in Mozambique: supporting documentation

## Overview
- Dataset documenting local tree names, species identification, and local uses across 17 villages in three Mozambican districts.
- Part of the ESPA-funded ACES project on how land-use changes affect ecosystem services and rural wellbeing.
- Data linked to forest plots, agricultural surveys, and household datasets to assess ecosystem service use and provision.

## Scope and context
- Location and timing:
  - Mabalane District, Gaza Province (7 villages): May–Sept 2014
  - Marrupa District, Niassa Province (10 villages): May–Aug 2015
  - Gurue District, Zambezia Province (10 villages): Sep–Dec 2015
- Data collected from forest plots and agricultural field surveys within sampled villages; local uses captured via interviews, focus groups, surveys, and ad-hoc observations.
- Standardization and verification:
  - Local names consolidated into standardized names; species identified in the field when possible, with cross-validation by botanists in Maputo for uncertain cases.
  - Some sites used digital data collection (Gurue with tablets/ODK); cultural/hunting uses not consistently recorded in all districts.

## Data collection methods
- Approaches:
  - Focus group discussions, village surveys, key informant interviews, transect walks, ad-hoc observations.
  - Field identification prioritized; dried samples collected for cross-check when needed.
- Uses recorded by district:
  - Mabalane: broad use categories (charcoal, firewood, construction, wild foods, traditional medicines); fewer specific uses recorded.
  - Marrupa: specific local uses captured.
  - Gurue: semi-structured surveys with ODK; more detailed use entries.
- Data are aggregated at the district level (not disaggregated to individual villages); within-district language consistency allows transferability of local names.

## Data structure and contents
- One main dataset: tree_species_identification_and_uses.csv
- Key fields:
  - survey_id (5 = Mabalane, 6 = Marrupa, 7 = Gurue)
  - recorded_local_name (all spellings/synonyms recorded)
  - standardised_local_name (assigned standardized name)
  - species_name (identified genus and species)
  - identification_notes (uncertainties)
  - specific_use (detailed uses where recorded)
  - charcoal, firewood, construction, food, medicine, cultural_b, hunting_b (binary indicators; 'yes' indicates record; blanks indicate no/unknown)
- Unidentified species labeled as unknownX_location (location corresponds to district)

## Quality control and provenance
- Data quality assured by the first two authors; field teams trained; translators provided; field identifications preferred over dried samples when conflicts arose.
- Translation workflow: Portuguese field notes translated to English; standardized local names assigned by lead author.
- Management of uncertainty:
  - If identification was very uncertain, species labeled as 'unknown'.
  - Local names and synonyms standardized for consistency.

## Limitations and considerations for monitoring frameworks
- District-level aggregation limits village-level granularity; nuanced village-level patterns may be obscured.
- Not all possible uses were recorded; some districts lack detailed cultural/hunting data.
- Variability in data collection methods across districts due to evolving methodologies.
- Some species remain unidentified; potential gaps in metadata and context for uses.

## Linkage and relevance for monitoring
- Data are designed to support linking with forest plot and agricultural survey datasets to evaluate ecosystem service use and provisioning by local tree species.
- Provides a structured basis for monitoring tree diversity, local knowledge, and use patterns as part of broader environmental health and livelihoods assessments.
- Useful for cross-district comparisons and for informing data governance and metadata needs in monitoring frameworks.

## References
- Coates Palgrave K (2003) Trees of Southern Africa; Coates Palgrave M (ed) (2003) Trees of Southern Africa; van Wyk B, van Wyk P (1997) Field Guide to Trees of Southern Africa; Woollen E et al. (2016) Charcoal production in the Mopane woodlands of Mozambique.