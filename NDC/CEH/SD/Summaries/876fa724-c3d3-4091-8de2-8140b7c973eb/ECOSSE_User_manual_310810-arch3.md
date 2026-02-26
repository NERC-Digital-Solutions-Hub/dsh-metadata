# D2.2 Format of Output File for Results on 20km 2 grid

- Purpose
  - Defines how results are organized and stored for each 20km2 grid cell, enabling policy-relevant monitoring of carbon change and greenhouse gas emissions across land-use changes and decadal periods.

- Scope and depth
  - Results are reported for the profile to the depth specified in line 9 of GNAMES.DAT.

- Structure (highlights)
  - Lines 1–2: Title lines.
  - Lines 3–4: ID of the 20km2 grid cell; grid coordinates (Easting, Northing).
  - Decadal results: Carbon change by land-use change (kt C per km2 per 10 years) for:
    - Decade 1 through Decade 7, including all listed LU changes (e.g., Arable to Grassland, Forestry to Arable, etc.) and projections for Decade 7 based on Decade 6 LU changes.
  - Special summaries:
    - Carbon change for all soils in the cell.
    - Carbon change for organic soils only.

- Land-use change reporting
  - Each decade presents multiple LU change pairs (e.g., Arable to Arable, Grassland to Arable, Forestry to Arable, Natural/semi-natural to Arable, Miscanthus to Arable, SRC to Arable, etc.), followed by the corresponding transitions for other target LU categories (e.g., Arable to Grassland, Grassland to Grassland, etc.).

# D2.3 Format of Output File for C Change data ('CHANGE.OUT')

- Purpose
  - Provides per-grid-cell, per-decade data on carbon changes and associated gas emissions for specified land-use changes.

- Structure (highlights)
  - For each 20km2 grid cell, results cover the profile depth indicated by GNAMES.DAT line 9.
  - Lines and fields:
    - Line 1: Title.
    - Lines 2–end: ID of the 20km2 grid cell; 2 grid coordinates; Series; Land use 1; Land use 2; Fraction of the first 1km2 cell in the 20km2 grid that changes from LU1 to LU2 in decade 5.
    - For each decade (1–7):
      - C Change (t C per ha per decade).
      - CO2 emission (t C per ha per decade).
      - CH4 emission (t C per ha per decade).
      - N2O emission (t C per ha per decade).
      - Total greenhouse gas emission in CO2 equivalents (t C per ha per decade).
      - Carbon content of soil at start (percent C).
      - Clay content (percent clay).
      - Error in simulation? (0 = No; 1 = Yes).

# D2.4 Format of Climate Change Results file

- Purpose
  - Reports climate-change-related results on a 1km2 grid, enabling assessment of climate-driven changes across scales and decades.

- Structure (highlights)
  - For each 1km2 grid cell, results cover the profile depth specified by GNAMES.DAT line 9.
  - Lines:
    - Line 1: Title.
    - Decade 2–7 sections (and Decade 1 details listed under Decade 1 as applicable).
    - Lines 2–end: ID of the 20km2 grid cell; Easting; Northing; Carbon change per land use (t C per km2 per 10 years).
    - Decade entries:
      - Decade 1: Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC.
      - Decades 2–7: same LU categories, with changes driven by climate-change scenarios.

# D2.5 Format of File for Calculation of Effects of Different Mitigation Options

- Purpose
  - Captures outputs when evaluating mitigation options, on a per-1km2 basis to assess potential reductions or shifts in land use.

- Structure (highlights)
  - For each 1km2 grid cell, results cover the profile depth indicated by GNAMES.DAT line 9.
  - Lines:
    - Lines 1–2: Title lines.
    - Lines 3–end: ID of the 20km2 grid cell; coordinate grid (Easting, Northing); Dominant soil series (1–5); Wetness class; Percentage C in top soil layer; Percentage clay in top soil layer; Fraction of the 1km2 cell with a given land use (km2 per km2).
    - Decade 1–7: Carbon change associated with LU change applied in the first decade (t C per ha per decade).

- Notes
  - All outputs reference the depth specified in GNAMES.DAT line 9 and include spatial context (grid IDs and coordinates) to support aggregation, visualization, and policy evaluation.

# PART E – REFERENCES

- Content
  - Provides sources underpinning the model and processes (e.g., peat soil carbon dynamics, microbial activity, nitrogen turnover, and methane/CO2/N2O flux modelling) to support the methodology and parameterization used in the output formats above.