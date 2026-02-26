# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A compiled traits database for butterflies and macro-moths of Great Britain and Ireland, intended to support environmental health monitoring, policy scrutiny, and future decision-making.
- Six main data files (plus ReadMe and references) provide life cycle ecology, host-plant associations, and distribution/abundance information, with detailed metadata to support data governance and reuse.
- The dataset emphasizes transparency, data provenance, and ease of integration into monitoring reports and dashboards.

## Dataset contents and file descriptions
- ecological_traits.csv
  - Life cycle ecology and phenology; host plant specificity and characteristics; breeding habitat; morphological traits; conservation status; distribution/occupancy and abundance trends.
  - Contains multi-resolution categories and numerous trait columns, including occupancy/abundance by political boundaries (GB, UK, Ireland) and various trend metrics.
  - Monthly phenology indicators (egg, larval, pupal, adult stages) and overwintering strategies; diurnal/nocturnal activity; habitat and breeding data; hostplant relationships and plant-associated environmental values.
- excluded_species.csv
  - List of Lepidoptera species excluded from the database (mainly adventive or micro-moths).
- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv
  - Raw host plant data for larvae from Henwood, Sterling & Lewington (2020); multiple rows per species for each hostplant.
- hostplant_list_unstacked.csv
  - Restructured host plant data; one row per species with hostplant indicators across columns.
- ReadMe.doc
  - Detailed guidance on data derivation, column criteria, and metadata for ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, and both hostplant lists; explains numbering criteria and data provenance.
- Acknowledgments and References
  - Acknowledges data sources and provides full bibliographic references for underlying datasets and methods.

## Data structure and metadata
- Header and column notes
  - Table 2 in ReadMe documents header definitions, data sources, and column merging (e.g., monthly egg stage represented by 12 monthly columns).
  - Distribution and abundance data are aligned to political boundaries with metadata clarifying coverage (Great Britain, United Kingdom, Ireland, and related regions).
- Boundary definitions
  - Great Britain: England, Scotland, Wales; United Kingdom includes Northern Ireland; Ireland includes the island (Republic of Ireland and Northern Ireland); special notes for the Isle of Man and Channel Islands where relevant.
- Key data types in ecological_traits.csv
  - Taxonomic identifiers (e.g., ABH number, B&F number, various taxon checklists).
  - Status indicators: recorded_present, reintroduced, immigrant, resident, extinct, red_list_gb/ireland, occupancy/abundance trends, and statistical significance markers.
  - Phenology and life stages: diurnal/nocturnal, easily_disturbed_by_day, communal_nest, pupal/larval/adult_stage columns by month, overwintering_stage.
  - Ecology and behavior: larval hostplant specificity (monophagous/oligophagous/polyphagous), number_hostplants, hostplant_category and related hostplant metadata.
  - Hostplant environment and habitat: native/non-native status, Ellenberg light/moisture/reaction/nitrogen/salt_tolerance values, and broad_host_plant_categories.
  - Breeding habitat and habitat categories; host plant sections (roots, stems, leaves, etc.).
- Data scale
  - ecological_traits.csv: 331 KB, 970 rows.
  - hostplant_list_stacked.csv: 179 KB, 4,955 rows; hostplant_list_unstacked.csv: 612 KB, 798 rows.
  - Exclusion lists: smaller core datasets (tens to hundreds of rows).

## Provenance and data sources
- Primary publication: Cook, P.M. et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.
- Core data sources and references include:
  - Agassiz, Beavan & Heckford (2013); Wiemers et al. (2018); Karsholt & Razowski (1996) for taxonomic identifiers.
  - Butterfly monitoring and moth recording schemes: Butterflies for the New Millennium (BNM, 2021), National Moth Recording Scheme (NMRS, 2021), MothsIreland (2021), UKBMS, and related monitoring outputs.
  - Life cycle and phenology sources: Emmet & Heath (1991, 1992); Henwood, Sterling & Lewington (2020); Waring & Townsend (2017).
  - Habitat and plant data: Stace (2019); Ellenberg indicator values (Hill et al., 1999).
  - Mass and morphometrics: Kinsella et al. (2020) and related hazard caution notes for modeled estimates.
- Citation requirement
  - If used in publications, the dataset must be cited as Cook et al., 2021.

## Use in monitoring and policy evaluation
- Provides standardized trait and distribution data to inform environmental health measures, policy scrutiny, and decision-making.
- Supports:
  - Tracking long- and short-term distribution trends (GB and Ireland) and abundance trends.
  - Assessing species’ life-cycle timing, overwintering strategies, and phenology shifts (with notes on statistical significance and data range).
  - Linking species to hostplant preferences and habitat requirements, enabling impact assessments of habitat management and land-use changes.
  - Data governance through explicit metadata coverage by political boundary, data sources, and criteria for trait assignments.

## Data governance, challenges, and limitations
- Data quality and availability
  - Noted barriers include gaps in data, timely access, siloed datasets, and the need for metadata to verify suitability.
  - Some variables rely on model-derived estimates (e.g., estimated dry mass) or need cautious interpretation (e.g., latitude-agnostic phenology in monthly egg/larval/pupal data).
- Metadata and transparency
  - The ReadMe provides comprehensive guidance on column derivation, sources, and criteria to support data validation and reuse.
  - Some elements (e.g., monthly phenology) are generalized and may not capture latitudinal or regional phenology variation.
- Data sharing and governance
  - The dataset emphasizes transparent data provenance and explicit sharing of underlying data where possible; acknowledgments indicate collaboration with data providers and permission to incorporate raw data.
  - Public sharing considerations are addressed through metadata and documentation, aiding governance and governance-compliant dissemination.

## Citation and licensing
- Primary citation: Cook, P.M., et al., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland.
- Acknowledgments and references accompany the dataset, detailing sources and permissions related to data incorporation.

## Practical takeaways for policymakers and monitoring authors
- Use this database to ground environmental monitoring frameworks in standardized, source-documented traits and distribution data for Lepidoptera.
- Leverage the explicit boundary definitions and metadata to align monitoring outputs with regional policy scopes (GB, UK, Ireland, etc.).
- Combine ecological traits with hostplant and habitat data to model potential policy impacts on species distributions and phenology.
- Account for data gaps and uncertainty when interpreting trends, and rely on the ReadMe and Table 2 for methodological context and data provenance.