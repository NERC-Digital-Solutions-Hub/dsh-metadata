# Bunce Woodland Survey of Great Britain 2020-2022

## Overview
- A repeat survey of broadleaved woodlands across Britain conducted between 2020 and 2022.
- 97 woodland sites surveyed; ecological information collected at the site level and in detail from 16 randomly located 200 m² plots per site.
- Data cover canopy and ground flora composition, soil pH, soil organic matter (Loss on ignition), habitat management, and various plot- and site-level descriptors.
- Built to enable analyses of ecological change since earlier surveys (1971; 2000–2003; referred to as the 2001 survey).
- GIS-ready data intended for broad use by researchers and practitioners interested in woodland ecology and change over time.

## Geographic and Temporal Coverage
- Geographic scope: Great Britain (97 woodland sites).
- Timeframe: 2020–2022.
- Spatial data: site locations provided as approximate point features with Easting/Northing (BNG OSGB36) and OS grid references (OSGR) for each site.

## Data Products and Dataset Structure
- WOODLANDS_SURVEY_SITES_2022.csv
  - Description: Approximate locations of surveyed woodlands as point features.
  - Key fields: SITE_NUMBER (1–103), SITE_NAME, EASTING, NORTHING, OSGR.
  - Note: Some sites marked with an asterisk indicate access restrictions (not granted in 2020–2022).
- WOODLANDS_SURVEY_SITE_INFORMATION_2022.csv
  - Description: Site- and plot-level descriptions, including habitat, slope, aspect, and survey metadata.
  - Key fields: SITE_NO, SITE_NAME, PLOT_NO (1–16), CODE_GROUP, CODE_GROUP_DESCRIPTION, CODE, DESCRIPTION, CODE_VALUE, OTHER, DATA_SHEET.
  - Use: supports contextual mapping of plots within each site and interpretation of codes.
- WOODLANDS_SURVEY_TREE_DATA_2022.csv
  - Description: Tree data from each plot, including diameter at breast height (DBH).
  - Key fields: SITE_NO, SITE, PLOT_NO, QUARTER (1–4), TREE_TYPE (Tree/Sapling/Shrub), MULTI, MULTI_ID, DEAD, SP_CODE, SPECIES, DBH, SHEET.
  - Use: enables spatial analysis of tree size structure and species distribution within plots.
- WOODLANDS_SURVEY_GROUND_FLORA_2022.csv
  - Description: Ground flora records (vascular plants and bryophytes) for each plot, with cover and growth form data.
  - Key fields: SITE_NO, SITE_NAME, PLOT_NO, NEST, BRC_NUMBER, BRC_NAMES, NEST_1_COV, TOTAL_COVER, GROWTH_FORM, etc.
  - Use: supports species distribution and habitat quality mapping at plot level.
- WOODLANDS_SURVEY_SOIL_DATA_2022.csv
  - Description: Plot soil data from analyses (pH, LOI, etc.).
  - Key fields: SITE_NO, SITE, PLOT_NO, SOIL, SOIL_DATE, PH_FRESH, PH_AIRDRY, LOI_PERCENT, MISSING_CODE, SAMPLE_NOTES.
  - Notes: -9999 denotes missing values; seven samples have missing plot numbers (labelled >16 for matching issues).

## Survey Design and Methods
- Design: Stratified sampling across each site; 16 plots per site (200 m² each) located randomly within the woodland.
- Field methods: Follow Bunce & Shaw’s (1973) standardized ecological survey procedures; field handbook updated in 2021 (National Woodland Survey & Native Pine Survey Field Handbook, Smart & Wood).
- Data types collected: canopy and ground flora composition, soil chemistry (pH, LOI), habitat management, and a wide range of plot- and site-level descriptors.
- Data quality and reproducibility: Described methods and handbooks facilitate consistent re-survey and temporal analyses.

## Provenance, Field Teams, and References
- Originators: S.M. Smart, C.M. Wood, F.M. Seaton (UK Centre for Ecology & Hydrology, Lancaster).
- Field surveyors: listed in the dataset (multiple individuals across sites).
- Soil analyses: C. Benskin and team.
- Related references and context:
  - Bunce & Shaw (1973): Standardized procedure for ecological survey.
  - Smart & Wood (2021): Field handbook for national woodland survey and native pine survey.
  - Stace (1997): Nomenclature reference for flora.
- Related/earlier datasets for context and comparison:
  - Bunce National Woodland Survey 1971 and 2000–2003.
  - Countryside Survey.
  - Scottish Pinewood Survey (1971, repeated 2018–2022).

## How to Use for GIS and Spatial Analysis
- Primary keys: SITE_NO and PLOT_NO link plots to sites; SITE_NAME provides descriptive naming; coordinates in WOODLANDS_SURVEY_SITES_2022.csv enable spatial plotting of site points.
- Data integration: join datasets by SITE_NO (and PLOT_NO for plots), enabling multi-layer GIS analyses (site-level context, plot-level vegetation, soil, and tree metrics).
- Data categories include both site-level and plot-level records, requiring careful handling (e.g., CODE_GROUP and CODE_GROUP_DESCRIPTION in SITE_INFORMATION) to interpret coded fields.
- Coordinate reference: OSGB36/BNG coordinates provided for site locations, suitable for UK-focused GIS work.

## Limitations and Notes
- Access-restricted sites indicated by asterisks in the site list.
- Some entries in the site and plot records may have missing values; -9999 and other QC notes are included in soil data.
- The dataset is a historical baseline intended for longitudinal analyses, enabling comparisons with earlier Bunce surveys and subsequent re-surveys.

## Additional Resources
- Field handbook and methodological references available in the accompanying documentation.
- Further reading includes long-term ecological change studies in British woodlands and methodological comparisons across surveys.