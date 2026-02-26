# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- A data-rich study documenting carbon concentrations in natural and restoration (artificial) pools across blanket peatlands in Scotland over 2013–2015.
- Data were quality controlled (e.g., values below detection limits addressed) and are described in the accompanying manuscript: Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022.
- Data are organized into six CSV files, with separate datasets for quarterly composites, routine high-frequency sampling, and depth/soil-related measurements.

## Datasets included
- Pool_Carbon_Quarterly
  - All data from LL, CL, MU pools amalgamated into one table.
  - Variables include: pool, treat (NAT = natural; ART = artificial/restoration), site (LochLier, Munsary, CrossLochs), Quarter, Year, Date, Time, pH, EC (µS/cm), DO (mg/L), Water Temp (°C), abs254, SUVA, E4E6, DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L), pool area (m²), pool depth (cm), pool volume (m³).

- Pool_Carbon_Routine
  - CL site only; high-frequency routine sampling.
  - Includes standard water chemistry (pH, EC, DO, water temperature), DOC-related metrics, POC, CH4, CO2, absorbance metrics (abs254, SUVA, E4E6), and pool geometry (area, depth, volume). Also includes DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF, and Water Table Depth (WTD).

- Pool_Carbon_Routine_DOC
  - CL site only; depth-specific data for soil-related DOC.
  - Depth, Pool, Treat, and DOC (mg/L).

- Pool_Carbon_Routine_Colour
  - CL site only; colour and light-absorption metrics for soil solution.
  - Depth, Pool, Treat, Abs254 (abs/m), E4E6, SUVA.

- Pool_Carbon_Routine_Depth
  - CL site only; depth below peat measurements.
  - Depth below peat, Pool, Treat, and related sampling timing (Year/Date/Week).

- Pool_Carbon_Routine_Soil
  - CL site only; soil solution measurements.
  - DOC (mg/L), Abs254 (abs/m), E4E6, SUVA for bulked soil solution water.

## Key variables and units
- Water chemistry: pH; EC (µS/cm); DO (mg/L); Water Temp (°C); abs254 (abs/m); SUVA (l/mg/m); E4E6 (dimensionless).
- Carbon metrics: DOC (mg/L); POC (mg/L); CH4 (µg/L); CO2 (mg/L); DOC fractions in routine and soil datasets.
- Hydrology and geometry: Pool area (m²); Pool depth (cm); Pool volume (m³); WTD (cm); Depth below peat (cm).
- Sampling design: Year, Date, Week; Quarter (autumn 2013, winter 2013/2014, spring 2014, summer 2014, autumn 2014); Pool/treatments (NAT vs ART); Site identifiers (LochLier, Munsary, CrossLochs).

## Study design and scope
- Sites: LL, CL, MU corresponding to LochLier, CrossLochs, Munsary.
- Pool types: NAT (natural) vs ART (artificial/restoration) pools.
- Temporal coverage: 2013–2015 with quarterly sampling for aggregated data; frequent routine sampling within CL site for more detailed temporal resolution.
- Data focus: Carbon concentrations and related water chemistry across pool water, surface and soil solutions, and within-situ depth measurements.

## Data quality and provenance
- Data collection and generation methods are described in the associated manuscript (Hydrological Processes, 2022).
- Quality control applied to the dataset (e.g., handling values below detection limits) to ensure reliability of the measurements.
- Datasets are designed for integration and comparison across sites, pool types, and time, with explicit metadata for each variable.

## How to use the data (analytical ideas)
- Compare carbon concentrations and related chemistry between NAT and ART pools to assess restoration impact on carbon dynamics.
- Examine temporal trends across seasons (quarters) and between years for DOC, DOC fractions, and colour metrics (abs254, SUVA, E4E6).
- Explore relationships between DOC metrics and hydrological variables (WTD, pool depth, pool volume) and gas emissions (CH4, CO2).
- Analyze routine high-frequency data (Pool_Carbon_Routine) to identify short-term responses to hydrological changes or restoration interventions.
- Investigate depth- and soil-associated carbon processes using Pool_Carbon_Routine_DOC, Pool_Carbon_Routine_Colour, Pool_Carbon_Routine_Depth, and Pool_Carbon_Routine_Soil datasets.

## Considerations for analysts
- Data integration challenges across six files with multiple site-specific variables; CL is the focus for routine datasets.
- Local-scale measurements and depth-dependent data require careful alignment by pool, site, and sampling date.
- Potential data gaps or irregular sampling should be accounted for in models (e.g., mixed-effects approaches with site as a random effect).
- The datasets provide rich chemical and optical proxies (abs254, SUVA, E4E6) alongside direct carbon measures (DOC, POC, CH4, CO2) suitable for multivariate analyses.

## Access and references
- Primary methods and data collection details are described in the manuscript: Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022.
- Data files are provided as six CSVs with accompanying variable dictionaries and descriptions embedded in the file headers.