# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

- Overview: A six-file dataset providing life-cycle ecology traits, host plant relationships, breeding habitats, morphology, conservation status, distribution and abundance trends for butterflies and macro-moths of Great Britain and Ireland. Includes metadata and cross-references to multiple sources; must be cited in publications.

- Purpose for data leaders: exemplifies a multi-file, trait-centric biological database that integrates species-level traits with distributional and ecological context, highlighting data provenance, metadata detail, and the need for clear data boundaries and standards when assembling a data asset for broader use.

## What the dataset contains

- six files in total:
  - ecological_traits.csv: core traits data
  - excluded_species.csv: list of excluded Lepidoptera species (mainly adventive or micro-moths)
  - excluded_subspecies.csv: excluded subspecies/forms
  - hostplant_list_stacked.csv: raw host plant data (multiple rows per species)
  - hostplant_list_unstacked.csv: one row per species with hostplants as columns
  - ReadMe.doc: metadata, derivation criteria, and references
- metadata and documentation are designed to explain data derivation, column meanings, and data sources.

## Key contents and structure of ecological_traits.csv

- Life cycle ecology and phenology
- Host plant specificity and characteristics
- Breeding habitat and morphological characteristics
- Conservation status, distribution (occupancy) trends, and abundance trends
- Data notes on data resolution: broad categories and subcategories
- Distribution and abundance data align with political boundaries and sources (Great Britain, United Kingdom, Ireland, etc.)
- Example header concepts include:
  - taxonomic identifiers (abh_number, b&f_number, etc.)
  - species names and common names
  - presence/occurrence indicators across regions (England, Wales, Scotland, Northern Ireland, Ireland)
  - status indicators: reintroduced, immigrant, resident, extinct, red-list
  - distribution and abundance trends (long-term, short-term, significance, ranges)
  - phenology by life stage (egg, larval, pupal, adult) across months
  - overwintering strategies and stages
  - host plant specificity (monophagous, oligophagous, polyphagous) and hostplant counts
  - hostplant-related environmental values (Ellenberg values for light, moisture, reaction, nitrogen, salt tolerance)
  - broad and sectioned habitat/breeding habitat categories
  - host plant section preferences and common hostplants list
- Data provenance notes include:
  - sources for presence/occurrence and trends (e.g., BNM, NMRS, MothsIreland, Rothamsted Insect Survey, UKBMS)
  - references for phenology and life cycle data (e.g., Waring & Townsend, Henwood et al., Eeles, Randle et al.)
  - habitat and hostplant classifications guided by field guides and expert sources
- Data interpretation notes:
  - some columns use 1/0/2/3 and '?' markers to denote certainty and partial data
  - egg/larval/pupal/adult monthly columns reflect presence/occurrence with notes on possible latitudinal differences not explicitly modeled
  - units and boundaries align with defined political areas and time ranges

## Files and headers (Table-level descriptions)

- Table 2 (Headers of ecological_traits.csv): explains column meanings, data sources, and cases where headers are merged for space; notes on political boundary definitions:
  - Great Britain: England, Scotland, Wales
  - United Kingdom: GB + Northern Ireland
  - Ireland: island of Ireland
  - Additional notes for Republic of Ireland, Isle of Man, and Channel Islands where relevant
- Table 3 (Headers of excluded_species.csv): standard header definitions for excluded species
- Table 4 (Headers of excluded_subspecies.csv): header definitions for excluded subspecies
- Table 5 (Headers of hostplant_list_stacked.csv): description of stacked hostplant data
- Table 6 (Headers of hostplant_list_unstacked.csv): description of unstacked hostplant data
- ReadMe.doc: detailed methodology, column derivation, and references
- File sizes and counts provided (ecological_traits: 970 rows, 331 KB; excluded_species: 2022 rows, 97 KB; excluded_subspecies: 276 rows, 19 KB; hostplant_list_stacked: 4955 rows, 179 KB; hostplant_list_unstacked: 798 rows, 612 KB)

## Data provenance and usage

- Primary citation required when using the dataset:
  Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
- Acknowledges numerous data sources and collaborators; includes permissions to incorporate raw hostplant data and guidance on interpreting estimated body mass data.

## Data quality, limitations, and considerations for data leaders

- Complex, multi-source integration:
  - diverse origins for presence, trends, phenology, and hostplant data
  - clear attributions to multiple boundary definitions and timeframes
- Data granularity and gaps:
  - varying levels of detail across traits and life stages
  - some data are not latitudinally adjusted (phenology notes)
  - certain entries marked with uncertain status ( '?', 2, or blank)
- Data standardization needs:
  - multiple nomenclatural sources for plants and species; alignment via Stace (2019) and Henwood et al. (2020)
  - standardized Habitat and Breeding Habitat taxonomy with broad and subcategories
- Temporal coverage and trends:
  - long-term and short-term distribution and abundance trends derived from specific schemes (e.g., BNM, NMRS)
  - trend significance flags (Y/N) and ranges (range_long_term, range_short_term) included
- Access and reuse considerations:
  - dataset requires proper citation; no explicit license noted in summary
  - ReadMe and metadata provide key guidance for reproducibility and interpretation

## Practical implications for data strategy

- Demonstrates a comprehensive data product that fuses trait data, distribution, phenology, and habitat preferences into a single reference resource.
- Highlights importance of:
  - robust metadata and provenance to enable trust and reuse
  - explicit boundary definitions and time ranges for cross-region analyses
  - clear treatment of uncertainty and data gaps
  - documentation of data transformations and criteria in ReadMe/doc
- Could inform design of future data assets:
  - establish data standards across traits, hostplants, and habitat categories
  - create governance around data sources, versioning, and updates
  - plan for integration with external networks and communities of practice
- Applications for policy and practice:
  - supports assessment of conservation status with trait- and trend-based insights
  - informs prioritization of data collection to fill identified gaps (e.g., granularity, harmonization)

## References and acknowledgments

- Comprehensive references section listing primary taxonomic checklists, red lists, field guides, and monitoring programs
- Acknowledges data authors, organizations, and publishers who contributed raw data and guidance (e.g., Henwood, Sterling, Lewington; Moths Ireland; UKBMS; Rothamsted Insect Survey)