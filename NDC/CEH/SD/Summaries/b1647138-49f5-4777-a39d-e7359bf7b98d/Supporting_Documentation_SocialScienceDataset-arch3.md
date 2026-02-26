# Economic and social science questionnaire dataset, Mambwe District, Zambia (2013)

- A dataset of 211 household surveys conducted in Mambwe District, Eastern Zambia, between June and August 2013 as part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC) research.
- Focuses on human and animal health within the context of household wellbeing, assets, and access to resources, integrating socio-economic, health, livestock, ecosystem, and migration information.
- Funded by NERC (NE/J000701/1) with support from ESPA; contributing to broader DDDAC research.

## Overview of aims and scope

- Aim: to identify environmental health measures for scrutinising and evaluating policy and informing future decisions.
- Topics covered:
  - Household demographics and welfare
  - Human and animal health, health service access and utilization
  - Livestock and dog demographics, production, and disease
  - Human–animal interactions, wildlife contact, and zoonoses
  - Water, sanitation, energy, and access to resources
  - Livelihoods, poverty indicators, assets, and resilience
  - Ecosystem changes, migration patterns, and agricultural practices (notably cotton)

## Data collection, sampling, and governance

- Sampling frame:
  - Built from a 2012 census of 3,717 households; households randomly selected to achieve adequate sub-samples for estimating trypanosomiasis prevalence (including 50% extra households with no animals).
  - Final sample: 211 households (some initially selected had no livestock/dogs).
- Data collection methods:
  - Semi-structured household interviews plus biological sampling of people and animals for disease indicators.
  - Questionnaire administered by a team of four interviewers; translations used where needed.
  - Tablet-based data capture (droidSURVEY), offline operation with daily internet uploads; data stored securely and anonymised before export.
- Consent and ethics:
  - Written consent obtained prior to interviews and blood sampling.
  - Anonymisation included removing respondent names, GPS coordinates, and interviewers’ names; household numbers retained.
- Data handling and dissemination:
  - Data cleaned, coded, and transformed in Excel; exported to CSV for ingestion by the Environmental Information Data Centre (EIDC).
  - Data governance and openness emphasised; metadata and underlying data shared appropriately.

## Dataset structure and key content

- File and structure:
  - CSV file: Socio-econ_Zambia_DDDAC_2017
  - Contains a broad set of variables spanning 13 thematic areas (sections below) with detailed coding schemes.
- Sectional coverage:
  - 1. Household information (e.g., household number, head demographics, composition)
  - 2. Education
  - 3. Health services and human health (health access, costs, satisfaction, training, mortality)
  - 4. Water and sanitation
  - 5. If livestock kept, veterinary services (availability, distance, drug access, sourcing, treatments)
  - 6. If yes, animal production (livestock ownership, purpose, births/deaths, management, feeding, diseases)
  - 7. Fauna/wildlife, tsetse flies, and contacts with them (wildlife seen, contact with wildlife, tsetse presence)
  - 8. Crop/vegetable production (vegetation change, cotton growing, field proximity, pesticides, harvest)
  - 9. Migration and livelihoods (immigration, reasons for moving, rains-driven migration)
  - 10. Economic status/poverty (farm area, maize storage, assets, energy use, savings, markets)
  - 11. Resilience (food security, malnutrition, community groups)
  - 12. Value setting (ownership of possessions, perceived value, coping capacity)
  - 13. Additional asset- and market-related indicators (varied asset ownership like mobile phones, vehicles, solar panels)
- Data detail examples:
  - Demographics: HH_head_sex, HH_head_age, adult/child counts, tribe
  - Health access: Health_Centre_access, Health_Centre_time, Health_Centre_cost, Health_Centre_satis, WTP_health_centre_better_ac cess
  - Animal and veterinary data: Vet_services_avail, Vet_distance_km, Vet_drugs_avail, Vet_drugs_source, animal counts by species, births/deaths, diseases, tick control
  - Environment and agriculture: Veget_change_last5yr, Cotton_grown_HH, Cotton_field_mins_fromHH, pesticides use, energy sources
  - Wildlife and disease: Wildlife_seen_regularly, Wildlife_contact_with_humans/animals, Tsetse_seen, Tsetse_direction_from_HH
  - Migration and markets: Immig_last10yrs, Reasons_immig, Livestock_market_compare_5yr, Crop_market_compare_5yr
- Data quality and coding:
  - Extensive internal coding for multi-response and grid questions
  - Anonymisation and data cleaning applied to ensure uniform variable coding
  - Some language-translation considerations acknowledged in data collection and interpretation

## Data governance, metadata, and accessibility

- Metadata and structure:
  - Detailed data dictionary available within the record, outlining variable names, questions, and coding schemes.
  - Clear anonymisation and data management practices documented (removal of identifiable data, retention of household identifiers for analytical linking).
- Data sharing and governance implications:
  - Data designed for ingestion into a central repository (EIDC) under the DDDAC framework.
  - Emphasizes data quality assurance, open/transparent sharing of underlying data where appropriate, and consistent data governance.
- Potential use in monitoring frameworks:
  - Multi-sector indicators suitable for One Health monitoring, linking human and animal health with livelihoods and environment.
  - Useful for evaluating policy interventions targeting disease drivers, health service access, livestock management, water/sanitation, and climate/vegetation changes.

## Relevance for monitoring environmental health frameworks

- Cross-cutting indicators:
  - Human and animal health outcomes, disease exposure, and treatment practices
  - Health service access, costs, satisfaction, and willingness to pay for improved services
  - Livestock management, production, ownership dynamics, and animal health risks (e.g., trypanosomiasis, tick-borne diseases)
  - Wildlife exposure, tsetse fly presence, and zoonotic risk pathways
  - Water quality, sanitation, energy sources, and household resilience
  - Crop production, cotton farming practices, pesticides usage, and market access
- Policy and decision support:
  - Enables monitoring of environmental health interventions, livestock interventions, and health system improvements
  - Supports assessment of community vulnerability and resilience to environmental and disease drivers
  - Provides a rich, auditable data source to inform dashboards and policy evaluations within environmental health monitoring frameworks

## Limitations and considerations for users

- Temporal scope:
  - Data collected in 2013; the dataset captures historical conditions and may not reflect current dynamics without updating.
- Data collection challenges:
  - Language and translation complexities; some questions rely on nuanced local concepts
  - One day of electricity outage during data collection affected tablet-based data capture
- Data processing:
  - Extensive data cleaning and recoding required due to grid-style and multi-response questions
  - Coding schemes are complex; researchers should refer to the accompanying data dictionary for accurate interpretation
- Generalizability:
  - District-level data with specific local contexts; extrapolation to other regions should be done with caution

## Authors, funding, and provenance

- Authors: Kathrin Schaten, Alexandra Shaw, Noreen Machila, Martin Simuunza, Emmanuel Chirwa, Neil Anderson, Ewan MacLeod, Susan Welburn
- Project context: Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC)
- Data provenance:
  - Linked to a broader research effort examining drivers of disease in Africa
  - Data collection and management aligned with ESPA and NERC support; data integrated into the Environmental Information Data Centre (EIDC) for sharing and reuse