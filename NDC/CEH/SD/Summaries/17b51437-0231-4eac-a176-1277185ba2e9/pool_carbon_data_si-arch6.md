# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

- This dataset collection presents carbon concentrations in natural and restoration pools from blanket peatlands in Scotland during 2013–2015. Data collection methods and quality control are described in the associated manuscript (Hydrological Processes, 2022). All data are quality controlled, with values below detection limits noted.

## Overview of the data and purpose

- Purpose: to quantify carbon concentrations and related water chemistry across natural and restoration pools to enable analysis and interpretation of carbon dynamics in peatland systems.
- Scope: data cover both quarterly pooled datasets and routine high-frequency sampling from piezometers across selected sites.
- Sites: Loch LiER, Munsary, CrossLochs (abbreviated as LL, MU, CL in the data).

## Datasets included (six CSV files)

- Pool_Carbon_Quarterly
  - Description: All data from LL, CL, MU pools amalgamated into one table for quarterly sampling.
  - Key variables: Pool, Treat (NAT = natural, ART = artificial/restoration), Site (CL, LL, MU), Quarter (1–5), Year, Date, Time; pH, EC (µS/cm), DO (mg/L), Water Temp (°C), abs254, SUVA, E4E6, DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L), Pool area (m²), Pool depth (cm), Pool volume (m³).

- Pool_Carbon_Routine
  - Description: Routine data from CL only (frequent sampling).
  - Key variables: Pool, Treat (NAT/ART), Year, Date, Week; DOC_BASE (mg/L), DOC_INFLOW (mg/L), DOC_OUTFLOW (mg/L), DOC_SURFACE (mg/L), DOC_OLF (mg/L); pH; EC (µS/cm); DO (mg/L); Water Temp (°C); WTD (cm); POC (mg/L); CH4 (µg/L); CO2 (mg/L); abs254 (abs/m); SUVA (l/mg/m); E4E6; Pool area (m²); Pool depth (cm); Pool volume (m³).

- Pool_Carbon_Routine_DOC
  - Description: Piezo soil water DOC data at different depths (CL site).
  - Key variables: Year, Date, Week; Pool; Depth (cm); DOC (mg/L).

- Pool_Carbon_Routine_Colour
  - Description: Piezo soil water colour data at different depths (CL site).
  - Key variables: Year, Date, Week; Pool; Depth (cm); Abs254 (abs/m); E4E6; SUVA (l/mg/m).

- Pool_Carbon_Routine_Depth
  - Description: Pool depth on sampling day derived from continuous loggers (CL site).
  - Key variables: Year, Date, Week; Pool; Depth below peat (cm).

- Pool_Carbon_Routine_Soil
  - Description: Bulked soil solution from piezometers (all depths bulked into a single sample, CL site).
  - Key variables: Year, Date, Week; Pool; DOC (mg/L); Abs254 (abs/m); E4E6; SUVA (l/mg/m).

## Variables and units (high-level)

- Water chemistry and carbon metrics: pH, EC (µS/cm), DO (mg/L), Water Temp (°C), abs254 (abs/m), SUVA (l/mg/m), E4E6 (dimensionless), DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L).
- Physical pool attributes: Pool area (m²), Pool depth (cm), Pool volume (m³).
- Additional DOC measurements by depth and sample type: DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF; Soil/solution depth (Depth in cm; Depth below peat in CL-specific datasets).
- Sampling metadata: Year, Date, Time or Week, Quarter; Treat (NAT vs ART) and Site (CL/LL/MU).

## Data quality and guidance for use

- Data are quality controlled; notes indicate values below detection limits were addressed.
- The datasets are designed to enable self-service analysis and cross-dataset joins (e.g., linking routine water chemistry with quarterly pool metrics and soil/colour measurements).
- The presence of multiple related files allows researchers to analyze carbon dynamics across different compartments (water column, soil solution, and bulked soil) and across temporal scales (quarterly vs routine).

## How this data can support data use and insights

- Facilitates comparison of natural vs artificial/restoration pools regarding carbon concentrations and related water chemistry.
- Enables exploration of temporal trends across 2013–2015, including seasonal and depth-related patterns in DOC, absorbance properties, and greenhouse gas precursors.
- Supports integration with other peatland hydrology data to assess carbon fluxes, pool turnover, and effects of restoration interventions.
- Useful for building dashboards or reports that illustrate self-serve access to pool chemistry, optical properties, and soil solution metrics.