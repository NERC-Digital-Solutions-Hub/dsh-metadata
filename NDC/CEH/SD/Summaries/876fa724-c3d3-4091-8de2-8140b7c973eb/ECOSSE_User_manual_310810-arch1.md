# Model to Estimate Carbon in Organic Soils - Sequestration and Emissions (ECOSSE). User-Manual

## Overview of the sections (as reflected in the provided text)
- The outputs are structured to show carbon changes and greenhouse gas emissions under land-use change scenarios across spatial grids and decades.
- Results include total soil carbon changes, organic-soil–specific changes, and full GHG emissions (CO2, CH4, N2O) with CO2-equivalent totals.
- Seven decades are presented, with decade 7 using LU-change projections based on decade 6. Transitions among multiple land-use types are enumerated (e.g., Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC).

## D2. Output formats by grid and decade
- D2.2 Format of Output File for Results on 20km^2 grid
  - For each 20 km^2 grid cell:
    - Includes cell identifiers, easting/northing, and carbon change per land-use change (kt C km^-2 per 10 years) for each decade.
    - Lists decadal results for various land-use transitions (e.g., Arable to Arable, Grassland to Arable, Forestry to Arable, Natural/semi-natural to Arable, Miscanthus to Arable, SRC to Arable, and other combinations such as Arable to Grassland, Grassland to Grassland, etc.).
    - Separate sections show carbon change for all soils, carbon change for organic soils only, and CO2/CH4/N2O emissions alongside total greenhouse gas (GHG) emissions in CO2 equivalents. 
    - Decade labels included: Decade 1 through Decade 7 (with Decade 7 described as LU-change projections using decade 6).
- D2.3 Format of Output File for C Change data ('CHANGE.OUT')
  - For each 20 km^2 grid cell:
    - Includes: series, Land use 1, Land use 2, and fraction of the first 1 km^2 cell changing from LU1 to LU2 in decade 5.
    - For each decade (1–7): C Change (t C/ha/decade), CO2 emission (t C/ha/decade), CH4 emission (t C/ha/decade), N2O emission (t N/ha/decade), Total GHG emission in CO2 equivalents (t C/ha/decade), soil C content at start (%C), clay content (% clay), and an error flag (0=No; 1=Yes).
- D2.4 Format of Climate Change Results file
  - For each 1 km^2 grid cell:
    - Results are organized per decade (Decade 2–7) and show the Land Use combinations for each 20 km^2 parent cell.
    - Output lines include: ID of 20 km grid, easting, northing, and carbon change per land-use change (t C km^-2 per 10 years) for each decade, with the same LU-pair labeling as in D2.2 (e.g., Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC).
- D2.5 Format of File for Calculation of Effects of Different Mitigation Options (files named MIT_A2P.OUT, etc.)
  - For each 1 km^2 grid cell:
    - Includes: title lines, 20 km grid ID, cell coordinates, dominant soil series (1–5), wetness class, %C in top soil layer, % clay in top soil layer, and the fraction of the 1 km^2 cell that has this land use.
    - Decades 1–7: Carbon change associated with LU change applied in the first decade (t C/ha/km^2/decade).

## Decadal structure and land-use transitions
- Decade structure
  - Seven decades of results (Decade 1 to Decade 7).
  - Decade 7 uses LU-change projections based on decade 6.
- Land-use transitions (examples shown)
  - Transitions include Arable to Arable, Grassland to Arable, Forestry to Arable, Natural/semi-natural to Arable, Miscanthus to Arable, SRC to Arable, and similarly for other LU pairs (e.g., Arable to Grassland, Grassland to Grassland, etc.).
  - Climate-change results and mitigation-option files provide parallel LU-transition frameworks for assessment.

## Key variables and metrics
- C change metrics
  - Carbon change per land-use change (kt C km^-2 per 10 years) across decades and LU pairs.
  - Carbon change data are provided for all soils and for organic soils only.
- Greenhouse gas emissions
  - CO2 emissions (kt C km^-2 per 10 years)
  - CH4 emissions (kt C km^-2 per 10 years)
  - N2O emissions (kt N km^-2 per 10 years)
  - Total GHG emissions in CO2 equivalents (kt C km^-2 per 10 years)
- Soil and site properties
  - Carbon content at start (% C)
  - Clay content (% clay)
- Data quality
  - An error flag is included in CHANGE.OUT to indicate potential simulation issues.

## Grid scales and data integration
- Spatial scales
  - Results are provided for both 20 km^2 grid cells (D2.2, D2.3) and 1 km^2 grid cells (D2.4, D2.5), enabling national-scale inventories and finer spatial analyses.
- Data dependencies
  - Outputs are linked to input/support files (e.g., GNAMES.DAT, management data, soil parameters) and align with LU and weather datasets to support scenario analyses.

## Practical implications for analysts
- Use cases
  - Inform national GHG inventories and land-use policy by projecting soil C stock changes and a full suite of GHG fluxes under different LU scenarios and climate inputs.
- Data requirements
  - Requires consistent LU, soil, management, and weather inputs formatted to ECOSSE’s file structures (including management, GNAMES, D1–D2 blocks).
- Interpretation notes
  - Decadal projections assume LU-change trajectories and may involve LU-change fractions at grid scales; mitigation-option outputs allow comparison of different management scenarios.
- Limitations and validation
  - Some results may rely on inferred rate modifiers where data are sparse; validation status is ongoing for several modules (as noted in the broader manual).

## References and underpinning literature
- The document aggregates extensive references on peat and soil carbon dynamics, dissolved organic carbon, microbial activity, nitrogen cycling, methane fluxes, and RothC-based decomposition concepts, underscoring the empirical basis for ECOSSE parameterizations and processes.