# 'Bunce' Scottish Pinewood Survey 2018-2022 Habitat, vegetation, tree and soil data from Native Pinewoods in Scotland, 2018-2022

## Overview
- A detailed ecological survey of Scots Pine woodlands across Scotland, conducted 2018–2022.
- Repeats the 1971 baseline survey to enable environmental monitoring and assessment of change.
- 27 woods were surveyed; within each wood, 16 randomly selected 200 m² plots were sampled using standardized procedures.

## Geographical Coverage
- Location: Scotland.
- Woods covered include Glentanar, Ballochbuie, Mar, Abernethy, Rothiemurchus, Glenmore, Black Wood of Rannoch, Ardgour, Shieldaig, Old Wood of Meggernie, Glen Moriston, Glengarry, Barrisdale, Glen Affric, Glen Cannich, Glen Strathfarrar, Guisachan and Cougie, Coulin, Amat, Loch Maree, Black Mount, Glen Orchy, Tyndrum, Glen Feshie, Loch Arkaig and Glen Mallie, and Achnashellach. Note: Dulnan has little Scots pine remaining.
- Original purpose: define ecological variation in pinewoods and support conservation; repeat survey enables monitoring of change.

## Survey Design & Methods
- Sample design: all major native pinewoods from the 1971 survey were included; 16 random 200 m² plots per wood.
- Methods follow Bunce & Shaw (1973) with details in the National Woodland Survey & Native Pine Survey Field Handbook (Smart & Wood, 2021).
- Vegetation data per plot in three categories: trees/saplings/shrubs; vascular plants; bryophytes (ground flora).
- Nested quadrat approach for vascular plants (4 m², 25 m², 50 m², 100 m², 200 m²) with % cover estimates; bryophytes recorded for the plot.
- Soil data: pH and loss on ignition (LOI) measured from topsoil (0–15 cm).
- Habitat data: habitat types, slope, and aspect recorded; additional site descriptions.
- Data coding and classifications follow standardized field codes; additional plots beyond 16 per site (up to 50 at Abernethy) were also undertaken.

## Data Available per Site
- Site-wise metadata include start dates, site descriptions, and the presence/absence of plot-level data (soil, ground flora, tree data, plot data).

## Data Tables and Descriptions
- SCOTS_PINE_2022_SITES.csv
  - Approximate locations of surveyed Scots Pine woodlands (27 sites).
  - Fields: SITEID, SITE_NAME, OSGR, EASTING, NORTHING.
- SCOTS_PINE_2022_SITE_INFO.csv
  - Descriptions of surveyed sites (wood) and plots, including habitat descriptions, animal signs, and tree descriptions.
  - Fields include SITE_NO_SP, SITE_NAME, PLOT_NO, CODE_GROUP, DESCRIPTION, DATA_SHEET, etc.
- SCOTS_PINE_2022_TREE_DATA.csv
  - Tree data per plot, including DBH, species, tree type, dead indicator, nest info.
  - Fields: SITE_NO, PLOT_NO, TREE_ID, NEST, TREE_TYPE, SPECIES, DBH, DEAD, DATA_SHEET.
- SCOTS_PINE_2022_GROUND_FLORA.csv
  - Ground flora records for vascular plants and bryophytes per plot.
  - Fields include SITE_NO, PLOT_NO, NEST, BRC_NUMBER, BRC_NAME, COMMON_NAME, TOTAL_COVER, GROWTH_FORM, etc.
- SCOTS_PINE_2022_SOIL_DATA.csv
  - Soil data per plot: pH (fresh and air-dry), LOI, SOIL_DATE.
  - Fields: SITE_NO, PLOT_NO, PH_FRESH, PH_AIRDRY, LOI_PERCENT, SOIL_DATE.
- Note: All data follow standardized field sheets and coding; missing values use -9999 where applicable.

## Data Quality & Standards
- Standardized procedures derived from Bunce & Shaw (1973) with field handbook updates (Smart & Wood, 2021).
- Data organized per site and per plot with consistent coding for habitat, vegetation, and soil characteristics.
- Tables provide both site-level and plot-level detail to support aggregation, trend analysis, and cross-site comparisons.

## Related Datasets & References
- Baseline context:Scottish Pinewood Survey 1971; Bunce National Woodland Survey 1971 (same methodology), repeated 2000–2003 and 2020–2022.
- Field handbooks and method standards: National Woodland Survey & Native Pine Survey Field Handbook (Smart & Wood, 2021); Ecological survey references (Shaw & Bunce, 1971; Stace, 1997; Wood & Bunce, 2016).
- Originators: UK Centre for Ecology & Hydrology (Lancaster) and collaborating teams.
- Related datasets and follow-up: 1971 surveys and subsequent repeat surveys; references listed in the documentation.

## Access & Usage Notes
- Data provided as CSV files with explicit site, plot, and measurement fields suitable for integration with other pinewood datasets.
- 2018–2022 time frame enables assessment of change since the 1971 baseline.
- Useful for ecological monitoring, conservation planning, habitat classification, and data-driven policy support related to native pinewoods in Scotland.