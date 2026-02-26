# Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

## Aim and scope
- Multi-faceted dataset designed to understand diets, nutritional status, crop production, plant-pollinator interactions, and the influence of climate change in rural Nepal.
- Integrates ecological, agricultural, and human health indicators to inform policy decisions and monitoring of environmental health and livelihoods.

## Datasets included (high-level overview)
- Plant-pollinator interactions
  - 11,107 interactions recorded across 10 study villages (April–November 2021).
  - Data on plant species, pollinator visitors, collection methodology, and specimen identifications.
  - Structure: two CSV sheets (data and metadata); each row an interaction.
- Flower density data
  - Flower abundance for crop and non-crop species across 10 villages (April–November 2021).
  - Multiple CSV sheets (metadata, raw data, plot-, habitat-, and village-level summaries).
  - Measured via quadrats and supplementary abundance scores.
- Pollen analysis
  - Pollen grain counts on 1,928 insect specimens linked to four target crops (pumpkin, apple, bean, slipper gourd) plus other visitors.
  - Files include data by species/genus/family/order and raw counts; quality control via pollen imagery and reference library.
- Farmer questionnaire data
  - Survey of 200 lead farmers across 10 villages.
  - Topics: land ownership, farming knowledge and income, practices, crops, pollination, climate adaptation, and production data for six pollinator-dependent crops.
- Field experiment data (pollination services along altitude)
  - Pollinator exclusion, open pollination, and hand pollination treatments on four crops (apple, beans, pumpkin, slipper gourd) across 15 sites (altitudinal gradient 2400–3100 m).
  - Includes insect visitation and crop yields by treatment; site information and per-crop yield datasets.
- Beekeeper questionnaire data
  - Survey of 116 beekeepers across 10 villages (Sept 2022).
  - Topics: honeybee populations, honey yield, hive numbers, perceived drivers of changes, livelihoods impacts.
- Household census data
  - Demographic census for 10 villages to establish sampling frame.
  - Includes household-level and individual-level data (household heads and members).
- 24-hour dietary recall data
  - 12-month fortnightly recalls for 721 participants from 200 households (Nov 2021–Dec 2022).
  - Detailed intake of every food ingredient per recall event.
- Anthropometry data
  - Monthly anthropometric measurements for 721 individuals (Nov 2021–Dec 2022) following WHO guidelines.
  - Includes age, sex, height, weight, oedema; adult heights captured at baseline.
- Participant information data
  - Enrollment data for households and individuals from the dietary/anthropometry components.
  - Separate household and participant enrollment metadata and records.
- Cook questionnaire data
  - Dietary/cooking habits questionnaire for the main cooks of 200 households.
  - Information on cooking methods, stove/fuel, food security, eating habits, and access.

## Population, sampling, and context
- Geography: Patarasi Rural Municipality, Jumla District, Nepal; 10 smallholder farming villages.
- Temporal span: 2021–2022 with multiple biweekly/monthly data collection points.
- Populations covered: households and individuals participating in dietary recalls, anthropometry, beekeeping, farming practices, and field experiments; beekeepers and cooks as key informants.

## Methods and quality assurance
- Data collection tools: CommCare-based smartphone app; data uploaded to secure servers; anonymisation applied where relevant.
- Training and standardisation: extensive training for nutrition and anthropometry data collection; standard protocols followed; regular monitoring and supervision.
- Biological and ecological data: expert identifications for plants and pollinators; photographic references for pollen; regular field monitoring visits.
- Data governance: data anonymisation, careful handling of personally identifiable information; openness and data sharing processes considered in governance plans.
- Data structure and metadata: each dataset provides a dedicated metadata sheet describing variables and column headers; main data sheets capture the relevant observations or measurements.

## Indicators and potential monitoring uses
- Nutritional indicators: dietary intake (24-hour recalls), nutrient density, and anthropometric trends to monitor community nutrition and vulnerability.
- Food system indicators: household food security, crop diversity, and pollinator-dependent crop production yields under different pollination scenarios.
- Ecological indicators: plant-pollinator interaction networks, flower density and phenology, pollinator visitation rates, and pollen loads on insects.
- Agricultural resilience indicators: field experiment results showing the relative contributions of open vs. excluded vs. hand pollination to crop yields along an altitude gradient.
- Livelihood indicators: beekeeping activity (hives per beekeeper), honey yield changes, and socio-economic factors from farmer questionnaires.
- Demographic indicators: household composition, enrolment status, and participant characteristics informing sampling frames and equity analyses.
- Climate and adaptation indicators: farmers’ climate adaptation practices and perceptions, in relation to ecological and agricultural outcomes.

## Data structure and access notes
- Multiple datasets are organized as ZIP-like collections with:
  - A metadata CSV describing each dataset and its columns.
  - A main data CSV containing observations.
  - Additional summarised sheets (e.g., at plot, habitat, village levels for ecological data; species/genus/family/order aggregations for pollen data).
- Datasets are anonymised where appropriate; some datasets include NA-filled columns to preserve question options and survey structure.

## Limitations and considerations for monitoring use
- Some columns contain NA values due to conditional questioning; metadata explains intent but users should interpret with caution.
- Data governance constraints may affect full public sharing; transparency and data sharing plans are addressed but may require appropriate approvals.
- Complex, multi-source nature of the data requires careful integration when constructing composite indicators (ecology–nutrition–socio-economics).

## Data lineage and provenance
- Project: Micro-Poll Project (The Pollination of Nepal's Micronutrient-rich Crops in a Changing Climate).
- Funded by: Natural Environment Research Council (NERC), NSF, Academy of Finland; coordinated through Belmont Forum Climate, Environment and Health Collaborative Research Action; additional funding from Bristol Centre for Agricultural Innovation.
- Data collection and management: field staff and data managers; smartphone-based data collection; anonymisation and cleaning prior to analysis.

## Summary for monitoring framework authors
- This resource provides a comprehensive, longitudinal, multi-domain dataset linking ecological processes (pollination, flowering, pollinator activity) with agricultural outputs (crop yields, field experiments) and human health/nutrition (diet, anthropometry, household demographics, and livelihoods).
- The integrated structure supports development of indicators that connect environmental health with nutrition and livelihoods, enabling policy-relevant monitoring across biophysical, agricultural, and socio-economic dimensions.
- Key strengths for monitoring design:
  - Longitudinal, biweekly to monthly data across a defined rural landscape.
  - Rich ecological data (interactions, densities, pollen loads) paired with human health and economic indicators.
  - Standardised quality control, metadata-rich datasets, and anonymisation practices.
- Primary considerations:
  - Harmonising disparate data types and scales (individual-level dietary data vs. plot-level ecological measures).
  - Navigating data gaps and NA columns due to conditional questions.
  - Ensuring governance and data-sharing arrangements align with open-data or restricted-access policies as appropriate.