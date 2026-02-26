# D2.2 Format of Output File for Results on 20km 2 grid

- Purpose: Defines how model results are formatted for each 20 km² grid cell, with depth determined by line 9 of GNAMES.DAT.
- Depth specification: Outputs are profile-based up to the depth specified, enabling depth-dependent analyses.

- File structure:
  - Lines 1–2: Title lines
  - Lines 3–end: ID of the 20 km² grid cell, grid coordinates (Easting, Northing), and carbon change per land-use change (kt C km⁻² per 10 years)
  - Decade sections (Decade 1, Decade 2, … Decade 7):
    - Lists of land-use change pairs (e.g., Arable to Arable, Grassland to Arable, Forestry to Arable, Natural/semi-natural to Arable, Miscanthus to Arable, SRC to Arable, etc.)
    - Decade-specific transitions for all LU combinations (Decade 2–7 follow the same pattern)
    - Note: Decade 7 may reflect LU change projections using decade 6
  - Carbon change summaries:
    - Carbon change for all soils in the cell (kt C km⁻² per 10 years) across Decades 1–7
    - Carbon change for organic soils in the cell only (kt C km⁻² per 10 years) across Decades 1–7

- Outputs included:
  - Net carbon change by land-use change per decade
  - Grid-level context for all soils and (separately) organic soils

---

# D2.3 Format of Output File for C Change data ('CHANGE.OUT')

- Purpose: Provides carbon-change and greenhouse gas emission details at the grid level for LU transitions.
- File structure:
  - Lines 1: Title line
  - Lines 2–end: ID of the 20 km² grid and a 2-grid representation of the cell (including Easting and Northing)
  - Series; Land use 1; Land use 2
  - Fraction of the first 1 km² cell in the 20 km² grid changing from LU1 to LU2 in decade 5 (placeholder in the text)
  - For each decade (1–7):
    - C Change (t C ha⁻¹ per decade)
    - CO2 emission (t C ha⁻¹ per decade)
    - CH4 emission (t C ha⁻¹ per decade)
    - N2O emission (t C ha⁻¹ per decade)
    - Total GHG emission in CO2 equivalents (t C ha⁻¹ per decade)
    - Carbon content of soil at start (%C)
    - Clay content (% clay)
    - Error in simulation? (0 = No; 1 = Yes)

- Notes:
  - Designed to summarize C changes and full GHG indicators by LU transitions and decades
  - Includes soil properties metadata (initial carbon content, clay content)
  - Includes a flag for potential simulation errors

---

# D2.4 Format of Climate Change Results file

- Purpose: Presents climate-related scenario results at a finer 1 km² grid resolution.
- File structure:
  - Line 1: Title line
  - Decades 2–7: Headers (e.g., Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC)
  - Lines 2–end: ID of 20 km grid, Easting, Northing
  - Carbon change per land use (t C km⁻² per 10 years) for each decade
  - For Decade 1: listing of land-use categories
  - Decades 2–7: similar structure, showing LU-specific carbon changes across time

- Notes:
  - Enables assessment of carbon changes under climate scenarios at finer spatial detail
  - Aligns with GNAMES.DAT depth specification for depth-consistent outputs

---

# D2.5 Format of File for Calculation of Effects of Different Mitigation Options (files named MIT_A2P.OUT etc)

- Purpose: Captures mitigation-option analyses for LU changes and soil responses.
- File structure:
  - For each 1 km² grid cell:
    - Lines 1–2: Title lines
    - Lines 3–end: ID of the 20 km grid, Easting, Northing
    - Dominant soil series (1–5) and Wetness class
    - % C in the top soil layer
    - % clay in the top soil layer
    - Fraction of the 1 km² cell that has this land use (km²/km²)
    - Decades 1–7: Carbon change associated with LU change applied in the first decade (t C ha⁻¹ km⁻² per decade)

- Notes:
  - Supports comparison and quantification of mitigation options across the grid
  - Includes soil and top-layer properties to contextualize mitigation effects

---

# PART E - REFERENCES

- Contains a bibliography of supporting literature for peat, soil carbon dynamics, microbial processes, nitrogen cycling, and related modeling foundations
- Indicates the empirical and theoretical basis for model processes and assumptions

---

# Practical Takeaways for Data Leaders

- Standardized, grid-based outputs:
  - Outputs are organized by 20 km² cells (and 1 km² in climate-change results), enabling scalable, policy-relevant analyses.
- Depth-consistent reporting:
  - Depth coverage is controlled by GNAMES.DAT line 9, ensuring comparability across datasets and scenarios.
- Rich metadata and provenance needs:
  - Outputs include soil properties (carbon content, clay content), land-use transitions, and LU fractions, underscoring the need for robust metadata and source tracking.
- Multi-faceted data products:
  - D2.2 and D2.3 provide LU-change-centric carbon and GHGI results; D2.4 adds climate-change context at finer resolution; D2.5 enables evaluation of mitigation options.
- Data governance implications:
  - Clear file formats, consistent grid IDs, and documented assumptions are essential for reproducibility.
  - Include error flags (as in D2.3) to communicate simulation reliability.
  - Versioning and traceability are important, given multiple decades and LU-transition scenarios.
- Usability in GIS and policy:
  - Outputs are designed for integration with GIS, inventories, and policy reports, supporting decadal trend analyses and scenario planning.
- Data quality considerations:
  - The outputs rely on accurate GNAMES.DAT definitions, LU histories, soil properties, and input climate data; gaps should be managed with documented defaults and spin-up strategies.