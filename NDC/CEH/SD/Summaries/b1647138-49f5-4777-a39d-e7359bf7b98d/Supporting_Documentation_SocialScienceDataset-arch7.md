# Economic and social science questionnaire dataset, Mambwe District, Zambia (2013)

- Purpose: Document the results of 211 household surveys in Mambwe District, Eastern Zambia, as part of a broader study on human and animal trypanosomiasis, settlement patterns, and household wellbeing.
- Context: Part of the Dynamic Drivers of Disease in Africa Consortium (DDDAC); funded by NERC (NE/J000701/1) with ESPA support.
- Potential GIS relevance: Rich, map-ready indicators on household assets, livestock/dog holdings, water access, health service access, agriculture (including cotton), wildlife contact, tsetse exposure, migration, and vegetation change perceptions suitable for spatial visualization and spatially-informed analysis.

## What the dataset covers (scope and content)

- Household-level socio-economic and health data, including:
  - Demographics, assets, wealth/poverty indicators, resilience, food security, water and sanitation access.
  - Human and animal health access and outcomes, health facilities, and vaccination/deworming practices.
  - Livestock and dog demographics, production, ownership, births/deaths, disease, management, and marketing.
  - Wildlife interactions, tsetse fly encounters, and zoonoses knowledge.
  - Crop and vegetable production, including cotton cultivation, pesticides, field proximity, and market considerations.
  - Migration patterns, seasonal movements to fields, and health impacts.
  - Education, occupation, assets, energy use, and household infrastructure.
- Time span and geography: Data collected June–August 2013 from 211 households in Mambwe District; census-based sampling frame from August 2012 and Oct–Nov 2012 census data.
- Data linkage potential: Designed to support wider DDAC research; can be integrated with spatial datasets for district-level mapping and risk profiling.

## Data collection and lineage

- Sampling design:
  - Base: full census of people and animals (Aug 2012) to establish a sample frame; target minimum sample for trypanosomiasis prevalence.
  - Final sample: 211 households (144 with livestock/dogs; 67 without animals).
  - One-stage cluster survey with specified prevalence/precision assumptions; expanded by 50% to accommodate socio-economic aims.
- Data collection methods:
  - Household interviews and blood sampling from people and animals.
  - Tablet-based questionnaire using droidSURVEY; offline data capture with daily online uploads.
  - Data anonymised and securely stored before conversion to Excel and CSV for ingestion into the EIDC (Environmental Information Data Centre).
- Language and recording:
  - Predominant languages: Chikunda and Chichewa; translations conducted as needed.
  - Question formats include multiple choice, grids, and open-ended responses; data recoded into standardized variable formats.

## Data structure and format

- File: Socio-econ_Zambia_DDDAC_2017.csv
- Content organization:
  - Sections include: Introduction; Household information; Education; Health services and human health; Water and sanitation; If livestock present, veterinary services; Animal production; Fauna/wildlife; Crop/vegetable production; Migration; Economic status/poverty; Resilience; Value setting.
- Variable handling and coding:
  - Coding schemes include numeric, letter codes, and special placeholders:
    - Symbols for missing/applicable data: \ (not applicable), # (no answer)
  - Anonymisation details: removal of respondent names, GPS locations, and interviewers’ names; household numbers retained.
- Examples of data themes:
  - Household head demographics; adult and child counts; education levels.
  - Health service access: travel mode, travel time, costs, satisfaction, willingness to pay for better access; health/hygiene training; mortality within the last 12 months.
  - Livestock: ownership by species, births, deaths, offtake, ownership, management practices, tick control, vaccination, and veterinary access.
  - Wildlife and tsetse: regular wildlife sightings, contact with wildlife, tick/taiga exposure, tsetse fly sightings and timing.
  - Cotton and agriculture: field distances, pesticide use, company associations, farm assets, and crop management.
  - Migration and livelihoods: reasons for moving, rainy-season migration patterns, health effects.
  - Assets and energy: ownership of vehicles, radios, TVs, solar panels, and energy sources.

## Data quality, limitations, and processing notes

- Data quality considerations:
  - Language translation challenges and variability in disease naming due to local concepts.
  - Offline data collection with one day of electricity outage; data cleaned post-collection.
  - Anonymisation reduces locational precision; GPS data not provided to protect privacy.
- Data handling:
  - Extensive data cleaning to create distinct coding for open responses and to consolidate “other” responses into meaningful categories.
  - Data derived from self-reported responses and farm/livestock records; potential reporting biases to consider in GIS analyses.

## GIS-specific considerations and opportunities

- How to use in map-based analyses:
  - Spatial visualization of household wealth/assets and poverty indicators by location.
  - Mapping water access types, travel times to health facilities, and costs to identify service gaps.
  - Distribution maps for livestock/dog ownership by species, vaccination/de-worming coverage, and veterinary access.
  - Wild fauna exposure, tsetse fly encounter frequency, and seasonal patterns to inform disease risk mapping (with caveat on anonymized coordinates).
  - Crop production patterns (cotton cultivation) and pesticide usage linked to field proximity and market access.
  - Migration flows and seasonal field movements linked to livelihoods and health indicators.
- Geospatial data needs:
  - District-level shapefiles (Mambwe District) for aggregation and choropleth mapping.
  - Aggregation by ward or village where possible, given anonymization of precise GPS data.
  - Temporal dimension is limited to a single survey window (2013) in this dataset; cross-year comparisons would require additional data.
- Privacy and ethics:
  - GPS removal protects respondents; when spatial analysis is required, work with aggregated/obfuscated location data or request constrained access for higher-resolution analyses.
- Integration opportunities:
  - Can be joined with ecological layers (wildlife habitats, vegetation cover) and infrastructure datasets (health facilities, veterinary services, markets) for risk and resilience mapping.

## Access, attribution, and project context

- Data provenance: Economic and social science questionnaire dataset from the DDAC project, with authorship and acknowledgments listed in the source.
- Funding and affiliations: NERC grant NE/J000701/1; ESPA support; part of broader DDAC research network.
- Usage notes for GIS work:
  - Attribute-rich CSV suitable for joining with spatial layers.
  - Proper citation required when used in maps or analyses; acknowledge original DDAC study and funding sources.

- How this dataset supports GIS specialists:
  - Provides multi-dimensional socio-economic and agricultural indicators tied to a spatially referenced population (with privacy safeguards).
  - Enables development of map-based data products to communicate household resilience, health access, livestock/sustainability, and human–animal–environment interfaces in Mambwe District.