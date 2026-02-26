# Bunce Woodland Survey of Great Britain 2020-2022

## Overview
- A repeat survey of 97 broadleaved woodlands across Great Britain conducted from 2020 to 2022.
- Builds on earlier surveys (1971; 2000-2003, referred to as '2001') using the same field methods to enable analyses of ecological change over time.
- Ecological data collected at the site level and from 16 randomly located 200 m² plots within each site.
- Data collected include plant species composition (canopy and ground flora), soil pH and soil organic matter (loss on ignition), habitat management, and a wide range of other plot- and site-level descriptors.

## Data Coverage and Design
- Coverage: 97 woodland sites across Britain; some sites marked with asterisks indicate access was not granted for the 2020-2022 survey.
- Survey design: Stratified sampling across the area; field methods follow Bunce & Shaw (1973) standardized procedures; field handbook by Smart & Wood (2021) provides detailed methods.
- Data collection aims: Allow analyses of ecological change since the 2000-2002 survey and facilitate cross-site comparisons with historical datasets.

## Data Files and Structure
- WOODLANDS_SURVEY_SITES_2022.csv
  - Description: Approximate locations of surveyed woodlands as point features.
  - Key fields: SITE_NUMBER, SITE_NAME, EASTING, NORTHING, OSGR (grid reference).

- WOODLANDS_SURVEY_SITE_INFORMATION_2022.csv
  - Description: Descriptions of surveyed sites (whole woodland) and surveyed plots (individual plots), including habitat and tree descriptions; notes slope and aspect, survey dates.
  - Key fields: SITE_NO, SITE_NAME, PLOT_NO, CODE_GROUP, CODE_GROUP_DESCRIPTION, CODE, DESCRIPTION, CODE_VALUE, OTHER, DATA_SHEET.

- WOODLANDS_SURVEY_TREE_DATA_2022.csv
  - Description: Tree species data from each plot, including diameter at breast height (DBH).
  - Key fields: SITE_NO, SITE, PLOT_NO, QUARTER, TREE_TYPE, MULTI, MULTI_ID, DEAD, SP_CODE, SPECIES, DBH, SHEET.

- WOODLANDS_SURVEY_GROUND_FLORA_2022.csv
  - Description: Ground flora records for plots, including vascular plants, bryophytes, and related cover and growth form data.
  - Key fields: SITE_NO, SITE_NAME, PLOT_NO, NEST, BRC_NUMBER, BRC_NAMES, NEST_1_COV, TOTAL_COVER, GROWTH_FORM.

- WOODLANDS_SURVEY_SOIL_DATA_2022.csv
  - Description: Plot soil data from analyses; includes pH (fresh and air-dry), loss on ignition (LOI), and related metadata.
  - Key fields: SITE_NO, SITE, PLOT_NO, SOIL, SOIL_DATE, PH_FRESH, PH_AIRDRY, LOI_PERCENT, MISSING_CODE, SAMPLE_NOTES.

## Background and Context
- The 2020-2022 repeat survey was initiated to compare with the 2000-2003 survey across the same sites and methods, enabling assessment of ecological changes since the early 2000s.
- Historical context: The original Bunce 1971 survey investigated 103 broadleaved woodlands with similar field methods; subsequent surveys in 2000-2003 (2001) revisited sites.
- Users are advised to consult the referenced publications and the field handbook for methodological details and prior analytical results.

## Related Datasets and References
- Bunce R.G.H. & Shaw M.W. (1973). A Standardized Procedure for Ecological Survey.
- Smart, S. M. and Wood, C. M. (2021). National Woodland Survey & Native Pine Survey Field Handbook.
- Stace, C. (1997). New flora of the British Isles.
- Related historical datasets: Bunce National Woodland Survey 1971 (and 2000-2003), Countryside Survey, Scottish Pinewood Survey 1971/2018-2022, and other historic woodland surveys.

## Use and Potential Analyses
- Assess long-term ecological change by comparing 2020-2022 data with 1971 and 2000-2003 baselines.
- Analyze changes in canopy and ground flora composition, soil chemistry (pH, LOI), and habitat management practices across sites.
- Enable self-service exploration of data through site- and plot-level datasets (sites, plot descriptions, tree data, ground flora, and soil data).
- Cross-reference with related datasets for broader landscape-scale analyses (e.g., Countryside Survey, Scottish Pinewood Survey).

## Quality, Access, and Notes
- Some sites were not accessible during the 2020-2022 survey; access restrictions are noted in the site list.
- Data files include quality-control notes and field-recorded codes; refer to the field handbook and code descriptions for interpretation of CODE_GROUP and CODE_VALUES.
- Data are provided in CSV format with explicit site and plot identifiers to support merging and longitudinal analyses.