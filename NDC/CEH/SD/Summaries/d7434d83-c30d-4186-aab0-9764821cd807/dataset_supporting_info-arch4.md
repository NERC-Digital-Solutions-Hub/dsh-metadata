# Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

## Executive summary
- Transdisciplinary data from 10 villages in Jumla District ( Nepal ) collected in 2021–2022, covering human dietary intake, nutrition, socioeconomic status, farming and cooking practices, beekeeping, and ecological components (plant–pollinator interactions, flowering phenology, pollinator-exclusion field experiments).
- Enables integrated analyses of diets and nutrition, crop production, pollination services, and climate-change impacts, with data lineage,Quality control, and detailed metadata to support data discovery and re-use.

## Datasets included (high-level overview)
- Plant–pollinator interactions
  - plant_pollinator_interactions_all_data.csv and plant_pollinator_interactions_metadata.csv
  - 11,107 plant–insect pollinator interactions across 10 villages (Apr–Nov 2021)
  - Data collected via biweekly 40-minute surveys; insects captured and identified; plants identified; specimens deposited.
- Flower density
  - flower_density_metadata.csv, flower_density_all_flower_data.csv, flower_density_plot_level.csv, flower_density_habitat_level.csv, flower_density_village_level.csv
  - Flower density measurements (quadrats and abundance scales) across plots, habitats, villages (Apr–Nov 2021)
- Pollen analysis
  - pollen_analysis_metadata.csv, pollen_analysis_all_data.csv, pollen_analysis_order.csv, pollen_analysis_family.csv, pollen_analysis_genus.csv, pollen_analysis_species.csv
  - Pollen load data from 1,928 insect specimens (subset from plant_pollinator_interactions) focusing on pumpkin, apple, bean, slipper gourd; microscopy-based pollen identification.
- Farmer questionnaire
  - farmer_questionnaire_metadata.csv, farmer_questionnaire_all_data.csv
  - Baseline data from 200 lead farmers; land ownership, practices, income, crops, environmental/climate awareness, and production data for six pollinator-dependent crops.
- Field experiment
  - field_experiment_metadata.csv, field_experiment_site_info.csv, field_experiment_insect_visitation.csv, field_experiment_apple_data.csv, field_experiment_bean_data.csv, field_experiment_karela_data.csv, field_experiment_pumpkin_data.csv
  - Pollinator-exclusion field experiment (open pollination, exclusion, hand pollination) across 15 altitudinal sites; yields by treatment for four crops; insect visitation data.
- Beekeeper questionnaire
  - beekeeper_survey_metadata.csv, beekeeper_survey_codes_questions.csv, beekeeper_survey_all_data.csv, beekeeper_survey_beehive_change.csv, beekeeper_survey_honey_yield_change.csv
  - 116 beekeepers across 10 villages; honey yield, hive counts, perceived drivers of change.
- Household census
  - household_census_metadata.csv, household_census_HH.csv, household_census_indiv.csv
  - Village-level census for sampling frame; household heads and individual household members.
- 24-hour dietary recall
  - 24hr_dietary_recall_metadata.csv, 24hr_dietary_recall_all_data.csv
  - 12-month, fortnightly recalls for 721 individuals from 200 households; detailed ingredient-level intake data.
- Anthropometry
  - anthropometry_metadata.csv, anthropometry_all_data.csv
  - Monthly anthropometric measures (height, weight, age, sex, oedema) for 721 individuals.
- Participant and household enrolment
  - hh_enrolment_metadata.csv, hh_enrolment_all_data.csv, participant_enrolment_metadata.csv, participant_enrolment_all_data.csv
  - Baseline demographic and household characteristics; anonymised participant information.
- Cook questionnaire
  - cook_questionnaire_metadata.csv, cook_questionnaire_all_data.csv
  - Household cooking practices, fuel use, food security, eating habits.

## Data collection, processing, and lineage
- Field collection by a team of about 20 staff; smartphone data captured via CommCare v2.48.3 and uploaded to a secure private server.
- Anonymisation of person-identifiable information and data cleaning prior to analysis; datasets merged where relevant to support cross-domain analyses.
- Plant identifications validated by Nepal botanists; insect identifications by Nepali and Indian taxonomists; pollen grains validated against reference library.
- Data collection aligned with harmonized protocols (e.g., 40-minute pollinator surveys, 15-quadrat flower density assessments, 5-stage dietary recall method).

## Data structure and metadata
- Each dataset includes a metadata file describing column headers and data meaning.
- Main data files paired with summary-level or category-specific sheets (e.g., species-, genus-, family-, order-level pollen analyses; plot-, habitat-, village-level flower density).
- Data organized to support multi-scale analyses (individuals, households, plots, sites, villages).

## Quality control and standards
- Regular field monitoring, species identifications validated by experts, and consistency checks across datasets.
- Standardized data collection tools and predefined coding (e.g., 0–4 flower abundance scales; conditional questions yielding NA values preserved to reflect possible survey paths).
- Ethical safeguards: informed consent, anonymisation, and data handling conducted to protect participants.

## Use cases and relevance for data leaders
- Integrate nutrition, agriculture, ecology, and climate data to inform data strategy, policy briefs, and program design.
- Assess user needs across policy colleagues and researchers by mapping data flows, discoverability, and gaps (e.g., data at household and village levels, long-term ecological data, and crop yield under pollination treatments).
- Identify data gaps (e.g., granularity for certain variables, sector coordination) and opportunities for cross-sector collaboration and community of practice.
- Ensure robust data assets with clear provenance, lineage, metadata, discoverability, and plans for updates or extension studies.

## Limitations and notes
- Some columns contain NA values due to conditional questioning; the dataset retains these columns to preserve survey design and potential question paths.
- Large 12-month dietary recall dataset (792 MB) requires substantial storage and processing resources.
- Data represent a specific region and period (Patarasi Rural Municipality, Jumla District, 2021–2022) but offer rich cross-domain context for integrative analyses.

## Access and governance
- Data originated from the Micro-Poll Project and associated funders; anonymised and stored on secure infrastructure.
- Metadata-rich, designed to support discoverability and reuse by data professionals, researchers, and policy teams.