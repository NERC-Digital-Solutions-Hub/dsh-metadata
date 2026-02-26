# Bunce Woodland Survey of Great Britain 2020-2022

- A repeat survey of 97 broadleaved woodlands across Great Britain conducted from 2020 to 2022.
- Data collected at site level and in detail from 16 randomly located 200 m2 plots per site.
- Ecological information includes canopy and ground flora composition, soil pH and soil organic matter (Loss on ignition), habitat management, and numerous plot- and site-level descriptors.
- Repeats the methodological framework of earlier surveys (1971; 2000-2003; referred to as the '2001 survey') to enable long-term analyses.

## Overview and Aims

- Purpose: Enable analyses of ecological change since the 2000-2002 survey and support long-term ecological change assessment in British woodlands.
- Scope: 97 woodland sites surveyed between 2020 and 2022; data designed for cross-temporal comparisons with earlier Bunce surveys.
- Methods reference: Standardized survey procedures (Bunce & Shaw 1973) and the 2021 field handbook (Smart, S.M. and Wood, C.M.) for national woodland and native pine surveys.

## Data Coverage

- Geographic scope: 97 broadleaved woodland sites across Great Britain (some sites not accessed; marked with asterisks in the site list).
- Survey design: Stratified sampling across the area; 16 plots per site, each 200 m2, with data collected on flora, soils, and tree structure.
- Timeframe: Data collection conducted during the 2020-2022 period; builds on 1971, 2000-2003 baselines and 2018-2022 Scottish pinewood baseline where relevant.

## Data Categories and Structures

- SITE LIST (WOOLAND_SURVEY_SITES_2022)
  - Contains approximate site locations and identifiers (SITE_NUMBER, SITE_NAME, EASTING/NORTHING/OSGR).
  - Notes that some sites were not granted access for the 2020-2022 survey.

- SITE INFORMATION (WOODLANDS_SURVEY_SITE_INFORMATION_2022)
  - Descriptions at the whole-site and plot levels, including habitat, animal descriptions, slope, aspect, and survey dates.
  - Includes SITE_NO, SITE_NAME, PLOT_NO, CODE_GROUP, CODE_DESCRIPTION, CODE, DESCRIPTION, CODE_VALUE, and OTHER fields.

- TREE DATA (WOODLANDS_SURVEY_TREE_DATA_2022)
  - Per-plot tree records: SITE_NO, SITE_NAME, PLOT_NO, QUARTER, TREE_TYPE (Tree/Sapling/Shrub), MULTI and MULTI_ID, DEAD status, SP_CODE, SPECIES, DBH, SHEET.
  - Captures species occurrence, diameter at breast height, and tree structure details.

- GROUND FLORA (WOODLANDS_SURVEY_GROUND_FLORA_2022)
  - Per-plot flora data: SITE_NO, SITE_NAME, PLOT_NO, NEST, BRC_NUMBER, BRC_NAMES, COVER metrics (NEST_1_COV, TOTAL_COVER), GROWTH_FORM, etc.
  - Uses Biological Record Centre codes and Stace nomenclature for species identification.

- SOIL DATA (WOODLANDS_SURVEY_SOIL_DATA_2022)
  - Plot-level soil analyses: SITE_NO, SITE, PLOT_NO, SOIL, SOIL_DATE, PH_FRESH, PH_AIRDRY, LOI_PERCENT, MISSING_CODE, SAMPLE_NOTES.
  - Includes notes on missing samples and data quality.

## Methodology and Documentation

- Field methods: Adheres to Bunce & Shaw (1973) standardized ecological survey procedures; field handbook published in 2021.
- Data standards: Uses Stace (1997) nomenclature for ground flora; BRC species codes for ground flora records.
- Data provenance: Prepared by S.M. Smart and C.M. Wood (UKCEH Lancaster); survey field staff and soil analysis teams listed in the document.
- Data sheets and codes: Detailed within the SITE_INFORMATION section, referencing the field handbook for coding and data entry.

## Related Datasets and Baselines

- Bunce National Woodland Survey 1971 (and repeats 2000-2003)
- Countryside Survey
- Scottish Pinewood Survey 1971 (repeated 2018-2022)
- Steele (1968) National survey of woodlands
- References and further reading provide methodological and analytical context for long-term ecological change studies.

## Usage, Access, and Quality Notes

- Accessibility: Some sites noted as not accessible during 2020-2022 (asterisk markers in the site list).
- Data completeness: Notes indicate 7 soil samples with missing plot numbers; some codes and fields may be missing or subject to quality control notes.
- Data formats: CSV files for sites, site information, tree data, ground flora, and soil data.
- Intended use: Longitudinal analyses of ecological change, cross-temporal comparisons with earlier Bunce surveys, and examination of ecological drivers in British woodlands.

## References and Further Reading

- Bunce, R.G.H. & Shaw, M.W. (1973). A Standardized Procedure for Ecological Survey.
- Smart, S.M. & Wood, C.M. (2021). National Woodland Survey & Native Pine Survey Field Handbook.
- Stace, C. (1997). New flora of the British Isles.
- Further reading includes analyses of landscape-scale drivers, long-term ecological change, and methodology for woodland surveys.