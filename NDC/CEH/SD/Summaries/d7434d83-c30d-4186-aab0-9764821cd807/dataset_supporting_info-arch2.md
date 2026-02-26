# Ecological, dietary, and socio-economic data from 10 smallholder farming villages in Jumla District, Nepal, 2021-2022

## Overview
- A transdisciplinary, multi-dataset resource from Patarasi Rural Municipality, Jumla District, Nepal (2021–2022) covering ecological, dietary, and socio-economic dimensions.
- Includes data from 776 participants across 200 smallholder households and encompasses plant-pollinator networks, flowering phenology, pollen analysis, agricultural practices, beekeeping, household demographics, dietary intake, anthropometry, andCook/cooking practices.
- Data were collected to understand diets, nutrition, crop nutrient sources, pollination ecology, and potential climate-change impacts on rural agricultural systems.

## Datasets included
- Plant-pollinator interactions: 11,107 plant–insect pollinator interactions across 10 villages (Apr–Nov 2021). two CSVs: data and metadata.
- Flower density: flowering abundance data for crop and non-crop species, with multiple summary levels (plot, habitat, village) and metadata.
- Pollen analysis: pollen grains from 1,928 insect specimens across crops, with species- and higher-level summaries and metadata.
- Farmer questionnaire: responses from lead farmers (200 households) on land, practices, crops, climate awareness, and pollinator-dependent crops; metadata and all_data.
- Field experiment data: pollinator-exclusion experiment across 15 altitudinal sites (2400–3100 m) with three treatments and yields for four crops; site_info, insect visitation, and crop-specific yield datasets plus metadata.
- Beekeeper questionnaire: survey of 116 beekeepers focusing on honeybee status, yields, hive numbers, and perceived drivers; multiple sheets including codes/questions.
- Household census: village-level demographic census to create sampling frames; household and individual-level data with metadata.
- 24-hour dietary recall: 12-month dataset for 721 individuals from 200 households; detailed intake by ingredient per recall event; extensive metadata.
- Anthropometry: monthly anthropometric measurements for 721 individuals (age, sex, height, weight, edema) over a year; metadata and all_data.
- Participant information: enrolment data for households and individuals (two datasets with codebooks).
- Cook questionnaire: cooking practices, fuel use, food security, eating habits for 200 households; metadata and all_data.

## Data collection, methods, and quality assurance
- General approach: standardized, field-based data collection using CommCare on mobile devices; anonymisation prior to sharing.
- Plant-pollinator and flower-density data: systematic sampling within a defined 600 × 600 m study area; habitat stratification (village, crop, semi-natural); fixed survey plots; biweekly surveys; taxa identifications verified by botanists and entomologists; regular quality checks.
- Pollen analysis: targeted selection of insect specimens from main plant-pollinator interactions; pollen extraction, microscopy, and grain counting with reference images for accuracy.
- Dietary and anthropometric data: 24-hour recalls using a five-pass method; anthropometry following WHO guidelines; trained staff with security and QA processes; geo-location and follow-up tracking.
- Household and participant data: random selection of households from census-derived eligible list; lead farmer interviews; participant interviews conducted with consent; cross-checks for extreme values.
- Field experiments (pollinator exclusion): standardized crop plots along an altitude gradient; treatments include open pollination, pollinator exclusion, and hand pollination; replicated across sites; routine site monitoring and outlier checks.
- Beekeeping and cook data: in-person interviews in local language; structured formats; data validation through expert review.
- Data lineage and governance: anonymisation and data cleaning by HERD International; secure private server storage; datasets merged and summarized to aid interpretation where applicable.

## Data structure and file formats
- Each dataset includes a metadata file describing column headers and data meaning.
- Main data files typically appear as CSVs, with additional summary sheets (e.g., species-, genus-, family-, order-level pollen summaries; plot- and village-level flower data).
- Some datasets are large (e.g., 24-hour dietary recall) and include multiple linked files (metadata + raw data).
- Data are organized to support hierarchical analyses (plot, habitat, village, site) and cross-domain integration (ecology, nutrition, socio-economics).

## Data lineage and funding
- Collected under the Micro-Poll Project (Pollination of Nepal's Micronutrient-rich Crops in a Changing Climate).
- Funded by Natural Environment Research Council (NERC NE/T013621/1), National Science Foundation (NSF), and Academy of Finland (AKA); coordinated via Belmont Forum Climate, Environment and Health Collaborative Research Action; additional support from Bristol Centre for Agricultural Innovation.
- Data captured via a dedicated field team of about 20 staff; anonymised and cleaned before sharing.

## Access, usage, and metadata
- Data are accompanied by metadata and codebooks describing each variable.
- Some NA values exist due to conditional questions; columns with all-NA values are retained to preserve question options and survey structure.
- Datasets are designed for interoperability across ecological, nutritional, and socio-economic domains to support environmental monitoring and policy evaluation.

## Relevance for environmental monitoring and policy
- Enables assessment of environmental health and ecosystem services (pollination networks, flowering phenology, pollen dynamics) in rural agricultural systems.
- Supports monitoring of how climate change and land-use factors affect crop yields, pollination services, beekeeping livelihoods, and dietary/nutritional status.
- Facilitates data integration for understanding policy impacts on biodiversity, agriculture, and nutrition in mountainous rural contexts.
- Addresses challenges of data value and accessibility by providing standardized data products and rich metadata to enable re-use and cross-dataset analyses.

## Key considerations and limitations
- Some datasets include large NA portions due to conditional questioning; these are retained for transparency and to document potential survey pathways.
- Large data volumes (e.g., 24-hour recalls) require robust data management and processing for effective analysis.
- Cross-dataset linkage is feasible but requires careful alignment of household, village, and site identifiers across diverse data types.