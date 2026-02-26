# Bunce' Scottish Pinewood Survey 2018-2022

## Overview
- A detailed ecological survey of native Scots pinewoods in Scotland conducted from 2018 to 2022.
- Involves 27 woods across northern Scotland, with 16 randomly selected 200 m² plots per wood.
- Repeats the baseline survey from 1971 to enable environmental monitoring and assessment of change over time.
- Data collected cover habitat, vegetation (trees, ground flora, bryophytes), soil properties, and habitat types using standardized procedures.

## Geographic Coverage
- Region: Scotland
- Woods surveyed: 27 named sites (e.g., Glentanar, Ballochbuie, Mar, Abernethy, Rothiemurchus, Glenmore, Black Wood of Rannoch, Shieldaig, Old Wood of Meggernie, Glen Moriston, Glengarry, Barisdale, Glen Affric, Glen Cannich, Glen Strathfarrar, Guisachan and Cougie, Coulin, Amat, Loch Maree, Black Mount, Glen Orchy, Tyndrum, Glen Feshie, Loch Arkaig and Glen Mallie, Achnashellach, among others)
- Note: The Dulnan has little Scots pine remaining and is west of Abernethy (4) and north of Glen Feshie (7).
- Timeframe: 2018–2022; baseline in 1971 used for comparison.

## Purpose and Survey Design
- Original purpose (1971): define ecological variation in native pinewoods and develop an integrated conservation strategy; enable monitoring of change.
- Repeat design (2018–2022): survey all major native pinewoods identified in the 1959 literature; 16 randomly assigned 200 m² quadrats per wood.
- Methodology: Based on Bunce & Shaw (1973) with details in the National Woodland Survey & Native Pine Survey Field Handbook (Smart & Wood, 2021).

## Data Collected

### Vegetation Data
- Three data categories per plot:
  - Trees, saplings & shrubs (recorded by individual trees; coppice stools and dead indicators)
  - Vascular plants (species lists in nested quadrats: 4 m², 25 m², 50 m², 100 m², 200 m² with increasing area)
  - Bryophytes (ground flora)
- Nested quadrat system and percent cover by species (with 5% bands; 1% for present) plus total cover for the plot
- Additional cover/abundance metrics: litter, wood, rock, bare ground, water
- Data coded according to field handbook specifications

### Soil Data
- Topsoil (0–15 cm) analysis for:
  - pH (fresh soil) and pH (air-dried soil)
  - Loss on ignition (LOI, %)

### Habitat Data
- Habitat categories classified per 200 m² plot with multiple classes (as detailed in the field handbook)
- Measured slope (degrees) and aspect (bearing)
- Site-level and plot-level habitat descriptors, including vegetation, rocks, water bodies, human-made features, and other descriptions

## Data Files and Schemas
- SCOTS_PINE_2022_SITES.csv
  - Approximate locations of the 27 surveyed Scots Pine woodlands
  - Site ID, name, grid reference, Easting/Northing (BNG)
- SCOTS_PINE_2022_SITE_INFO.csv
  - Descriptions of surveyed sites (whole woodland) and plots (individual plots)
  - Includes site name, plot slope/aspect, survey dates, data sheet classifications
- SCOTS_PINE_2022_TREE_DATA.csv
  - Tree-level data per plot
  - Fields: SITE_NO, PLOT_NO, TREE_ID, NEST, TREE_TYPE, SPECIES, DBH, DEAD, etc.
- SCOTS_PINE_2022_GROUND_FLORA.csv
  - Ground flora per plot
  - Fields: site, plot, nest, species codes/names, cover metrics, growth form
- SCOTS_PINE_2022_SOIL_DATA.csv
  - Plot soil data
  - Fields: SITE_NO, PLOT_NO, PH_FRESH, PH_AIRDRY, LOI_PERCENT, SOIL_DATE

## Data Collection Details
- Each of the 27 woods contains 16 plots (additional up to 50 plots at Abernethy site 4)
- Vegetation, soil, and habitat data collected using standardized field methods (field handbook by Smart & Wood, 2021)
- Data provenance includes field survey teams, field procedures, and references to baseline 1971 methods

## Data Quality, Access, and Usage Notes
- Standardized methodologies enable comparison with 1971 baseline surveys and subsequent repeats
- Codes for habitat and data groupings are defined in the field handbook; cross-referencing may be required for interpretation
- LOI values may include missing data indicated by -9999
- Data are organized to support analyses of ecological variation, change over time, and conservation planning

## Related Datasets and References
- 1971 baseline: Ecological survey of the native pinewoods of Scotland (1971)
- Scottish Pinewood Survey 1971; Bunce National Woodland Survey 1971 (and repeats in 2000–2003, 2020–2022)
- Field Handbook: National Woodland Survey & Native Pine Survey Field Handbook (Smart & Wood, 2021)
- Standardized Procedure for Ecological Survey: Bunce & Shaw (1973)
- Flora references: Stace (1997)
- Key comparative work: Wood & Bunce (2016) Ecological survey of the native pinewoods of Scotland (ESSD)

## Acknowledgements
- Field surveyors and collaborators listed; land permissions and project originators documented
- Prepared by UK Centre for Ecology & Hydrology, Lancaster