# Economic and social science questionnaire dataset, Mambwe District, Zambia (2013)

- Scope and purpose
  - Results from 211 household surveys in Mambwe District, Eastern Zambia, examining human and animal health, household wellbeing, assets, and resource access.
  - Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC); informs understanding of disease ecology, settlement patterns, and ecosystem–poverty linkages.
  - Funded by NERC (NE/J000701/1) with support from ESPA.

- Data collection and lineage
  - Sampling: 211 households selected from a census-based sample frame (3717 households) conducted in Aug 2012 and Oct–Nov 2012; intended to estimate trypanosomiasis prevalence with expanded socio-economic sampling (including households with no livestock).
  - Fieldwork: June–August 2013; interviews conducted in local languages (Chikunda, Chichewa) with translations as needed; blood sampling for humans and livestock.
  - Data capture: Questionnaire and responses recorded on tablets using droidSURVEY; offline data collection with daily internet uploads; data stored securely before being anonymised and exported to Microsoft Excel; later converted to CSV for ingestion into the Environmental Information Data Centre (EIDC).
  - Anonymisation and storage: Removal of respondent names, GPS locations, and interviewers’ names; household numbers retained; data stored on secure servers and anonymised before release.
  - Dataset packaging: CSV file named Socio-econ_Zambia_DDDAC_2017; accompanying variable definitions and coding schemes documented (detailed in the dataset’s structure section).

- Data structure and content
  - Multi-domain questionnaire spanning 12 sections:
    - Household information; Education; Health services and human health; Water and sanitation; Veterinary services; Animal production; Fauna/wildlife, tsetse flies and contacts; Crop/vegetable production; Migration; Economic status/poverty; Resilience; Value setting.
  - Domains collected include demographics, health (human and animal), health service access and utilisation, livestock and wildlife interactions, agricultural practices (including cotton), migration patterns, asset ownership, energy use, nutrition, and social networks.
  - Data format and coding: Variables are stored in a structured CSV with descriptive variable names and coded responses; complex grid and “other” responses are converted to defined codes; missing values coded as not applicable (\) or not answered (#); household-level identifiers retained for internal linkage.

- Metadata, documentation, and quality considerations
  - Comprehensive documentation exists for variable names, definitions, and coding, with an emphasis on traceability of responses (e.g., section 2 Household information, section 5 Water and sanitation, section 6 Veterinary services, etc.).
  - Data cleaning undertaken to standardise responses (e.g., consolidating “other” replies into coded categories; converting free text into categorical codes); thorough cleaning noted as still necessary for some analyses.
  - Languages and translation: Translation was required for certain concepts (e.g., livestock illness signs); some responses originally in local languages were translated; translators acknowledged.

- Sampling coverage and key statistics
  - Census in 2012 recorded 3,717 households; 51.2% owned livestock and/or dogs; 1.1% owned only chickens; 47.7% had no animals.
  - Target sample sized to support trypanosomiasis prevalence estimation, with additional socio-economic augmentation to capture non-livestock households.
  - Data facilitate cross-cutting analyses across health, wealth, assets, agricultural practices, and wildlife contact, within the DD DAC framework.

- Data access, provenance, and reuse
  - Data contributed to the Environmental Information Data Centre (EIDC) as part of the DDDAC project; accessible for research and policy-oriented work under the consortium’s governance.
  - Primary authors and contributors listed; acknowledgments note translation and fieldwork support.
  - Dataset is appropriate for data-led governance and decision-making in poverty alleviation, public health, veterinary services planning, and One Health analyses.

- Practical considerations for data leaders
  - Governance: Clear data lineage from field collection to anonymised CSV ready for ingestion; metadata and coding schemes documented to enable reproducibility.
  - Privacy: Personal identifiers removed; GPS data anonymised; household identifiers retained for longitudinal or cross-dataset linkage within governance constraints.
  - Data quality and usability: Offline-first data capture with daily synchronization; subsequent cleaning and recoding require careful metadata-aware handling; cross-domain integration possible (health, livestock, environment, migration).
  - Reuse potential: Can inform data-system design for cross-sector datasets (health policy, veterinary services planning, environmental and poverty analytics) and support co-ownership of data products with policy colleagues and partners.