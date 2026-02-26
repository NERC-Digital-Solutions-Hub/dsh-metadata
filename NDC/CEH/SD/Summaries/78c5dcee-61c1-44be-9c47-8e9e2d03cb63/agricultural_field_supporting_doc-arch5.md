# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

## Overview
- Dataset describes 259 smallholder agricultural field surveys from 26 villages across three districts in Mozambique: Mabalane (Gaza Province), Marrupa (Niassa Province), and Gurue (Zambezia Province).
- Data collection timeframe: Mabalane May–Sept 2014; Marrupa May–Aug 2015; Gurue Sep–Dec 2015.
- Collected as part of the ESPA-funded ACES project, aiming to understand how land use changes affect ecosystem services and rural livelihoods.
- Purpose: capture current and historical field management practices and linked soil data to assess soil fertility and nutrient status changes over time (soil data not included here).

## Data collection and scope
- Methods: structured interviews with field owners to gather information on management practices (inputs, tilling, fire and residue management), field age, crops, yields, fallow cycles, floods, erosion, pests, and wild animal problems; qualitative field observations recorded.
- Field and village selection: 26 villages chosen to represent a gradient of land-use intensity; within each village, 10 active fields were surveyed (excluding fallow fields). Village and field selection relied on local guides’ knowledge.
- Fieldwork practices: owners identified and consent obtained; field location mapped with GPS; field area measured; interviews conducted in the local language and translated into Portuguese, then into English by the lead author.
- Equipment: Garmin GPS devices for location; Android tablets with Open Data Kit (ODK) for data collection.
- Data lineage: methodologies co-developed by ACES researchers; all data quality assured by the lead author; translations and data processing performed by the lead author.

## Data structure and content
- The dataset comprises 12 spreadsheets that link via a common field_id:
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
- Key features:
  - field_main_survey: core interview responses (date, location, field area, etc.); district-specific questions may vary; presence/absence of items indicated per district.
  - crops_planted: crops normally planted; crops planted in the previous year and in the first year (district-dependent).
  - crop_yield: quantitative yields for the most recent harvest; some crops recorded as counts (individuals) when needed; unit conversions provided in a separate sheet.
  - yield_unit_conversion: conversion factors and uncertainties to translate local harvest units to kilograms; notes emphasize high uncertainty.
  - fertiliser_use, pesticide_use, field_tilling: management practices and frequencies; pesticide data collected only in Gurue.
  - insect_pest, animal_pest: pests and their qualitative frequency per field.
  - trees_on_field, trees_before_cleared, indicator_species: tree/grass species observed on or before field creation; indicator species for soil quality; species names primarily in local nomenclature.
- Data semantics:
  - Each dataset includes a field_id linking to the 259 fields; blanks indicate not recorded or unknown; -999 indicates unknown quantities.
  - Some fields lack data in certain datasets; not all datasets cover all 259 fields.

## Data quality, provenance, and governance
- Quality control: lead author conducted all quality assurance; field interviewers trained prior to data collection; in-field translations ensured; pre-coded responses used where possible to reduce ambiguity.
- Provenance and transparency: methodological notes describe district differences and the questions asked; soil samples collected but not included in this dataset; crop yield data rely on recall for older years and are treated as rough estimates.
- Limits of data:
  - Recall-based yield data and uncertain unit conversions introduce substantial uncertainty; use yield data with caution.
  - District-specific questionnaire differences may affect comparability across sites.
  - Soil data are not included here, though soil fertility was a focus of the original study.

## Usage, context, and supporting information
- Potential uses: analyses of land-use intensification, cropping systems, input use, and smallholder livelihoods; linking field management practices to soil fertility trends through the accompanying soil data (not included here); supports ecosystem services and poverty-related research within Mozambique.
- Metadata and references:
  - Related datasets include tree identification data submitted to the EIDC.
  - Key references: ACES project details; ESPA programme funding sources (DFID, ESRC, NERC); MINAG 2008 national agricultural survey; related publications on charcoal, soil fertility, and land-use impacts.

## Limitations and cautions for data stewards
- Data gaps: soil data not included in this release; some datasets incompletely cover all fields.
- Data heterogeneity: differences in questionnaires by district require careful harmonization for cross-site analyses.
- Uncertainty: unit conversions for yields are highly uncertain; treat as rough estimates and clearly document assumptions.
- Data quality considerations: reliance on local names for crops and pests; some species identifications are handled separately (tree identification dataset) and not fully embedded here.
- Consent and ethics: surveys conducted with consent; data management should maintain appropriate attribution and privacy considerations aligned with the project’s governance framework.

## References and related materials
- ESPA ACES project: NE/K010395/1; funded under ESPA by DFID, ESRC, and NERC.
- Related datasets and publications cited in the documentation (charcoal production, soil and land-use impacts, and Mozambique rural livelihoods), and the tree identification dataset submitted to the EIDC.