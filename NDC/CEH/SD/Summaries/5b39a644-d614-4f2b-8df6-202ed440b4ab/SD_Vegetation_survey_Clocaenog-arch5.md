# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf' Details of data structure for 'Vegetation survey_Clocaenog.csv'

## Overview
- Describes the data structure for the Vegetation survey_Clocaenog.csv dataset as part of the Clocaenog data series documentation.
- Focuses on how the single spreadsheet is organized and how units and time are represented.

## Data structure summary
- The dataset is a single spreadsheet containing 22 columns.
- Time span covered in the dataset: Year 1998 through 2012.
- Two main data blocks:
  - Columns 1–12: plot-level plant biomass data per unit area, detailed by species over time.
    - Column 1: Year (1998–2012)
    - Column 2: Species
    - Column 3: Biomass type indicator (Total biomass vs. Living biomass)
    - Columns 4–12: Biomass measurements for experimental plots 1–9
  - Columns 13–22: plot-level total plant biomass data per unit area over time.
    - Column 13: Year (1998–2012)
    - Columns 14–22: Total biomass measurements for experimental plots 1–9
- Empty cells indicate missing data.

## Column-level details
- 1: Year (1998–2012)
- 2: Species
- 3: Biomass type (Total vs Living)
- 4–12: Biomass values per Plot 1–9 for each species over time
- 13: Year (1998–2012)
- 14–22: Total biomass values per Plot 1–9 over time

## Data quality and governance considerations for Data Stewards
- Missing data: Empty cells are used to denote data not available; plan for imputation or annotation where appropriate.
- Consistency: Ensure consistent interpretation of “Total” vs “Living” biomass across records; verify metadata for biomass type definitions.
- Metadata alignment: This sheet is a supplement to the main Clocaenog supporting documentation; include cross-references to ensure users understand context, units (per unit area), and measurement protocols.
- Provenance and lineage: Track that this structure corresponds to years 1998–2012 and link to related documentation and datasets (Vegetation survey_Clocaenog.csv) for complete understanding.
- Data sharing readiness: The organized two-block structure (species-level over time and total biomass over time) facilitates joins by Year, Species, Plot, and Biomass type; ensure portals/catalogues reflect these dimensions and provide clear field-level definitions.