# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- A dataset describing carbon concentrations and related physico-chemical properties in blanket peatland pools (natural and restoration) in Scotland from 2013 to 2015.
- Data collection and generation methods are described in a companion manuscript (Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022).
- Data were quality controlled, including handling values below detection limits.

## Data collection and quality control
- Data collection methods are documented in the accompanying manuscript.
- Quality control performed on the data, including treatment of values below detection limits.

## Data files (six CSVs)
- Pool_Carbon_Quarterly
  - Sites: CL, LL, MU (Loch Lier, Munsary, CrossLochs)
  - Description: All data from CL, LL, MU pools amalgamated into one table
  - Key content: Quarterly measurements for pool-level properties and chemistry
- Pool_Carbon_Routine
  - Sites: CL only
  - Description: Routine, more frequent sampling at CL
  - Key content: Time-series of pool chemistry and physical variables
- Pool_Carbon_Routine_DOC
  - Sites: CL only
  - Description: Piezo soil water DOC data at different depths
  - Key content: Dissolved organic carbon in soil water by depth
- Pool_Carbon_Routine_Colour
  - Sites: CL only
  - Description: Piezo soil water colour data at different depths
  - Key content: Absorbance at 254 nm (Abs254), E4/E6, SUVA for soil water
- Pool_Carbon_Routine_Depth
  - Sites: CL only
  - Description: Pool depth on sampling day (from continuous loggers)
  - Key content: Depth below peat, depth measurements
- Pool_Carbon_Routine_Soil
  - Sites: CL only
  - Description: Bulked soil solution water from piezometers
  - Key content: Soil DOC, Abs254, E4/E6, SUVA

## Variable groups and sample design (high-level)
- Pool-level water chemistry and physics (pH, electrical conductivity EC, dissolved oxygen DO, water temperature)
- Organic carbon metrics (DOC, POC, DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF)
- Carbon-related optical metrics (abs254, E4E6 ratio, SUVA)
- Gas-related measurements (CH4, CO2)
- Physical pool characteristics (Pool area, Pool depth, Pool volume)
- Water column nutrients and related indices
- Depth-related sampling data (Depth below peat; piezometer depths)
- Time markers (Year, Date, Time/Week/Quarter depending on file)

## Spatial and temporal coverage
- Spatial: Three peatland pools/sites (CL, LL, MU) with CL having routine, detailed measurements; LL and MU included in the quarterly amalgamated dataset.
- Temporal: Data spanning 2013–2015, with quarterly samples (Pool_Carbon_Quarterly) and more frequent routine sampling at CL (Pool_Carbon_Routine and derivatives).

## Usage and governance considerations for data leaders
- Comprehensive, well-documented data dictionary and column definitions accompany the six CSV files, enabling discoverability and correct interpretation.
- Data are organized by distinct data streams (quarterly amalgamated vs. routine vs. soil/solution measurements), supporting modular analysis and integration with other peatland datasets.
- Quality control applied to ensure reliability (e.g., handling detection limits) and consistency across measurements.
- Methods for data generation and collection are described in a separate manuscript, enabling reproducibility and methodological auditing.
- Clear site labeling and depth/temporal descriptors facilitate cross-site comparisons and longitudinal analyses.

## Notes for potential users
- If integrating with other datasets, align units and metadata with the provided definitions (as specified in the file descriptions).
- For soil and piezometer-related measurements, pay attention to depth-related fields and the distinction between pool water and soil solution data.
- The primary methodological reference (Hydrological Processes 2022) should be consulted for detailed sampling protocols and QC procedures.