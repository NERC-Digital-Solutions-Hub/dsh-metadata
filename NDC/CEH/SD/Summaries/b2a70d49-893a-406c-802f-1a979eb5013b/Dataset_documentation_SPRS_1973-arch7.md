# Scottish Pinewood regeneration survey, 1973 Dataset Summary

- A follow-up survey to the Scottish Pinewood Survey (1971) investigating regeneration in 7 Scottish pinewoods.
- 419 plots of 200 m2 surveyed across the selected woods, with more plots per wood than in 1971.
- Data cover habitat, vegetation, trees/saplings/shrubs, soil pH, and regeneration using standardized procedures.

## Data Coverage and Structure (GIS-relevant)

- Geographic scope: Scotland; 7 woods (Mar, Abernethy, Barisdale, Glen Affric, Shieldaig, Loch Maree, Tyndrum).
- Time period: 1973; start dates for sites range from July to September 1973.
- Data categories:
  - Habitat Data: habitat types, slope, aspect, and site-level attributes.
  - Vegetation Data: three components per plot – trees/saplings/shrubs, vascular plants, bryophytes (Abernethy only).
  - Regeneration Data: regeneration heights, seedling counts, ground flora, soil attributes.
  - Soil Data: soil pH measured from various quadrats (top 10 cm).
- Spatial/attribute structure:
  - Plot-level data within each site, with site codes (OSGR references available in site summaries).
  - Data organized into separate CSV files describing plots/sites, ground flora, tree data, and regeneration data.

## Survey Design and Methods (key GIS attributes)

- Sample design: 7 woods selected from the 27 pinewoods in the 1971 survey; 419 plots total, each 200 m2.
- Plot layout: nested quadrat system for vegetation; trees/saplings recorded across the plot; regeneration sampled within central quadrats.
- Measurements:
  - Habitat: predefined categories; slope (degrees) and aspect (bearing).
  - Vegetation: DBH and height for trees; height of widest tree; saplings/shrubs recorded; vascular plant lists with percent cover; bryophytes (Abernethy only).
  - Regeneration: pin-marked seedlings up to 1.3 m; regeneration quadrats (25 cm diameter) for first five seedlings of each species; heights of tallest shoot and seedling; ground flora and soil attributes recorded.
  - Soil: top 10 cm soil samples for pH from seedling and non-seedling quadrats.
- Data quality/standards: follow Bunce & Shaw (1973) standardized survey methods; field documentation includes a field handbook with precise classifications.

## Data Tables and Schema (Summary of files)

- SPRS_1973_PLOT_SITE_DESCS.csv
  - Description: Plot and site descriptions; habitat information; start dates; sheet references.
  - Key fields: SITE_NO, SITE, START_DATE, PLOT_NO, DESCRIPTION, SHEET, CODE_GROUP, CODE_GROUP_DESC.

- SPRS_1973_PLOTS.csv
  - Description: Plot aspect, slope, and soil pH information; site and plot identifiers.
  - Key fields: SITE_NO, SITE, PLOT_NO, DATE, PLOT_SLOPE, PLOT_ASPECT, PH_NON_REG, PH_BIRCH, PH_ROWAN, PH_SPINE, PH_SALIX.

- SPRS_1973_GROUND_FLORA.csv
  - Description: Vascular plants and bryophytes (Abernethy); presence and cover data.
  - Key fields: SITE_NO, SITE, PLOT_NO, NEST, SP_CODE, BRC_NAMES, COMMON_NAME, GROWTH_FORM, TOT_COVER, SDG_COUNT, TYPE.

- SPRS_1973_TREE_DATA.csv
  - Description: Trees, saplings and shrubs – DBHs and heights.
  - Key fields: SITE_NO, SITE, PLOT_NO, NEST, TREE_NO, TREE_CAT, TREE_SP, DBH, DEAD, HT.

- SPRS_1973_REGEN.csv
  - Description: Scots Pine regeneration data – heights, seedling measurements, soil and ground cover.
  - Key fields: SITE_NO, SITE, PLOT, SHEET, NEST, REGEN_TYPE, CODE, DESCRIPTION, CODE_PC, TYPE.

## How this supports GIS work

- Rich, multi-layer data for mapping habitat types, vegetation structure, regeneration status, and soil conditions at plot level.
- Spatial references embedded via site codes and OS grid references (OSGR) in site descriptions, enabling GIS integration and spatial analysis.
- Data allow exploration of spatial patterns of regeneration across seven woods, as well as associations between habitat categories, soil pH, and vegetation structure.
- Some data (Bryophytes) limited to Abernethy; dataset provides a clear schema for handling missing data (Y/N indicators).

## References and Context

- Related datasets: Scottish Pinewood Survey 1971 (reference Bunce & Shaw 1971; Bunce & Shaw 1973; 2015 Bunce et al. work).
- Key methodological sources: National Woodland Classification 1971: Handbook of Field Methods; A Standardized Procedure for Ecological Survey (Bunce & Shaw, 1973).
- Acknowledgements: survey management, laboratory assistance, field surveyors, and data management team listed in the document.

## Acknowledgements

- Survey management: R. Bunce
- Laboratory assistance: C. Barr
- Field surveyors: Aberdeen University postgraduate students
- Data management and documentation: C. Wood, B. Dodd, C. Hallam