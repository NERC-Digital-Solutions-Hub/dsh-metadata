# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

## Overview
- A dataset comprising 259 smallholder field surveys from 26 villages across three districts in Mozambique (Mabalane, Marrupa, Gurue) collected in 2014–2015.
- Aims to understand current and historical management practices affecting soil carbon and nitrogen, and to contextualize how land use and scarcity influence farming decisions.
- Data linked to soil fertility context (soil data collected but not included here) and designed to inform ecosystem services and rural wellbeing within the ESPA ACES project.

## Study design and sampling
- Villages selected to create a gradient of land-use intensity (e.g., charcoal production, subsistence agriculture, forest resource extraction, smallholder commercial agriculture).
- 26 villages included; within each, 10 active fields surveyed (no fallow fields), chosen with local guides to reflect field age and ownership.
- Fields located and field boundaries delineated using GPS; ownership confirmed with local guides; interviews conducted in local language.

## Data collection and instruments
- Structured interviews with field owners to capture management practices (inputs, tilling, fire and residue management), field age, crops, fallow cycles, floods, erosion, pests, and wild animals; qualitative field observations also recorded.
- Data collection tools: Android tablets and Open Data Kit (ODK); GPS for location; field area measured by perimeter mapping.
- Interview questions sometimes varied by district; translation chain: local language → Portuguese ( interviewer ) → English (lead author).
- Yields focused on the most recent harvest due to recall limitations; soil data not included in these datasets.

## Data structure and contents
- 12 interlinked spreadsheets (datasets) with a common field_id key:
  1) field_main_survey
  2) crops_planted
  3) crop_yield
  4) yield_unit_conversion
  5) fertiliser_use
  6) pesticide_use
  7) field_tilling
  8) insect_pest
  9) animal_pest
  10) trees_on_field
  11) trees_before_cleared
  12) indicator_species
- Each dataset records field-level observations or responses; some questions differ by district (presence/absence columns indicate district coverage).
- Data types include: field location (GPS), area (hectares), dates, crop names (local/English), yields, units, management practices, pests, trees, and soil indicator species.
- Data linkage via field_id; blanks indicate missing or unknown data; -999 indicates unknown quantities or years; some year fields prefixed with negative signs denote years before known events (e.g., before wars).

## Data quality and governance
- Quality control conducted by the lead author; field staff trained; ongoing checks during data collection.
- Data translated from local language to Portuguese, then to English by the lead author; pre-coded or binary responses used where possible to minimize ambiguity.
- Yields are recall-based and unit conversions carry high uncertainty; conversions rely on local measures, national data, and literature; users should treat yield estimates as rough approximations.
- Soil data are not included in these datasets, though soil fertility context was a stated aim of the broader project.

## Relevance for monitoring frameworks
- Provides multi-dimensional indicators relevant to environmental health monitoring and policy evaluation:
  - Land-use intensity and field age; cropping systems (intercropping, monocropping, subsistence, commercial, etc.).
  - Agricultural inputs (fertilisers, pesticides) and management (tilling, residue management, fire).
  - Soil- and land-related risks (erosion, floods, fallow periods, field expansion).
  - Biodiversity and soil quality indicators via indicator_species and trees_before_cleared / trees_on_field.
  - Pests (insects and animals) and their frequency, informing risk assessments.
- Robust data architecture for monitoring frameworks:
  - Consistent field_id linking across datasets enables integrated indicators and dashboards.
  - Use of GPS and digital data collection supports spatial-temporal monitoring and reproducibility.
  - Metadata conventions (units, missing values, district differences) facilitate data governance and transparent data use.
- Limitations to consider in monitoring use:
  - District-specific questionnaire variations may affect comparability; account for differing question sets.
  - Recall-based yield data and uncertain unit conversions require cautious interpretation.
  - Soil data not included; limits linkage to soil fertility trajectories unless integrated with external soil datasets.

## Access, reuse, and interpretation notes
- Data collected under the ESPA ACES project; subsequent data use should acknowledge project context and data provenance.
- The datasets are designed for integration, trend analysis, and policy evaluation, with explicit caveats on data uncertainty and district differences.
- When reusing, consider:
  - The time frame (2014–2015) and regional focus on three districts.
  - The 259 fields and 26 villages; geographic and livelihood diversity within the sample.
  - The absence of soil chemistry data in these spreadsheets; supplement with external soil datasets if soil trend analyses are required.
  - Coding conventions (e.g., -999 for unknown, blanks for not recorded) for accurate data cleaning.