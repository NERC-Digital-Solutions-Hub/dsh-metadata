# Model to Estimate Carbon in Organic Soils - Sequestration and Emissions (ECOSSE)

- The ECOSSE documentation defines structured output formats across grid scales for reporting carbon changes and greenhouse gas emissions under different land-use scenarios and climate conditions.
- Outputs are depth-specific (to the depth in GNAMES.DAT line 9) and are intended for inventories, policy analysis, and scenario comparison.

## D2.2 Format of Output File for Results on 20km2 Grid

- For each 20km2 grid cell, results are provided for the profile to the depth specified in GNAMES.DAT line 9.
- File structure:
  - Lines 1–2: Title lines
  - Line 3 onward: ID of 20km2 grid cell, Easting, Northing
  - Carbon change per land-use change (kt C km-2 10years-1)
  - Decade 1: listing of multiple land-use change pairs (e.g., Arable to arable, Grassland to arable, Forestry to arable, Natural/semi-natural to arable, Miscanthus to arable, SRC to arable) and similar pairings for Decade 1
  - Decade 2 to Decade 7: similar LU-change listings (e.g., Arable to grassland, Grassland to grassland, etc.), with Decade 7 noted as “LU change projections using decade 6”
  - Carbon change for all soils in the cell (kt C km-2 10years-1) by decade (Decade 1–Decade 7)
  - Carbon change for organic soils in the cell only (kt C km-2 10years-1) by decade (Decade 1–Decade 7)

## D2.3 Format of Output File for C Change data ('CHANGE.OUT')

- For each 20km2 grid cell, results are provided for the profile to the depth in GNAMES.DAT line 9.
- File structure:
  - Line 1: Title line
  - Lines 2–end: 20km2 grid identifier; Easting; Northing
  - Series; Land use 1; Land use 2
  - Fraction of the first 1km2 cell in the 20km2 grid that changes from LU1 to LU2 in decade 5 (illustrative placeholder in the format)
  - For each decade (1–7):
    - C Change (t C/ha/decade)
    - CO2 emission (t C/ha/decade)
    - CH4 emission (t C/ha/decade)
    - N2O emission (t C/ha/decade)
    - Total GHG emission in CO2 equivalents (t C/ha/decade)
    - Carbon content of soil at start (%C)
    - Clay content (% clay)
    - Error in simulation? (0=No; 1=Yes)

## D2.4 Format of Climate Change Results file

- For each 1km2 grid cell, results are provided for the profile to the depth in GNAMES.DAT line 9.
- File structure:
  - Line 1: Title line
  - Decade 2–7: header line (e.g., Arable…)
  - Lines 2–end: ID of 20km grid; Easting; Northing
  - Carbon change per land use (t C km-2 10years-1)
  - Decade 1: listed land-use categories (Arable, Grassland, Forestry, Natural/semi-natural, Miscanthus, SRC)
  - Decade 2–7: corresponding results for subsequent decades

## D2.5 Format of File for Calculation of Effects of Different Mitigation Options (files named MIT_A2P.OUT, etc.)

- For each 1km2 grid cell, results are provided for the profile to the depth in GNAMES.DAT line 9.
- File structure:
  - Lines 1–2: Title lines
  - Lines 3–end: ID of 20km grid; Easting; Northing
  - Dominant soil series (1–5)
  - Wetness class
  - % C in top soil layer
  - % clay in top soil layer
  - Fraction of the 1km2 cell that has this land use (km2/km2)
  - Decade 1–7: carbon change associated with LU change applied in the first decade (t C/ha/km2/decade)

## Data Governance and Stewardship Implications for Data Stewards

- Provenance and traceability:
  - Ensure alignment between GNAMES.DAT specifications (e.g., depth line) and output depth.
  - Track the lineage of grid-cell results from input LU changes through to decade-by-decade outputs.
- Metadata and units:
  - Maintain clear metadata for all fields (e.g., kt C km-2 10years-1, t C/ha/decade, %C, % clay) and the exact LU change labels used.
- Versioning and reproducibility:
  - Preserve and document model version, parameter sets, and any site-specific calibrations used to generate outputs.
  - Capture the mapping between LU change scenarios and decades (including the note that Decade 7 projections use Decade 6 as input).
- Data quality and limitations:
  - Note that results depend on depth specification, grid-scale aggregation, and the accuracy of LU-change assumptions; document any gaps or assumptions.
- Privacy, licensing, and data reuse:
  - Manage licensing for input data and ensure proper attribution when outputs are reused in inventories or policy analyses.
- Interoperability and integration:
  - Outputs are designed for GIS-scale integration; ensure consistent coordinate references, grid definitions, and file naming to enable integration with inventories and policy tools.

## References (PART E)

- The output format references and the overall ECOSSE framework draw on a broad set of literature related to soil carbon and gaseous emissions, supporting the process-based reporting of carbon dynamics and GHG emissions across land-use changes.