# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

- Purpose and use
  - A standardized, citable dataset to support monitoring of environmental health and policy performance by recording life-cycle ecology, phenology, host plant interactions, breeding habitat, and morphology for butterflies and macro-moths in Great Britain and Ireland.
  - Enables researchers and analysts to verify, quality assure, clean, and transform data from established sources and to present outputs (e.g., trends, distributions) in clear formats.

- Scope and boundaries
  - Geographic coverage includes Great Britain (England, Scotland, Wales) and Ireland (Republic of Ireland and Northern Ireland); references to other island groups are provided in metadata where relevant.
  - Data are drawn from multiple monitoring schemes and published datasets (e.g., BNM/NMRS, MothsIreland, UKBMS) and aggregated to consistent trait-based outputs.

- Dataset contents (six files)
  - ecological_traits.csv: core traits for life cycle ecology and phenology, host plant specificity and characteristics, breeding habitat, and morphological traits; includes conservation status, occupancy trend, and abundance trend. Contains broad categories with subcategories for data resolution. Headers and data values include complex, monthly phenology, overwintering, and geographic qualifiers.
  - excluded_species.csv: Lepidoptera species in Agassiz, Beavan & Heckford (2013) excluded from the database (primarily adventive or micro-moths).
  - excluded_subspecies.csv: Lepidoptera subspecies/forms excluded from the database.
  - hostplant_list_stacked.csv: raw data on larvae host plant preferences; multiple rows per species to reflect multiple hostplants.
  - hostplant_list_unstacked.csv: table-formatted hostplant data; one row per species with hostplants as columns; binary indicators denote known hostplant usage.
  - ReadMe.doc: detailed methodology on data derivation, column by column, criteria, and references; also includes a summary of data sources and how numbering/coding was applied.

- Data structure and key definitions
  - Headers and data columns in ecological_traits.csv are described in Table 2 (e.g., abundance, distribution, occupancy status, residency, migration, extinction status, long/short-term distribution trends, diurnal/nocturnal activity, larval/pupal/adult stages by month, overwintering strategies, and hostplant relationships).
  - Phenology and life-history data are provided on monthly scales (e.g., egg/larval/pupal/adult stages by month) and include indicators for uncertainty (e.g., '?') and multi-year overwintering.
  - Host plant data cover monophagous, oligophagous (genus or family), and polyphagous feeding strategies, with native/non-native status, Ellenberg environmental preference values, and broad host-plant categories.
  - Breeding habitat and habitat categorization include both broad and specific subcategories (e.g., broadleaved woodland, wet woodland, scrub/hedgerows, montane upland) and upland associations.
  - Data fields include conservation status (red lists), occupancy counts (e.g., 10 km squares), and long/ short-term distribution and abundance trends, with significance flags where available.

- Data provenance and references
  - Primary sources include Agassiz, Beavan & Heckford (2013); Wiemers et al. (2018); Henwood, Sterling & Lewington (2020); Emmet & Heath (1991, 1992); Hill et al. (1999); Waring & Townsend (2017); Rothamsted Insect Survey; UKBMS; MothsIreland; and related national monitoring and atlas publications.
  - The dataset is accompanied by a formal citation for publication and acknowledgment of data providers and permissions (Cook et al., 2021).

- Usage notes and cautions
  - Data may be bounded by political boundaries that vary by source; metadata clarifies the exact area covered per column.
  - Some fields rely on modeled estimates (e.g., estimated dry mass) or expert judgment; use with caution for cross-species biomass analyses.
  - Phenology and overwintering information may be latitude/region dependent; some entries do not account for latitudinal variation.
  - Native vs non-native status is determined from Stace (2019) and related sources; multiple hostplant interactions are captured, but some data may be incomplete for certain species.

- Accessibility, quality, and reutilization
  - Data are intended to be stored and uploaded to appropriate data portals; standardised formats and metadata support accessibility and reuse.
  - The six-file structure facilitates modular usage (traits, exclusions, hostplants) and allows cross-dataset linkage for integrated environmental monitoring analyses.
  - The dataset aligns with monitoring aims to demonstrate environmental health and policy performance over time by enabling trend analyses, distribution assessments, and habitat associations.

- Citation and acknowledgments
  - If used in publications, cite: Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.
  - Acknowledgments recognize contributors to source datasets and permission providers (e.g., Henwood, Sterling, Lewington) and the organizations supporting data compilation.

- Practical takeaway for analysts
  - Use ecological_traits.csv as the central resource to link species life history and habitat preferences to environmental indicators.
  - Cross-reference hostplant_list_stacked/unstacked.csv to analyze plant-pollinator/plant-herbivore relationships in ecosystem monitoring.
  - Leverage the exclusion lists to ensure transparency about taxa not included in analyses.
  - Consult ReadMe.doc for column-level definitions and data derivation details to ensure accurate interpretation and reproducibility.