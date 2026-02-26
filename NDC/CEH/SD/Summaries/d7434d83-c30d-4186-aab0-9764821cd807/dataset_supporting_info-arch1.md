Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

## Overview
- Transdisciplinary dataset from 10 smallholder farming villages in Patarasi Rural Municipality, Jumla District, Nepal, collected during 2021–2022.
- Integrates ecological, dietary, and socio-economic data to address:
  - diets, nutritional status, and socioeconomic status
  - crops and their nutrient contributions and farming practices
  - insect pollinators and their interactions with crops
  - potential climate-change impacts on the system
- Key participant and household counts:
  - 776 participants from 200 households in 10 villages (dietary recalls, anthropometry, household/farmer data)
  - 11,107 plant–pollinator interactions across 10 villages
  - 1,928 pollen specimens analyzed from insect visitors
  - 116 beekeepers surveyed
  - 200 household cooks and other household informants
- Data collected and stored using CommCare on smartphones; anonymised and cleaned for analysis
- Funders and coordination: Micro-Poll Project (Pollination of Nepal’s Micronutrient-rich Crops in a Changing Climate); Natural Environment Research Council (NERC), National Science Foundation (NSF), Academy of Finland; coordinated through Belmont Forum and Bristol Centre for Agricultural Innovation

## Datasets and what they cover
- Plant-pollinator interactions
  - 11,107 interactions recorded in 10 study villages (Apr 18 – Nov 4, 2021)
  - 3 habitat types per village with 9 plots per village; 40-minute visitation surveys every two weeks
  - Data includes plant species, pollinator species, site, plot, time, and interaction details
  - Structure: plant_pollinator_interactions_all_data.csv and plant_pollinator_interactions_metadata.csv
- Flower density data
  - Flower density measurements for crop and non-crop species (Apr 18 – Nov 4, 2021)
  - Quadrats (15 per plot) with 4-point abundance scale; additional spot checks for unobserved flowering plants
  - Summary levels: plot, habitat, village
  - Structure: metadata, all_flower_data, plot_level, habitat_level, village_level CSVs
- Pollen analysis data
  - Pollen counts from 1,928 insect specimens (subset of pollinators from the plant-pollinator dataset)
  - Pollen identified to crop-specific categories (pumpkin, apple, bean, slipper gourd) and other pollen
  - Structure: metadata, all_data, and genus/family/order-level summary sheets
- Farmer questionnaire data
  - Lead farmer responses from 200 households (land ownership, farming practices, crops, climate awareness, etc.)
  - Structure: metadata and all_data
- Field experiment data
  - Pollinator exclusion experiment across 4 crops (apple, beans, pumpkin, slipper gourd) at 15 sites
  - Treatments: open pollination, pollinator exclusion, hand pollination; yields recorded per plant/branch/node
  - Insect visitation data per crop/site
  - Structure: metadata, site_info, insect_visitation, and crop-specific yield data (apple, karela, bean, pumpkin)
- Beekeeper questionnaire data
  - 116 beekeepers across 10 villages; honey yield, hives per beekeeper, perceived drivers of change
  - Structure: metadata, codes_questions, all_data, honey_yield_change, beehive_change
- Household census data
  - Demographic census to develop sampling frame; comprises households and individual members
  - Structure: metadata, household_csv, individuals_csv
- 24-hour dietary recall data
  - 12-month fortnightly dietary recalls for 721 individuals from 200 households (Nov 2021 – Dec 2022)
  - Detailed intake data at ingredient level per recall event
  - Structure: metadata and all_data
- Anthropometry data
  - Monthly anthropometric measurements for 721 participants (weight, height, age, sex, oedema)
  - Structure: metadata and all_data
- Participant information data
  - Enrollment details for households and individuals (de-identified)
  - Structure: hh_enrolment_metadata, hh_enrolment_all_data, participant_enrolment_metadata, participant_enrolment_all_data
- Cook questionnaire data
  - Interviews with main cooks of 200 households (cooking methods, fuel, food security, eating habits)
  - Structure: cook_questionnaire_metadata and cook_questionnaire_all_data

## Data collection and quality assurance
- Methods and tools
  - Data collected in the field by 20+ full-time staff; smartphone data entry via CommCare v2.48.3
  - Field workflows included regular monitoring and site visits
  - Pollen and plant identifications validated by taxonomists (Nepal National Herbarium; Tribhuvan University; Bengaluru experts)
  - Anthropometry followed WHO guidelines using standardized equipment
- Data handling and privacy
  - Personal identifiers removed; datasets anonymised where applicable
  - Data merged, cleaned, and, where relevant, merged to aid analysis
- Documentation and structure
  - Each dataset includes a dedicated metadata sheet describing columns and coded values
  - Data files organized to support various scales of analysis (plot, habitat, village, site, crop, etc.)

## Units, scope, and structure highlights
- Each dataset is built around well-defined units, enabling cross-dataset linkage:
  - Interactions: plant–pollinator events
  - Flower density: flowering abundance per plant species per plot
  - Pollen: pollen counts per insect specimen
  - Dietary recalls and anthropometry: individual-level, time-bound observations
  - Field experiments: treatment-level yields and visitation data
  - Household and participant data: household and individual-level while maintaining confidentiality
- Data structure typically includes a metadata file plus a main data file; some datasets also include multiple aggregation levels (species, genus, family, order)

## Potential analyses and use cases for Analysts
- Nutrition and health
  - Link dietary intake and anthropometric data to household socio-economic variables
  - Explore nutrient contributions of crops and dietary patterns across villages
- Agriculture and pollination
  - Correlate pollination services (plant-pollinator interactions, flower density, pollen loads) with crop yields under different pollination treatments
  - Assess impact of altitude and habitat on pollinator activity and crop production
- Climate change insights
  - Examine how flowering phenology, pollinator visitation, and crop yields respond along the altitudinal gradient
- Policy and program planning
  - Identify key crops and pollinator dependencies for micronutrient-rich diets in rural Nepal
  - Inform interventions targeting livelihoods, beekeeping, and crop diversification

## Considerations and caveats
- Data completeness and gaps
  - Some columns may be NA due to conditional questions or non-response; columns retained to preserve question structure
- Scale and access
  - Large, multi-dataset resource with potential data integration challenges across variable formats and scales
- Privacy and governance
  - De-identified data; researchers should follow project guidelines for data usage and citation
- Data quality and standardization
  - Despite rigorous QA, cross-dataset harmonization may require careful alignment of taxonomic identifications and unit definitions

## Provenance and access notes
- Data are part of the Micro-Poll Project and associated with multiple funders and collaborators
- Collected via a standardized data collection platform (CommCare) and anonymised by a data manager
- Dataset is organized into multiple CSVs with accompanying metadata to support interpretation and reuse