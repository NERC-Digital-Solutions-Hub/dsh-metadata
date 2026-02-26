# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

- A dataset documenting 259 smallholder agricultural field surveys across 26 villages in three Mozambican districts: Mabalane (Gaza Province), Marrupa (Niassa Province), and Gurue (Zambezia Province).
- Data collection occurred in three periods: Mabalane (May–Sep 2014), Marrupa (May–Aug 2015), Gurue (Sep–Dec 2015).
- Purpose: capture current and historical management practices affecting soil fertility (carbon and nitrogen), land use, and ecosystem services; field data linked with soil data (not included here).

Spatial data and geography

- Field locations and perimeters measured with Garmin GPS devices (etrex 10 and 30); field boundaries delineated with local guides.
- Spatial attributes include:
  - Field location coordinates (location_x, location_y) and altitude.
  - geo_ref (geographic coordinate system reference).
  - field_id encodes village and field number (e.g., first three letters = village, last digits = field number).
- Field-level data are structured to support map-based analyses and spatial joins.

Data collection, structure, and instrumentation

- Village selection: 26 villages chosen to represent a gradient of land-use intensity across districts.
- Field selection: ten active fields per village, selected to vary by age and ownership; fallow fields excluded from sampling.
- Data collection methods:
  - Structured interviews with field owners conducted in local language and translated into Portuguese, then English.
  - Field location and area captured via GPS; field area recorded in hectares.
  - Field observations documented (cropping system, tree/bush presence, erosion, floods, pests, etc.).
  - Data captured on paper forms or Android tablets using Open Data Kit (ODK).
- Instrumentation:
  - GPS: Garmin etrex 10/30.
  - Data collection: Android tablets with ODK.

Dataset structure and linkages

- The dataset comprises 12 spreadsheets, all linked by a common field_id:
  1. field_main_survey
  2. crops_planted
  3. crop_yield
  4. yield_unit_conversion
  5. fertiliser_use
  6. pesticide_use
  7. field_tilling
  8. insect_pest
  9. animal_pest
  10. trees_on_field
  11. trees_before_cleared
  12. indicator_species
- Key content by dataset:
  - field_main_survey: core interview responses (date, location, area, field type, ownership, etc.).
  - crops_planted: crops normally planted per field and crops planted in prior years (where available).
  - crop_yield: quantitative yields from the most recent harvest; other historical yield data excluded due to recall unreliability.
  - yield_unit_conversion: how local harvest units are converted to kilograms with sources and uncertainties.
  - fertiliser_use and pesticide_use: types, frequency, and extent of fertiliser/pesticide use (pesticide data limited to Gurue).
  - field_tilling: tilling methods and frequency.
  - insect_pest and animal_pest: pests affecting crops and their frequency.
  - trees_on_field and trees_before_cleared: live trees on fields at sampling and trees present before field creation (separate species identification dataset exists).
  - indicator_species: tree/grass species used as indicators of soil quality.
- Data quality and uncertainties:
  - Some fields and datasets are incomplete; blanks indicate missing or unknown data; -999 denotes unknown quantities.
  - Local units and recall-based yields require caution; unit conversions are uncertain and based on local measures, national data, and literature.

Data quality, limitations, and notes

- All data were quality assured by the lead author; field interviewers were trained; translations standardized where possible.
- Quantitative crop yields rely on recall and local units; unit conversions are highly uncertain and should be treated as rough estimates.
- Soil samples were collected but are not included in this dataset.
- Some questions differed by district; presence/absence columns indicate where a question applied.
- Some datasets are not complete for all 259 fields; missing fields should be treated as not recorded.

How this dataset supports GIS work

- Enables creation of map-based data products showing:
  - Field boundaries, locations, and perimeters for spatial visualization.
  - Field-level attributes: cropping systems, yield estimates (converted via yield_unit_conversion), input use (fertilisers, pesticides), tillage practices, pests, trees, and soil quality indicators.
  - Spatial analysis of land-use intensity and its relation to management practices, erosion risk, and flood exposure.
- Data can be joined in GIS via field_id to produce layered maps (e.g., crops_planted, yields, vegetation indicators, and soil quality proxies) and to perform landscape-level analyses across districts.
- Provides a basis for assessing spatial patterns in farming practices and their potential effects on soil nutrients and ecosystem services, complementing soil data not included here.

Access notes and references

- Data are organized in 12 interconnected spreadsheets; field_id links across datasets.
- Referenced sources for context include ESPA ACES project, Mozambican agricultural surveys (MINAG 2008), and related studies on land-use and charcoal production in Mozambique.