# Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

## What this resource covers
- Transdisciplinary data from 10 farming villages in Patarasi Rural Municipality, Jumla District, Nepal, collected in 2021–2022.
- Human data: fortnightly 24-hour dietary recalls (721 participants from 200 households), monthly anthropometry for the same participants, plus household and participant enrolment information,Cook and farmer questionnaires, and household census data.
- Ecological data: plant–pollinator interaction networks (11,107 interactions), flower density measurements, flowering phenology, and a pollinator-exclusion field experiment across an altitudinal gradient.
- Integrated aims: understand diets, nutritional status, crop sources and cultivation, pollinator relationships, and potential climate-change impacts on the system.

## Datasets included (scope, content, and structure)
- Plant-pollinator interactions
  - 11,107 interactions recorded across 10 villages (Apr 18–Nov 4, 2021).
  - Files: plant_pollinator_interactions_all_data.csv; plant_pollinator_interactions_metadata.csv.
  - Data: one interaction per row; habitat categories include village, crop, and semi-natural areas; identification verified by specialists.

- Flower density data
  - Flower density of crop and non-crop species during Apr–Nov 2021.
  - Files: metadata; all_flower_data.csv; plot_level.csv; habitat_level.csv; village_level.csv.
  - Data: per plot per survey; 15 quadrats per plot with a 4-point abundance scale plus an auxiliary abundance score for undetected flowering plants.

- Pollen analysis data
  - Pollen grains from 1,928 insect specimens (subset from pollinator dataset) collected from 10 villages.
  - Files: pollen_analysis_metadata.csv; pollen_analysis_all_data.csv; pollen_analysis_order.csv; pollen_analysis_family.csv; pollen_analysis_genus.csv; pollen_analysis_species.csv.
  - Data: counts of pollen grains by pumpkin, apple, bean, slipper gourd and other pollen per insect specimen.

- Farmer questionnaire data
  - Lead farmer responses for 200 households covering land ownership, practices, crops, income, climate awareness, and pollinator-dependent crops.
  - Files: farmer_questionnaire_metadata.csv; farmer_questionnaire_all_data.csv.
  - Data: one row per household respondent.

- Field experiment data
  - Pollinator-exclusion experiment on four crops along an altitude gradient (2400–3100 m) across 15 sites; treatments: open pollination, pollinator exclusion, hand pollination.
  - Files: field_experiment_metadata.csv; field_experiment_site_info.csv; field_experiment_insect_visitation.csv; field_experiment_apple_data.csv; field_experiment_bean_data.csv; field_experiment_karela_data.csv; field_experiment_pumpkin_data.csv.
  - Data: yields by treatment/crop/site and insect visitation per crop/site.

- Beekeeper questionnaire data
  - Survey of 116 beekeepers across 10 villages; honey yield, hives, drivers of changes, and livelihoods.
  - Files: beekeeper_survey_metadata.csv; beekeeper_survey_codes_questions.csv; beekeeper_survey_all_data.csv; beekeeper_survey_honey_yield_change.csv; beekeeper_survey_beehive_change.csv.
  - Data: one row per beekeeper; additional sheets track historical yield and hive counts.

- Household census data
  - Demographic census to define sampling frame; data for 10 villages.
  - Files: household_census_metadata.csv; household_census_HH.csv; household_census_indiv.csv.
  - Data: household-level and individual-level records; anonymised.

- 24-hour dietary recall data
  - 12-month fortnightly dietary recall for 721 individuals from 200 households (18/11/2021–17/12/2022).
  - Files: 24hr_dietary_recall_metadata.csv; 24hr_dietary_recall_all_data.csv.
  - Data: per ingredient recalled per survey event; 1 row = ingredient, 1 survey event.

- Anthropometry data
  - Monthly anthropometric measurements for 721 participants (age, sex, height, weight, oedema) over a year.
  - Files: anthropometry_metadata.csv; anthropometry_all_data.csv.
  - Data: one row per participant per month; adult height measured at baseline.

- Participant information data
  - De-identified participant and household enrolment details linked to dietary/anthropometry data.
  - Files: hh_enrolment_metadata.csv; hh_enrolment_all_data.csv; participant_enrolment_metadata.csv; participant_enrolment_all_data.csv.
  - Data: one row per household or participant at enrolment.

- Cook questionnaire data
  - Household-level cooking practices, stove/fuel, food security, eating habits, and access.
  - Files: cook_questionnaire_metadata.csv; cook_questionnaire_all_data.csv.
  - Data: one row per household cook.

- Note on data quality
  - Some columns may be entirely NA due to conditional questions; columns retained to show possible questions and data collection design.

## Data collection, provenance, and stewardship
- Project: Micro-Poll Project (Pollination of Nepal's micronutrient-rich crops in a changing climate).
- Funding and coordination: Natural Environment Research Council (NERC), National Science Foundation (NSF), Academy of Finland; Belmont Forum collaboration; Bristol Centre for Agricultural Innovation.
- Data collection: field team of about 20; smartphone-based capture via CommCare v2.48.3; anonymisation by HERD International; data cleaning and merging performed as needed.
- Identification validation: plant identifications via Nepal's National Herbarium; insect identifications by Tribhuvan University and Bengaluru University experts.
- Quality control: regular field monitoring, staff training, outlier checks, geo-location tracking, and QA processes.

## Data structure and access notes
- Most datasets include a metadata sheet describing each column and dataset-specific context, plus a main data sheet (CSV). Some datasets include multiple summary levels (plot, habitat, village) or taxonomic summaries.
- Data are anonymised; sensitive personal information removed.
- Data are provided as CSV files (often zipped) for interoperability and reuse.

## Potential uses and cautions
- Opportunities:
  - Integrate diet, anthropometry, household socio-economics, farming practices, and crop data to study nutrition–agriculture linkages.
  - Ecological analyses of plant–pollinator networks, pollination services across altitudes, and effects of pollinator exclusion vs. hand pollination on yields.
  - Climate-change impact assessments on nutrition, agriculture, and biodiversity in rural Nepal.
- Cautions:
  - Manage missing data and NA columns due to conditional questioning.
  - Ensure proper linking across datasets using household, participant, plot, site, and crop identifiers.
  - Consider data privacy and anonymisation when sharing or publishing analyses.
- Data products to consider:
  - Self-serve dashboards by village/site showing dietary intake, anthropometry trends, and crop yields.
  - Interactive networks for plant–pollinator interactions and flowering density across habitats and altitude.
  - Policy-oriented summaries on nutrient sources, crop diversification, and beekeeping livelihoods.