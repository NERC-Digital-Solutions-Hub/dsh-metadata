# D2.2 Format of Output File for Results on 20km 2 grid

- Overview: For each 20km 2 grid cell, results are given for the profile to the depth specified in line 9 of GNAMES.DAT.

- File structure (Lines 1–2): Title lines.

- Content (Lines 3 to end): 
  - ID of 20km 2 grid containing the cell, Easting, Northing.
  - Carbon change per land use change (kt C km -2 10years -1).
  - Decade 1, with multiple land-use change pairs, for example:
    - Arable to arable
    - Grassland to arable
    - Forestry to arable
    - Natural/semi-natural to arable
    - Miscanthus to arable
    - SRC to arable
    - Arable to grassland, Grassland to grassland, Forestry to grassland, Miscanthus to grassland, SRC to grassland
    - Natural/semi-natural to grassland
    - Arable to forestry, Grassland to forestry, Forestry to forestry, Natural/semi-natural to forestry, Miscanthus to forestry, SRC to forestry
    - Arable to natural/semi-natural, Grassland to natural/semi-natural, Forestry to natural/semi-natural, Natural/semi-natural to natural/semi-natural, Miscanthus to natural/semi-natural, SRC to natural/semi-natural
    - Arable to miscanthus, Grassland to miscanthus, Forestry to miscanthus, Natural/semi-natural to miscanthus, Miscanthus to miscanthus, SRC to miscanthus
    - Arable to SRC, Grassland to SRC, Forestry to SRC, Natural/semi-natural to SRC, Miscanthus to SRC, SRC to SRC
  - Decade 2, 3, 4, 5, 6, 7 sections (each with LU change pairs as above, including “Decade 7 (LU change projections using decade 6)”).
  - Carbon change for all soils in the cell (kt C km -2 10years -1) across Decades 1–7.
  - Carbon change for organic soils in the cell only (kt C km -2 10years -1) across Decades 1–7.

---

# D2.3 Format of Output File for C Change data ('CHANGE.OUT')

- Overview: For each 20km 2 grid cell, results are given for the profile to the depth specified in line 9 of GNAMES.DAT.

- File structure (Lines 1–1): Title line.

- Content (Lines 2 to end):
  - ID of 20km 2 grid cell, 2 grid containing the cell, Series, Land use 1, Land use 2.
  - Fraction of the first 1km 2 cell in the 20km 2 grid that changes from LU1 to LU2 in decade 5 (placeholder text “(??)” indicates a decade-specific fraction).
  - For each decade (1–7):
    - C Change (t C / ha / decade)
    - CO2 emission (t C / ha / decade)
    - CH4 emission (t C / ha / decade)
    - N2O emission (t C / ha / decade)
    - Total GHG emission in CO2 equivalents (t C / ha / decade)
    - Carbon content of soil at start (%C)
    - Clay content (% clay)
    - Error in simulation? (0 = No; 1 = Yes)

---

# D2.4 Format of Climate Change Results file

- Overview: For each 1km 2 grid cell, results are given for the profile to the depth specified in line 9 of GNAMES.DAT.

- File structure (Line 1): Title line.

- Content (Decade sections 2–7):
  - Decade 2–7 header: Arable…
  - ID of 20km grid containing the cell, Easting, Northing.
  - Carbon change per land use (t C km -2 10years -1).
  - Decade 1: Land-use categories (Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC).
  - Decade 2–7: Corresponding land-use change results.

---

# D2.5 Format of File for Calculation of Effects of Different Mitigation Options (files named MIT_A2P.OUT etc)

- Overview: For each 1km 2 grid cell, results are given for the profile to the depth specified in line 9 of GNAMES.DAT.

- File structure (Lines 1–2): Title lines.

- Content (Lines 3 to end):
  - ID of 20km grid cell, 2 grid containing the cell, Easting, Northing.
  - Dominant soil series (1–5), Wetness class.
  - % C in top soil layer, % clay in top soil layer.
  - Fraction of 1km 2 cell that has this land use (km 2 / km 2).
  - Decade 1–7.
  - Carbon change associated with LU change applied in the first decade (t C / ha / km 2 / decade).

---

# PART E - REFERENCES

- The document includes references related to peat and soil carbon, microbial processes, and related GIS and modeling sources (e.g., RothC/ECOSSE models, methane dynamics, nitrogen turnover, etc.).