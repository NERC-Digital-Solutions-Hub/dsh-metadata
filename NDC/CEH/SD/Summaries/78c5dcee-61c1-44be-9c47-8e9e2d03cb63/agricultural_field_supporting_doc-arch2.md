# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

- Scope and purpose
  - A collection of 259 smallholder agricultural field surveys from 26 villages across three districts in Mozambique.
  - Conducted as part of the ESPA-funded ACES project to understand how changing land use impacts ecosystem services and the wellbeing of rural poor.
  - Aimed at documenting current and historical field management practices that could affect soil carbon and nitrogen content, and to profile dominant agricultural practices and land cover dynamics. Soil data were collected but are not included in this dataset; they are described as being coupled with field data in separate work.

- Geographic and temporal coverage
  - Districts: Mabalane (Gaza Province), Marrupa (Niassa Province), Gurue (Zambezia Province).
  - Villages: 26 villages across the three districts, selected to represent gradients of land-use intensity.
  - Fields: 10 active fields per village (total 259 fields sampled).
  - Survey periods: Mabalane (May–September 2014), Marrupa (May–August 2015), Gurue (September–December 2015).

- Study design and sampling
  - Village selection aimed to create a gradient of land-use intensity (characterized by activities such as charcoal production, subsistence agriculture, forest resource extraction, and smallholder commercial agriculture).
  - Field selection within villages focused on active fields (no fallow fields sampled); ownership and accessibility verified with local guides.
  - Field age and ownership history served as a basis for stratified sampling, with guides identifying 2–3 new fields, 2–3 very old fields, and others in between.

- Data collection and methods
  - Structured interviews with field owners to collect information on:
    - Current management practices (inputs, tilling, fire and residue management)
    - Field age and ownership history
    - Crops planted in current and past years
    - Crop yields and yield trends
    - Fallow cycles, floods, erosion, pests, and wildlife issues
    - Qualitative field observations (e.g., presence of trees, cropping systems)
  - Data captured on paper forms or Android tablets using Open Data Kit (ODK); interviews conducted in local language and translated into Portuguese, then into English by the lead author.
  - Field location and perimeter mapped with GPS (Garmin etrex 10/30); area measured by field perimeter mapping.
  - Tree and grass species identification conducted separately (dataset submitted to the EIDC).

- Data structure and contents (12 interconnected datasets)
  - field_main_survey: core survey responses per field (location, area, ownership year, date sampled, etc.).
  - crops_planted: crops normally planted and crops planted in last year/first year.
  - crop_yield: quantitative yield data for the most recent harvest; note that long-term yield recall is avoided due to unreliability.
  - yield_unit_conversion: units and conversion factors for yields, with uncertainties and data sources.
  - fertiliser_use: fertilisers used, frequency, and application extent.
  - pesticide_use: pesticide use and frequency (collected only in Gurue).
  - field_tilling: tilling type and frequency.
  - insect_pest: insects reported as crop pests.
  - animal_pest: animals reported as crop pests.
  - trees_on_field: trees observed on fields at the time of survey.
  - trees_before_cleared: tree species present before fields were created (only in Mabalane).
  - indicator_species: tree/grass species used as indicators of good soil; identification mostly conducted separately.
  - All datasets link via a field_id (village initials + field number); blanks indicate missing/unknown data; -999 denotes unknown quantities or years; negative years indicate dates before specified historical points (e.g., pre-war).

- Data collection instruments and data quality
  - Equipment: Garmin GPS devices for field mapping; Android tablets for data collection with ODK.
  - Quality control: data quality assured by the lead author; field interviewers trained for consistent interviewing and recording; translations from local language to Portuguese and then to English performed by the lead author.
  - Data limitations and cautions:
    - Some questionnaire items differ between districts; differences explicitly noted in the datasets.
    - Soil data collected but not included in these supporting documents; field data intended to be coupled with soil data in separate work.
    - Crop yield data rely on recall for older years; therefore, only the most recent harvest yields are included as reliable quantitative data.
    - Yield unit conversions are highly uncertain and should be used as rough estimates; conversions based on local measures, national data (MINAG 2008), and published literature.
    - Some fields/datasets are incomplete due to non-recorded information or unknowns.

- Applications for environmental monitoring and analysis
  - Enables analysis of land-use intensity and management practices across diverse Mozambican smallholders.
  - Supports understanding of factors affecting soil fertility, carbon and nitrogen content, and broader ecosystem services in rural Mozambique.
  - Provides a rich baseline for temporal and spatial comparisons, and for integrating with soil data and other ecosystem service assessments.

- References and related context
  - ESPA ACES project and associated literature on land use, soil fertility, and ecosystem services in Mozambique.
  - Key studies on charcoal production, small-scale farming, and land-use intensification in the region.

- Access and usage notes
  - Data are organized into structured datasets designed for cross-field linkage via field_id.
  - The supporting documentation clarifies methodological differences by district and the limitations associated with recall-based yield data and unit conversions.
  - Data are intended for integration with soil measurements and broader ecosystem service analyses conducted by ACES and collaborators.