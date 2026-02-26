# Model to Estimate Carbon in Organic Soils - Sequestration and Emissions (ECOSSE)

## Overview of Output Formats (D2.x)

- The ECOSSE documentation provides structured output files to support grid-based, policy-oriented analyses of soil carbon dynamics and greenhouse gas (GHG) emissions.
- Outputs are grid-specific (1 km2 and 20 km2 scales) and are aligned with land-use changes, climate scenarios, and mitigation options.
- Depths and grid references are defined to a specified soil profile depth (as per GNAMES.DAT).

## D2.2 Format of Output File for Results on 20km2 Grid

- For each 20 km2 grid cell, outputs cover the profile depth defined in GNAMES.DAT line 9.
- File contents include:
  - Title lines (Lines 1–2) and grid cell identifiers (Lines 3–end): ID, Easting, Northing.
  - Carbon change per land-use change (kt C km-2 per 10 years) across multiple decades.
  - Land-use transition columns for Decade 1 (e.g., Arable to arable, Grassland to arable, Forestry to arable, etc.).
  - Decade 2 to Decade 7 sections with LU transitions repeated.
  - Separate summaries for: carbon change for all soils and carbon change for organic soils only (by decade).

## D2.3 Format of Output File for C Change data ('CHANGE.OUT')

- For each 20 km2 grid cell, outputs include:
  - Title line; identification of grid (ID, grid reference, easting, northing).
  - Series and Land Use 1 to Land Use 2 transitions.
  - Fraction of the first 1 km2 cell in the 20 km2 grid that changes from LU1 to LU2 in decade 5 (and analogous entries for other decades).
  - For each decade (1–7):
    - C Change (t C/ha/decade)
    - CO2 emission (t C/ha/decade)
    - CH4 emission (t C/ha/decade)
    - N2O emission (t C/ha/decade)
    - Total GHG emission in CO2 equivalents (t C/ha/decade)
  - Additional metadata per cell:
    - Carbon content of soil at start (%C)
    - Clay content (% clay)
    - Error in simulation? (0 = No; 1 = Yes)

## D2.4 Format of Climate Change Results file

- For each 1 km2 grid cell, outputs cover the profile depth defined in GNAMES.DAT line 9.
- Structure includes:
  - Line 1: Title line
  - Decades 2–7 listed (Decade 2, Decade 3, … Decade 7)
  - For each 1 km2 cell: ID, Easting, Northing
  - Carbon change per land use (t C km-2 per 10 years) by decade
  - Land-use transition columns for Decade 2–Decade 7 (e.g., Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC)

## D2.5 Format of File for Calculation of Effects of Different Mitigation Options (MIT_A2P.OUT, etc.)

- For each 1 km2 grid cell, results include:
  - Title lines (Lines 1–2)
  - ID of 1 km2 grid and corresponding 20 km2 grid reference (Lines 3–end)
  - Dominant soil series (1–5) and Wetness class
  - % C in the top soil layer and % clay in the top soil layer
  - Fraction of the 1 km2 cell that has a given land-use (km2/km2)
  - Decades 1–7 with carbon change associated with LU change applied in the first decade (t C/ha/km2/decade)

## Practical Implications for Analysts

- Enables spatially explicit tracking of carbon change and GHG emissions under different land uses, climate scenarios, and mitigation options.
- Output files are designed for integration with GIS and grid-based policy analyses at both national and field scales.
- Separate outputs for all soils and for organic soils support targeted assessment of organic-soil management strategies.
- Includes quality and provenance indicators (e.g., error flags) to support data cleaning and uncertainty assessment.

## References and Model Foundation

- The D2 outputs are grounded in a broad set of references (as listed in PART E), covering peat and soil carbon dynamics, microbial processes, and biogeochemical modeling foundations that inform parameterization and interpretation of results.