# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

## Overview
- Dataset describing 259 field surveys from 26 villages across three districts in Mozambique (Mabalane, Marrupa, Gurue).
- Collected 2014–2015 to understand current and historical management practices and their potential effects on soil carbon and nitrogen, alongside broader patterns of land use and farming practices.
- Part of the ESPA-funded ACES project, linking agricultural practices to ecosystem services and rural wellbeing.

## Study design and scope
- Villages selected to represent a gradient of land-use intensity within each district.
- Districts and village counts: Mabalane (6 villages), Marrupa (10), Gurue (10); total 26 villages.
- Field selection: 10 active fields per village (no fallow fields at the time of sampling); fields within village limits with known ownership.
- Field mapping: location and perimeter recorded with GPS to delineate fields.
- Temporal coverage: Mabalane surveys May–September 2014; Marrupa May–August 2015; Gurue September–December 2015.
- Data collected included management practices, field age, crops, yields, fallow cycles, erosion, pests, and qualitative field observations (trees, cropping systems).

## Data collection methods and instrumentation
- Interview approach: structured questionnaires conducted in the local language, translated into Portuguese, then into English by the lead author.
- Data capture: paper forms or Android tablets using Open Data Kit (ODK).
- Field measurements: GPS for field perimeters; location coordinates and area; altitude captured where available.
- Data quality: all questionnaires pre-coded where possible to standardise responses; observers trained; translations checked by lead author.

## Data structure and datasets (12 spreadsheets)
- field_main_survey: main interview responses, field location, area, interview date, and related metadata.
- crops_planted: crops normally planted in each field; crops planted in last year; crops planted in the first year.
- crop_yield: quantitative yields for the most recent harvest by crop; notes on recording (most recent harvest due to recall issues).
- yield_unit_conversion: unit conversions for yields (kg_raw and kg_transformed), sources, uncertainties, and notes.
- fertiliser_use: types of fertilisers used, frequency, and extent of application.
- pesticide_use: pesticide use and frequency (collected only in Gurue).
- field_tilling: tilling methods and frequency.
- insect_pest: insects reported as crop pests and their frequency.
- animal_pest: animals raiding crops and their frequency.
- trees_on_field: live trees observed on the field at interview time.
- trees_before_cleared: tree species present before field creation (only in Mabalane).
- indicator_species: indicator trees/grasses used by farmers to gauge soil quality, including whether indicator is a tree or grass; species name data captured separately with limitations on grass identification.

- Key linkage: each dataset includes field_id to join records across datasets; field_id encodes village and field number.

## Data content and measurement notes
- Field identifier and metadata
  - field_id: unique id; first three letters = village, last digits = field number.
  - location_x, location_y: geographic coordinates; geo_ref specifies coordinate system.
  - area_ha: field area in hectares; altitude recorded when available.
  - date_sampled: interview date.
  - year_created, year of ownership, and various year-related fields capture field history and changes.
- Survey content and variation by district
  - Question sets vary by district; presence/absence indicators show which district collected which question.
  - Some questions are district-specific (e.g., certain tilling, pest, or pesticide questions).
- Data specifics per dataset
  - field_main_survey: captures interview details, field characteristics, management practices, and qualitative observations (e.g., impact of floods, erosion, fallow periods).
  - crops_planted: lists crops normally planted and those planted in last year or first year; local crop names used when translations were not available.
  - crop_yield: quantitative yields for the most recent harvest; units may be in local terms or “individuals”; where possible, conversion to kg via yield_unit_conversion.
  - yield_unit_conversion: documents units, conversion factors, sources (local measurements, MINAG 2008, literature), and notes on uncertainties.
  - fertiliser_use and pesticide_use: types and frequency; fertiliser_area indicates whether application was field-wide or partial (data available for Gurue and/or Marrupa/Mabalane where applicable).
  - field_tilling: tilling type (hoe, ox plow, tractor) and frequency.
  - insect_pest and animal_pest: lists of pests and qualitative frequency of impact.
  - trees_on_field and trees_before_cleared: observed tree species on site now and prior to clearing (where collected); tree species identification done separately.
  - indicator_species: local indicator species for soil quality, with distinction between trees and grasses; grass identification limited.
- Data quality notes
  - All data quality assured by lead author; field interviewers trained; translations from local languages to Portuguese and then English performed by lead author.
  - Quantitative yield data are recall-based and conversions are uncertain; figures should be treated as rough estimates.
  - Some fields may have missing data; blanks indicate not recorded, unknown, or not relevant; -999 marks unknown quantities or years.
  - Soil samples were collected but not included in this dataset; historical soil data not present here.

## Limitations and cautions
- Long recall period and unit conversion uncertainties affect yield and input estimates; use yield data with caution.
- Differences in questionnaires across districts may affect comparability; refer to district-specific notes in the main dataset.
- Soil data exist but are not included; cross-analysis with soil fertility requires external datasets.
- Not all datasets cover all 259 fields; missing records should be treated as not recorded for those fields.

## Provenance and context
- Data collected as part of the ACES project under ESPA, focused on how land-use changes influence ecosystem services and rural livelihoods.
- Methodologies co-developed with ACES researchers; local knowledge and field guides played a central role in field selection and data collection.
- References provided for related work on charcoal production, land-use intensity, and Mozambican agriculture and soils.