# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' HF_NW_herbage_yield.csv '.

- Overview
  - Defines the dataset HF_NW_herbage_yield.csv: 7 columns, 96 rows, containing herbage yield data.
  - Data originate from grassland fertiliser trials conducted in 2016 at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).

- Dataset structure
  - Columns and explanations:
    - Date: Date of grass cut.
    - Site: HF or NW, indicating trial location (HF = Henfaes; NW = North Wyke).
    - N_app: 1, 2, or 3 indicating fertiliser applications; 1st & 2nd applications are 90 kg ha-1, 3rd application is 60 kg ha-1.
    - Block: 1, 2, 3, or 4; blocking factor of randomized block design.
    - Plot: 1–16; plot harvested; plot size 2 × 6 m.
    - Treatment: AN, U, IU, C; nitrogen fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea with Agrotain, C = 0N control).
    - Dry_tonnes_ha: yield in tonnes per hectare on a dry weight basis.

- Data provenance and scope
  - Ties to the 2016 grassland fertiliser trials at the two named sites; intended for use with the accompanying supporting documentation.

- Governance and stewardship notes for Data Stewards
  - Ensure clear metadata alignment: consistent site codes, N_app coding, plot numbering, and treatment abbreviations.
  - Facilitate discoverability by cataloguing with complete descriptions and linkage to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
  - Verify units and formats (Dry_tonnes_ha in tonnes per hectare, Date format, etc.).
  - Document data provenance and any intended updates or corrections to maintain an auditable data lineage.

- Suggested actions for use and updates
  - Validate definitions with data creators to confirm accuracy.
  - Maintain and share metadata alongside the dataset to support reuse and interoperability.