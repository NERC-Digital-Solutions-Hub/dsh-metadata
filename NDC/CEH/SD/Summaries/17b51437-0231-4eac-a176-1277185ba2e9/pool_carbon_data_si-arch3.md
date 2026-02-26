# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- Presents data on carbon concentrations in natural and restoration (artificial) pools in blanket peatlands in Scotland, collected during 2013–2015.
- Data collection and generation methods are described in the accompanying manuscript (Hydrological Processes 2022); data were quality controlled, including handling values below detection limits.
- Datasets are organized into six CSV files, each with detailed metadata for variables and units.

## Data collection and quality control
- Quality control applied to the data (e.g., values below detection limits addressed).
- Sampling includes both quarterly pooled data and routine, higher-frequency sampling at CL (Cross Lochs) site.
- Piezo soil water sampling is used to capture depth- and depth-related water quality metrics.

## Data files and structure
- Pool_Carbon_Quarterly (all data from LL, CL, MU pooled into one table)
  - Variables include: pool, treat (NAT = natural, ART = artificial/restoration), site (LochLier, Munsary, CrossLochs), quarter (autumn 2013 to autumn 2014), year, date, time, pH, EC, DO, water temperature, absorbance metrics (abs254, SUVA, E4E6), DOC, POC, CH4, CO2, pool area, pool depth, pool volume.
- Pool_Carbon_Routine (CL site only)
  - Routine, higher-frequency sampling with similar measurement suite as quarterly data.
- Pool_Carbon_Routine_DOC (CL site)
  - Piezo soil water DOC measurements at different depths.
- Pool_Carbon_Routine_Colour (CL site)
  - Piezo soil water color data (Abs254, E4E6, SUVA) at different depths.
- Pool_Carbon_Routine_Depth (CL site)
  - Depth below peat, as measured on sampling days.
- Pool_Carbon_Routine_Soil (CL site)
  - Bulk soil solution data (DOC, Abs254, E4E6, SUVA).

## Variables and measurements
- Core pool and site identifiers: Pool, Treat (NAT/ART), Site (CL/LL/MU).
- Temporal markers: Year, Date, Time (and Week for routine data).
- Water chemistry and optical properties (all units specified in each file): pH, EC (µS/cm), DO (mg/L), Water Temp (°C), abs254, SUVA (l/mg/m), E4E6 (ratio 465/665), DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L), pool area (m²), pool depth (cm), pool volume (m³).
- Routine-specific measurements include DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF, WTD (water table depth), and surface vs bulked soil measurements (DOC/Abs254/E4E6/SUVA) for soil solution.

## Temporal and spatial coverage
- Geographic focus: blanket peatlands in Scotland.
- Sites included: CL, LL, MU (and CL for routine data).
- Timeframe: data collected during 2013–2015, with quarterly sampling in autumn 2013 to autumn 2014 and routine high-frequency sampling at CL.

## Data governance and sharing considerations for monitoring frameworks
- Well-documented data structure with explicit units and descriptions for each variable, aiding data governance and reproducibility.
- Data are linked to a methods manuscript (Hydrological Processes 2022), indicating transparency in measurement methods.
- Potential governance considerations for monitoring frameworks:
  - Need to ensure metadata completeness and consistency across datasets when integrating quarterly and routine data.
  - Accessibility and sharing of underlying data and methods to avoid duplicative data collection and to support evidence-based decision making.
  - Importance of clearly defined site codes, sample timing, and data roll-ups (quarterly vs routine) to prevent misinterpretation in policy evaluations.

## Relevance for monitoring framework design
- Demonstrates the value of:
  - Combining quarterly snapshots with routine high-frequency sampling to capture temporal dynamics.
  - Comprehensive metadata detailing each variable, unit, and description to facilitate data reuse and governance.
  - Rigorous quality control to ensure reliability of measurements used in policy scrutiny and decision making.
  - Clear documentation of sampling methods (via linked manuscript) to support transparency and comparability across monitoring programs.
- Highlights typical barriers addressed in monitoring frameworks:
  - Complexity of integrating multiple data streams (pool-level, soil water, depth, and color metrics).
  - The need to maintain data accessibility while documenting methodological provenance.