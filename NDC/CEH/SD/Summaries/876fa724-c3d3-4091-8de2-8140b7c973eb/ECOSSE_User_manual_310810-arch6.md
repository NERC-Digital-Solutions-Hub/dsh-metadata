# D2.2 Format of Output File for Results on 20km 2 grid

- For each 20km2 grid cell, outputs cover the profile to the depth specified in line 9 of GNAMES.DAT.
- Lines 1 & 2: Title lines
- Lines 3 onward: ID of 20km2 grid cell, followed by Easting and Northing
- Carbon change per land use change (kt C km-2 10years-1) for Decade 1, with the following LU change pairings:
  - Arable to arable, Grassland to arable, Forestry to arable, Natural/semi-natural to arable, Miscanthus to arable, SRC to arable
  - Arable to grassland, Grassland to grassland, Forestry to grassland, Miscanthus to grassland, SRC to grassland
  - Natural/semi-natural to grassland
  - Arable to forestry, Grassland to forestry, Forestry to forestry, Natural/semi-natural to forestry, Miscanthus to forestry, SRC to forestry
  - Arable to natural/semi-natural, Grassland to natural/semi-natural, Forestry to natural/semi-natural, Natural/semi-natural to natural/semi-natural, Miscanthus to natural/semi-natural, SRC to natural/semi-natural
  - Arable to miscanthus, Grassland to miscanthus, Forestry to miscanthus, Natural/semi-natural to miscanthus, Miscanthus to miscanthus, SRC to miscanthus
  - Arable to SRC, Grassland to SRC, Forestry to SRC, Natural/semi-natural to SRC, Miscanthus to SRC, SRC to SRC
- Decade 2 to Decade 7 follow with similar LU change pairings, including Decade 7 (LU change projections using decade 6)
- Carbon change for all soils in the cell (kt C km-2 10years-1) per decade 1–7
- Carbon change for organic soils in the cell only (kt C km-2 10years-1) per decade 1–7

# D2.3 Format of Output File for C Change data ('CHANGE.OUT')

- For each 20km2 grid cell, outputs begin with the grid ID and grid coordinates
- Fields:
  - Series
  - Land use 1 and Land use 2
  - Fraction of first 1km2 cell in 20km2 grid that changes from LU1 to LU2 in decade 5 (or specified decade)
- For each decade (1–7):
  - C Change (t C/ha/decade)
  - CO2 emission (t C/ha/decade)
  - CH4 emission (t C/ha/decade)
  - N2O emission (t C/ha/decade)
  - Total GHG emission in CO2 equivalents (t C/ha/decade)
  - Carbon content of soil at start (%C)
  - Clay content (% clay)
  - Error in simulation? (0=No; 1=Yes)

# D2.4 Format of Climate Change Results file

- For each 1km2 grid cell, outputs cover the profile to the depth specified in line 9 of GNAMES.DAT
- Line 1: Title line
- Decade 2–7: sections per decade
  - Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC
- Lines 2 onward: ID of 20km2 grid cell, grid coordinates (Easting, Northing)
- Carbon change per land use (t C km-2 10years-1) per decade

# D2.5 Format of File for Calculation of Effects of Different Mitigation Options (e.g., MIT_A2P.OUT)

- For each 1km2 grid cell, outputs cover the profile to the depth specified in line 9 of GNAMES.DAT
- Lines 1 and 2: Title lines
- Lines 3 onward: ID of 20km2 grid cell
- Grid details:
  - Dominant soil series 1–5
  - Wetness class
  - % C in top soil layer
  - % clay in top soil layer
  - Fraction of 1km2 cell that has this land use (km2/km2)
- Decade 1–7: carbon change associated with LU change applied in the first decade (t C/ha/km2/decade)

# Data Product Characteristics for Data Support

- Structure supports GIS-based visualization and policy analysis with explicit 20km2 and 1km2 grid outputs, including per-decade LU-change breakdowns and organic-soil-specific results.
- Enables cross-comparison of land-use change scenarios (e.g., Arable to Grassland, Grassland to Forestry) and their C balance and greenhouse gas emissions (CO2, CH4, N2O) with CO2-equivalent totals.
- Provides metadata fields useful for data quality checks (e.g., Error in simulation flag) and initial soil characteristics (start %C, % clay).
- File naming and depth parameters are governed by GNAMES.DAT and related input files, ensuring consistent extraction and integration into GIS or dashboards.
- Supports mitigation-option analyses (via MIT_A2P.OUT and related files) by coupling land-use scenarios with soil properties and broad C-climate metrics.

# Relevance to Data Support Archetype

- Delivers ready-to-use, structured data products that stakeholders can explore, combine with other datasets, and visualize.
- Facilitates self-serve data workflows for policy planning, inventory updates, and scenario analysis at regional to national scales.
- The explicit formatting and decadal breakdowns aid reproducibility, data validation, and dissemination to non-technical end users.