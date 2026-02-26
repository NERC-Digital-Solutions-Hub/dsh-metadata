# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A six-file dataset (with a ReadMe and supplementary metadata) compiling ecological and phenological traits, host plant associations, and distributional information for butterflies and macro-moths of Great Britain and Ireland.
- Aims to support research, conservation planning, and data-driven decision-making by providing standardized trait data and provenance.

## Data contents and structure
- ecologcial_traits.csv
  - Contains life cycle ecology, phenology, host plant specificity, breeding habitat, morphological traits, conservation status, distribution and abundance trends.
  - Includes data at varying resolutions (broader categories broken into sub-categories).
  - Provides presence/absence by political boundary (Great Britain, United Kingdom, Ireland, etc.) with headers and metadata describing data derivation.
  - Monthly phenology columns (e.g., egg_stage, larval_stage, pupal_stage, adult_stage) and overwintering strategy, along with categories for diurnal/nocturnal activity, disturbance sensitivity, communal nesting, and pupation environments.
  - Host plant data: specificity, number of hostplants, hostplant category, hostplant sections, common hostplants, habitat associations, and Ellenberg environmental values.
  - Habitats and breeding habitat classifications include detailed subcategories and upland associations.
- excluded_species.csv
  - List of Lepidoptera species excluded from the database (mainly adventive or micro-moths) with identifiers (abh_number, b&f_number, scientific_name, vernacular_name, family).
- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded, with similar identifying fields as above.
- hostplant_list_stacked.csv
  - Raw data on larval host plant preferences; each row links an species (by abh_number) to a hostplant; includes hostplant_category (main/occasional).
- hostplant_list_unstacked.csv
  - Table-formatted host plant data; each row for a species includes multiple hostplants listed across columns and a total column; rows indicate whether a given hostplant is used.
- ReadMe.doc
  - Detailed information on column derivations, data provenance, criteria for numbering, and references used.
  - Table1 lists files in the repository and provides high-level metadata about each file.
- Header documentation (Table 2 and related notes within ecological_traits.csv)
  - Explanations for header fields, data sources, and the meaning of coded values (e.g., presence/absence indicators, trends, and boundary definitions).

## Data model, headers, and provenance
- Header and data semantics
  - Multiple identifiers are provided (abh_number, b&f_number, Wiemers/K&R numbers) to align with established checklists and taxonomic references.
  - Distribution and abundance data are linked to political boundaries; definitions include Great Britain, United Kingdom, Ireland, and other specific areas (Isle of Man, Channel Islands) as applicable.
  - A rich set of status indicators (reintroduced, immigrant, resident, extinct in GB/IRE, red list status) capture conservation context.
  - Detailed life-stage monthly indicators (egg_stage, larval_stage, pupal_stage, adult_stage) reflect phenology; some cells note uncertainty or multiple overwintering strategies.
  - Hostplant data integrate monophagous/oligophagous/polyphagous classifications, counts of hostplants, and ecological traits of hostplants (Ellenberg indicator values for light, moisture, reaction, nitrogen, etc.).
  - Habitat and breeding habitat categorizations include both broad and specific subcategories; notes clarify exceptions (e.g., hedgerows, wet woodland, upland definitions).
- Data sources and references
  - Data compiled from multiple sources: Agassiz et al. (2013), Emmet & Heath (1991, 1992), Henwood et al. (2020), Waring & Townsend (2017), Hill et al. (1999), Rothamsted Insect Survey, UKBMS, MothsIreland, NMRS, BNM, and others.
  - Acknowledgments for data contributions and permissions, including permission to incorporate raw larval hostplant data from Bloomsbury.

## Provenance, usage, and citation
- Publication and citation
  - The dataset should be cited as: Cook, P.M., et al. 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, UK.
- Acknowledgments and permissions
  - Acknowledges authors of source datasets and specific permissions for hostplant data usage.
- Versioning and updates
  - The ReadMe-style documentation indicates a structured provenance trail (data derivation, column definitions, and references) to assist future updates and governance.

## Access, reuse, and governance
- Sharing and interoperability
  - Data are stored in separated CSV files with a comprehensive ReadMe and header documentation to facilitate reuse, integration, and standardization.
  - The dataset emphasizes consistent metadata and data formatting to support discovery and interoperability across systems.
- Licensing and reuse expectations
  - While a formal license isn’t stated in the excerpt, the dataset requires citation to Cook et al. (2021) for publication-based use, and emphasizes proper attribution for derived analyses.
- Data availability considerations
  - The metadata notes that distribution and abundance data exist for varying political boundaries depending on the source; provenance documentation clarifies boundary definitions used for analyses.
  - Some phenology fields note that latitudinal variation was not accounted for in certain columns, which is important for downstream analyses and data integration.

## Data quality, challenges, and stewardship considerations
- Quality and completeness
  - The dataset consolidates information from many sources and provides extensive metadata to support quality assessment and traceability.
  - Potential data gaps or uncertainties are explicitly noted in phenotype and overwintering fields (e.g., '?' indicators for uncertainty, multiple overwintering strategies).
- Reproducibility and governance
  - The ReadMe and header documentation provide a transparent trail of data derivation, criteria, and sources, supporting reproducibility and governance for Data Stewards.
- Practical data stewardship implications
  - For ingestion: align taxonomic identifiers across sources (abh_number, b&f_number, Wiemers/K&R numbers), map boundary definitions to current governance regions, and record data provenance.
  - For quality assurance: verify monthly phenology indicators against source publications; ensure hostplant associations reflect Henwood et al. (2020) and Stace (2019) taxonomies; confirm Ellenberg values are correctly applied per hostplant.
  - For updates: maintain a changelog linking new data to original sources; document any reclassifications or boundary changes; address latitudinal phenology nuances as needed.
- Challenges mirrored from archetype context
  - Incomplete user needs assessment for specialized trait data.
  - Timely ingestion from diverse sources with varying formats.
  - Ensuring metadata completeness and standardization across many systems and data types.
  - Handling large, complex datasets with countries/regions that require careful boundary alignment.
  - Updating older, non-interoperable data with a harmonized schema.

## Guidance for Data Stewards (practical takeaways)
- Ensure robust metadata coverage: maintain complete ReadMe and per-file header documentation; preserve provenance links to all source materials.
- Enforce consistent taxonomic identifiers and boundary definitions to support cross-dataset discovery and integration.
- Apply quality assurance workflows: validate life-stage, phenology, and hostplant fields against source references; flag uncertainties; document decisions.
- Plan for updates and governance: establish a versioning and change-notification process; capture any methodological changes (e.g., boundary redefinitions or data source updates).
- Facilitate reuse: include clear citation guidance; preserve licensing constraints; provide access to all six data files with consistent naming and structure.