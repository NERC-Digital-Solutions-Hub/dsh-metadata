# Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

## Overview
- Transdisciplinary data collection across 10 smallholder farming villages in Patarasi Rural Municipality, Jumla District, Nepal, conducted in 2021–2022.
- Aims to illuminate diets, nutritional status, socioeconomic conditions, crop production, pollination networks, flowering phenology, and potential climate-change impacts on the system.
- Participants include 776 individuals from 200 households for dietary, anthropometric, and household-level data; plus extensive ecological and agricultural datasets.
- Data gathered via a custom CommCare data collection platform on smartphones; anonymised where relevant and stored on a secure private server.
- Some columns contain NA values due to skip logic or conditional questioning; such columns are retained to preserve the full set of potential questions.

## Datasets and contents
- Plant-pollinator interactions
  - 11,107 plant–insect pollinator interactions collected across 10 villages (Apr–Nov 2021).
  - 2 CSV files: plant_pollinator_interactions_all_data.csv and plant_pollinator_interactions_metadata.csv.
  - Each row represents a single plant–insect interaction with details (host plant, insect, time, location, etc.).
- Flower density data
  - Flower density measurements for crop and non-crop species across 10 villages (Apr–Nov 2021).
  - 5 CSV sheets plus metadata: metadata, all_flower_data, plot_level, habitat_level, village_level.
  - Units are individual flowering plant species per survey plot; abundance scored on standardized scales.
- Pollen analysis data
  - Pollen grains collected from 1,928 insect specimens; counts for pumpkin, apple, bean, slipper gourd pollen (and others) with taxonomic resolution.
  - 6 CSV sheets plus metadata: pollen_analysis_all_data, pollen_analysis_species, pollen_analysis_genus, pollen_analysis_family, pollen_analysis_order, pollen_analysis_metadata.
- Farmer questionnaire data
  - Lead farmer responses from 200 households on land ownership, farming practices, income, crops, climate adaptation, and pollination-related questions.
  - 2 sheets: metadata and all_data.
- Field experiment data
  - Pollinator exclusion field experiment across four crops (apple, beans, pumpkin, slipper gourd) with three treatments (open pollination, exclusion, hand pollination) at 15 sites along an altitude gradient.
  - Datasets include site_info, insect visitation, and crop-specific yield data (apple, bean, karela, pumpkin).
  - 7 CSV sheets: metadata, site_info, insect_visitation, and crop yield data for the four crops.
- Beekeeper questionnaire data
  - 116 beekeepers from 10 villages; questions cover honeybee status, hive numbers, honey yield, and perceived drivers of changes.
  - 5 CSV sheets: metadata, codes_questions, all_data, honey_yield_change, beehive_change.
- Household census data
  - Demographic census to establish sampling frame (households and members) for 10 villages.
  - 3 CSV sheets: metadata, household_HH, household_indiv.
- 24-hour dietary recall data
  - Fortnightly dietary recalls over 12 months for 721 individuals from 200 households (18/11/2021–17/12/2022).
  - 2 CSV sheets: metadata and all_data (very large file, ~792 MB).
- Anthropometry data
  - Monthly anthropometric measurements (age, sex, height, weight, oedema) for 721 individuals from 200 households (12–13 months period).
  - 2 CSV sheets: metadata and all_data.
- Participant information data
  - De-identified participant and household enrollment data; links to dietary and anthropometric data.
  - 4 CSV sheets: hh_enrolment_metadata, hh_enrolment_all_data, participant_enrolment_metadata, participant_enrolment_all_data.
- Cook questionnaire data
  - Household cook responses on cooking practices, fuel, food security, and eating habits.
  - 2 CSV sheets: cook_questionnaire_metadata and cook_questionnaire_all_data.

## Data collection, provenance, and storage
- Collected by a team of field staff using CommCare Version 2.48.3 on smartphones; data uploaded to a secure private server.
- Anonymisation: person-identifiable information removed where relevant by a data manager.
- Datasets were processed (merged/summarised) to aid analysis and interpretation.
- Data lineage links to the Micro-Poll Project and its funding sources; dataset organized with structured metadata per dataset.

## Metadata, file structure, and governance
- Each dataset includes a metadata CSV describing column headers and the meaning of fields, plus one or more data CSVs.
- Data structure is documented for cross-dataset linkage (e.g., household and participant identifiers).
- Metadata and codebooks facilitate interpretation, serialization, and reuse.
- Data governance practices include anonymisation and adherence to ethical standards; data were stored securely to support controlled sharing and updates.

## Quality control and validation
- Plant and insect identifications reviewed by experts (botanists and taxonomists); pollen grain verification against reference images.
- Regular monitoring visits and in-field QC checks across datasets (survey quality, outliers, and data consistency).
- Anthropometry and dietary data collected under WHO-guided protocols with standardized equipment and procedures; training and standardization exercises conducted prior to data collection.
- For dietary recalls and household enrollment, manual checks and cross-verification with field supervisors were performed.

## Limitations and caveats
- NA values may arise from conditional questions or zero responses; columns retained to preserve question options.
- Large-memory dietary data (24-hour recalls) may present handling challenges due to file size.
- Interoperability across diverse datasets may require careful alignment of identifiers and timeframes.
- Some datasets involve localized plant and insect identifications that depend on regional taxonomies and reference libraries.

## Provenance and funding
- Funded by Natural Environment Research Council (NERC NE/T013621/1), National Science Foundation (NSF), and Academy of Finland; coordinated through the Belmont Forum Climate, Environment and Health Collaborative Research Action; additional support from Bristol Centre for Agricultural Innovation.
- Data collection and dissemination reflect a collaborative, cross-disciplinary effort aimed at informing policy and practice in rural Nepal.