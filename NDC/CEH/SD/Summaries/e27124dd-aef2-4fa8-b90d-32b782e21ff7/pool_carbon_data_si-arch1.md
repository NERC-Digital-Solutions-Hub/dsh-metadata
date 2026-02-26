# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- Comprehensive dataset on carbon-related chemistry in natural and restoration (artificial) pools across blanket peatlands in Scotland, collected during 2013–2015.
- Data collection and generation methods are described in the associated manuscript (Hydrological Processes, 2022). Quality control was applied (e.g., values below detection limits addressed).
- Six CSV datasets cover quarterly, routine, depth, and soil/solution measurements across multiple sites (Loch Lier, Munsary, Cross-Lochs) and treatments (NAT vs ART).

## Data structure and scope
- Sites: CL (Cross-Lochs), LL (Loch Lier), MU (Munsary).
- Treatments: NAT = natural pools; ART = artificial/restoration pools.
- Timeframe: 2013–2015, with seasonal/quarterly sampling in the quarterly data and more frequent sampling in routine datasets.
- Data types span water column chemistry, dissolved organic carbon, inorganic and organic carbon pools, absorbance indices, and physical pool characteristics.

## Dataset descriptions

- Pool_Carbon_Quarterly
  - Scope: All data from LL, CL, MU pooled into a single quarterly table.
  - Content: Pool number, treatment, site, quarterly time points (Year, Date, Time, Quarter), water chemistry (pH, EC, DO, Water Temp), optical properties (abs254, SUVA, E4E6), carbon metrics (DOC, POC, CH4, CO2), and pool physicals (Pool area, Pool depth, Pool volume).

- Pool_Carbon_Routine
  - Scope: CL site only; frequent sampling routine.
  - Content: Pool number, treatment, Year/Date/Week, DOC (base, inflow, outflow, surface, overland flow), pH, EC, DO, Water Temp, Water Table Depth (WTD), POC, CH4, CO2, absorbance (abs254), SUVA, E4E6, Pool area, Pool depth, Pool volume.

- Pool_Carbon_Routine_DOC
  - Scope: CL site only; piezometer-based soil water DOC at different depths.
  - Content: Year/Date/Week, Pool, Treatment, Depth (of sample), DOC (soil solution), plus related absorbance and UV indices as applicable.

- Pool_Carbon_Routine_Colour
  - Scope: CL site only; piezometer soil water colour data.
  - Content: Year/Date/Week, Pool, Treatment, Depth, Abs254 (soil solution colour), E4E6 (ratio), SUVA (soil water).

- Pool_Carbon_Routine_Depth
  - Scope: CL site only; depth measurements.
  - Content: Year/Date/Week, Pool, Treatment, Depth below peat (cm) – water depth below the peat surface in each pool.

- Pool_Carbon_Routine_Soil
  - Scope: CL site only; soil solution context.
  - Content: Year/Date/Week, Pool, Treatment, DOC in bulked soil solution, Abs254, E4E6, SUVA.

## Variables and units (highlights)
- Water chemistry: pH, EC (µS/cm), DO (mg/L), Water Temp (°C).
- Optical/organic indicators: abs254 (absorbance), SUVA (l/mg/m), E4E6 (ratio 465/665).
- Carbon metrics: DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L).
- Pool metrics: Pool area (m^2), Pool depth (cm), Pool volume (m^3), Water Table Depth (WTD, cm).
- Additional context: Year, Date, Week, Quarter; Pool number; Treat (NAT/ART); Depth-related measurements for soils and piezometers.

## Site design and sampling
- Natural vs restoration pools examined through a combination of quarterly and routine sampling.
- Routine data emphasize CL site with multiple depth and soil-related measurements, enabling comparisons between surface water and groundwater/soil solution.
- Data capture includes both in-pool water chemistry and soil solution parameters, providing a multi-habitat view of carbon dynamics in peatland systems.

## Quality assurance and provenance
- Data are subjected to quality control, with handling of detection-limit issues noted.
- Methods for data collection and generation are detailed in the accompanying Hydrological Processes manuscript (2022), enabling reproducibility and traceability.
- Meta-information (sample timing, site, pool, treatment) is embedded in the datasets to support reproducible analyses and cross-dataset integration.

## Potential analyses and use for data analysts
- Compare natural vs restoration pools in carbon pools (DOC, DIC components) and gas flux indicators (CH4, CO2) over time and across seasons.
- Explore relationships between DOC metrics (DOC, POC, absorbance indices) and hydrological variables (pH, EC, DO, water temperature, WTD).
- Assess how soil solution chemistry (DOC, Abs254, E4E6, SUVA) at different depths relates to in-pool chemistry and carbon cycling.
- Model seasonal and depth-specific drivers of carbon concentrations, including the influence of pool depth, volume, and area.
- Integrate quarterly and routine data to identify patterns at different spatial scales (multi-site synthesis) and timescales (short-term vs. long-term trends).

## Provenance and references
- Data collection and generation methods are documented in the manuscript: Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022.
- Data quality control steps are noted (e.g., handling of values below detection limits).