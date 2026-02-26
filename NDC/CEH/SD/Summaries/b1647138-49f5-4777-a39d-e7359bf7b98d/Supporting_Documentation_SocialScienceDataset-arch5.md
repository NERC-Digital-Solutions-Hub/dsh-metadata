# Economic and social science questionnaire dataset, Mambwe District, Zambia (2013)

## Overview
- Dataset from 211 household surveys in Mambwe District, Eastern Zambia, as part of a broader study on human and animal trypanosomiasis and settlement changes.
- Focus: household wellbeing in relation to assets, health (human and animal), veterinary and medical services, livestock, wildlife interactions, crop production (notably cotton), migration, water, fuel, poverty, resilience, and ecosystem changes.
- Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC); funded by NERC (NE/J000701/1) with ESPA support.

## Lineage, data collection and processing
- Lineage and sampling
  - Based on a census (Aug 2012–Oct/Nov 2012) of 3,717 households; 211 households selected for the study.
  - One-stage cluster survey aimed to estimate trypanosomiasis prevalence; sample size extended by 50% to include households without livestock/dogs.
  - Interviewed households selected from the census sample frame; consent obtained prior to interviews and blood sampling.
- Data collection
  - Semi-structured interviews conducted in local languages (Chikunda, Chichewa) with translation support; some responses in English.
  - Blood sampling for people and livestock; data collection occurred offline on tablets using droidSURVEY.
  - Data uploaded daily when internet available; stored securely on a server.
- Data capture and processing
  - Questionnaire designed for offline entry; various question formats (multiple choice, grid, open-ended).
  - Data downloaded to Microsoft Excel, anonymised, and then exported as CSV for ingestion into the Environmental Information Data Centre (EIDC).
  - Extensive data cleaning and transformation applied to convert to clean variables, with coding schemes (e.g., single-letter codes, numeric codes) and handling of missing values.
- Anonymisation and storage
  - Personal identifiers removed (names, GPS locations, interviewer names); household numbers retained.
  - Final dataset named Socio-econ_Zambia_DDDAC_2017 (.csv) with documented variable definitions.

## Data structure and metadata
- Dataset: Socio-econ_Zambia_DDDAC_2017.csv
- Coverage by sections (domains)
  - Household information and demographics (size, head, tribe, marriages, education)
  - Education and literacy
  - Health services and human health (health centre access, costs, satisfaction, training, deaths, disease, treatment)
  - Water and sanitation (water access, quality, scarcity, toilets)
  - Livestock and veterinary care (availability of veterinary services, drugs, sources, treatments, prevention)
  - Animal production (ownership, species, numbers, mortalities, off-take, intake, births, traction)
  - Fauna/wildlife, tsetse flies and interactions
  - Crop/vegetable production (vegetation change, cotton farming, pesticide use)
  - Migration and mobility (immigration, reasons, seasonal migration)
  - Economic status/poverty (land area, maize storage, assets, energy usage)
  - Resilience and assets (nutrition, malnutrition awareness, savings, social networks)
  - Value setting (possession value, household priorities, market perceptions)
- Variable coding and documentation
  - A comprehensive set of variables with descriptive names and coded options (e.g., Yes/No, numeric counts, categorical codes)
  - Special codes for missing or not applicable: '\' for not applicable, '#' for no reply
- Language and translation notes
  - Data recorded in regional languages with translation; some terms (e.g., disease signs) are context-specific and not always map to single diseases.
- Data provenance and authorship
  - Authors include Kathrin Schaten, Alexandra Shaw, Noreen Machila, Martin Simuunza, Emmanuel Chirwa, Neil Anderson, Ewan MacLeod, and Susan Welburn; project integration with DDDAC
  - Funding acknowledged (NERC project NE/J000701/1; ESPA support)

## Data quality, cleaning and governance
- Quality assurance
  - Thorough cleaning of Excel-derived data prior to CSV export; creation of distinct coding for all responses; consolidation of “other” responses into defined codes; handling of blank cells.
  - Anonymisation performed consistently (removal of personal identifiers) with retention of household identifiers for linkage.
- Metadata and traceability
  - Documented lineage from census sampling to final CSV; detailed variable definitions and coding schemes accompanying the dataset.
  - Data collection methods, languages, software (droidSURVEY), offline to online workflow, and data transfer steps are described to support reproducibility.
- Interoperability considerations
  - Dataset prepared for ingestion into the Environmental Information Data Centre (EIDC); standardized CSV format facilitates sharing with researchers and data repositories.

## Access, sharing and governance considerations for Data Stewards
- Storage and sharing
  - Data stored securely on a server and shared via EIDC for ingestion and discoverability.
  - Anonymised dataset prepared to enable secondary analyses while protecting participant privacy.
- Licensing and reuse
  - Documented provenance and consent practices; explicit licensing details are not provided in the document; data stewards should attach an appropriate data-use license and any access controls as part of governance.
- Versioning and updates
  - Clearly traceable lineage from field collection through cleaning to final CSV; consider versioning to manage updates or reprocessing.
- Reproducibility and provenance
  - Detailed description of sampling design, data collection instruments, languages, and coding ensures reproducibility and proper attribution for secondary users.

## Practical implications and usage notes for Data Stewards
- What the data enable
  - Cross-disciplinary analyses linking household welfare with health, livestock health, agricultural practices (cotton farming), migration patterns, resource access, and resilience indicators.
- Cautions
  - Temporal limitation: data from 2013; may need contextualization for current analyses.
  - Sampling design implications: one-stage cluster with oversampling; potential biases around livestock ownership status.
  - Language translation nuances may affect interpretation of certain variables (e.g., disease signs, local terminology).
- Recommendations for stewardship
  - Maintain comprehensive metadata describing variable definitions, coding schemes, and data cleaning steps.
  - Ensure licensing, access controls, and usage guidelines are clearly defined and attached to the dataset.
  - Provide versioned updates if reprocessing or extending the dataset; document changes in a changelog.
  - Facilitate interoperability by preserving the CSV structure and providing a machine-readable data dictionary aligned with the variable table.

## Authors and acknowledgments
- Authors: Kathrin Schaten; Alexandra Shaw; Noreen Machila; Martin Simuunza; Emmanuel Chirwa; Neil Anderson; Ewan MacLeod; Susan Welburn
- Acknowledgments: Recognition of local contributors, translators, field staff, and support from the broader DDDAC program.