# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

- Overview
  - A dataset of 259 smallholder agricultural field surveys across 26 villages in Mozambique, spanning three districts: Mabalane (Gaza Province), Marrupa (Niassa Province), and Gurue (Zambezia Province).
  - Fieldwork conducted in 2014–2015 (Mabalane: May–Sep 2014; Marrupa: May–Aug 2015; Gurue: Sep–Dec 2015).
  - Collected as part of the ESPA-funded ACES project to understand how changing land use affects ecosystem services and rural livelihoods; primarily links to soil carbon and nitrogen through management practices (soil data not included here).
  - Data represent current and recent management practices, field age, crops, yields, fallow cycles, floods, erosion, pests, and qualitative field observations. Yields data are recall-based and conversions are uncertain.

- Study scope and aims
  - Examine how land use intensity and management practices influence soil fertility, nutrient status, and household well-being.
  - Gather information on dominant agricultural practices, land cover, and scarcity to inform interpretations of soil conditions over time.
  - Collect alongside soil data (not included in this release) to build a broader view of soil fertility changes.

- Data collection and methods
  - Village and field selection
    - Villages chosen to create a gradient of land-use intensity within each district (charcoal production in Mabalane; subsistence agriculture and forest extraction in Marrupa; smallholder commercial agriculture in Gurue).
    - 26 villages total; within each, 10 active fields were surveyed (excluding fallow fields).
    - Field age, ownership, and localization verified with local guides; surveys conducted with consent of field owners.
  - Field surveys and instrumentation
    - GPS mapping of field locations and perimeters using Garmin GPS devices.
    - Data collection via Android tablets with Open Data Kit (ODK) software; interviews conducted in local languages and translated to Portuguese, then English by the lead author.
    - Observational data recorded on field attributes, including tree species, cropping system, and qualitative features (e.g., termite activity).
  - Data structure and linking
    - Data organized into 12 interconnected datasets with a common field_id key (field_id links field-level data across datasets).
    - Field_id encodes village and field number. Blank entries indicate non-recorded data; -999 indicates unknown quantities. Some year fields use negative values to indicate pre-war or pre-independence years.

- Data structure and datasets (12 spreadsheets)
  - field_main_survey: Core interview data per field (date, location, area, owner, ownership year, field age, cropping type, etc.). District-specific questions noted (present/not present flags).
  - crops_planted: Crops normally planted in the field; crops planted in last year and in the first year recorded where applicable.
  - crop_yields: Quantitative yields for the most recent harvest per crop; may include yields in non-standard units (individuals or local units); blanks where not recorded.
  - yield_unit_conversion: Conversion factors and uncertainties to translate local harvest units to weight (kg) or transformed units; sources include local measures, MINAG (2008), and literature; notes on uncertainties.
  - fertiliser_use: Fertiliser types used, frequency, and extent of application.
  - pesticide_use: Pesticide use (only collected in Gurue) and frequency.
  - field_tilling: Tilling methods and frequency (hoe, ox plow, tractor, etc.).
  - insect_pest: Insect pests observed and qualitative frequency.
  - animal_pest: Animals raiding crops and qualitative frequency.
  - trees_on_field: Live trees currently on fields (local names; species identification done separately).
  - trees_before_cleared: Tree species present before the field was created (only in Mabalane); identification done separately.
  - indicator_species: Species (trees/ grasses) used as soil quality indicators; includes indicator_type (grass or tree) and species name.
  - Each dataset includes field_id to enable cross-dataset linkage; many fields use blanks for missing data; -999 for unknown values.

- Content highlights by dataset
  - Main field survey: District, field location, area, field age, ownership year, field type (intercropping/monocropping; subsistence/commercial), date sampled, soil samples (whether taken), yield data availability.
  - Crops planted: Crops normally planted; crops planted in last year; crops planted in first year; district-specific inclusions/exclusions.
  - Crop yields and yield units: Most recent harvest quantities; unit of harvest; any notes from interviewer; optional large-volume unit dimensions (recent_unit_dim_m3) when applicable.
  - Yield unit conversion: Details on conversion factors, uncertainties, and data provenance for translating local units to kilograms or transformed yields.
  - Fertiliser, pesticide, tilling: Practices and frequency; area of application (whole field vs partial); pesticide data limited to Gurue.
  - Pests and trees: Local names for insect and animal pests; counts/frequencies; live trees currently on fields; trees present before clearing (where available); indicator species for soil quality.
  - Quality control: Data quality assured by lead author; trained interviewers; translation workflow; emphasis on reducing ambiguity via pre-coded/binary responses; caution advised for yield data due to recall and conversion uncertainties.

- Data quality, limitations, and caveats
  - Data collection relies on farmer recall for historical yields and practices; unit conversions are uncertain and should be treated as rough estimates.
  - Soil data are not included in this release; integration with soil measurements requires access to the corresponding soil dataset.
  - District differences mean some questions were not asked in all districts; presence/absence flags indicate district coverage per question.
  - Some fields may have missing data (blanks) or unknown values (-999); year data may include negative values to denote pre-war or pre-independence periods.
  - Species identifications for trees and grasses were conducted separately; some grasses could not be identified due to lack of inflorescence.

- References and provenance
  - Data collection linked to broader ACES/ESPA research on land-use changes and ecosystem services.
  - Related publications and data sources include Baumert et al. (2016, 2017), MINAG (2008), and Woollen et al. (2016), among others.

- Access relevance for data leaders
  - Provides a rich, linked field-level dataset with standardized field_id linking across multiple data dimensions (agro-management, yields, pests, trees, soils indicators).
  - Emphasizes governance aspects: standardized data collection tools (ODK), GPS-based geolocation, district-specific adaptations, quality assurance by a lead author, and transparent documentation of uncertainties and data provenance.
  - Useful for evaluating data system design, metadata completeness, cross-district harmonization, and strategies for integrating recall-based agricultural data with objective measurements in learning how to manage data assets across networks.