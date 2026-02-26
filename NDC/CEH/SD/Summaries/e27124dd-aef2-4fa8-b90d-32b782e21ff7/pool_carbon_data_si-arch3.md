# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- A study of carbon concentrations in natural and restoration pools across blanket peatlands in Scotland during 2013–2015.
- Data collection and generation methods are described in the accompanying manuscript (Hydrological Processes, 2022).
- Data undergo quality control (e.g., handling values below detection limits).

## Data structure and contents
- Six CSV files comprising the full dataset:
  - Pool_Carbon_Quarterly (sites: CL, LL, MU) – amalgamated quarterly pool data across sites.
  - Pool_Carbon_Routine (sites: CL) – routine, frequent sampling data for CL.
  - Pool_Carbon_Routine_DOC (sites: CL) – piezo soil water dissolved organic carbon (DOC) data at different depths.
  - Pool_Carbon_Routine_Colour (sites: CL) – piezo soil water colour data at different depths.
  - Pool_Carbon_Routine_Depth (sites: CL) – pool sampling day depth data from continuous loggers.
  - Pool_Carbon_Routine_Soil (sites: CL) – bulked soil solution carbon data.
- Each file includes detailed metadata for columns, with explicit units and descriptions.

## Measurements and key variables
- Quarterly data (Pool_Carbon_Quarterly): pool number, treatment type (NAT = natural, ART = artificial/restoration), site (LochLier, Munsary, CrossLochs), time points (Year, Date, Time, Quarter), and a range of water chemistry and physics parameters.
- Core water chemistry and carbon indicators:
  - pH, electrical conductivity (EC in µS/cm), dissolved oxygen (DO in mg/l), water temperature (°C).
  - Absorbance at 254 nm (abs254), Specific UV absorbance (SUVA, l/mg/m), E4E6 ratio (465/665).
  - Dissolved organic carbon (DOC in mg/l), Particulate organic carbon (POC, mg/l).
  - Methane (CH4, µg/l) and carbon dioxide (CO2, mg/l).
  - Additional pool metrics: pool area (m2), pool depth (cm), pool volume (m3).
- Routine data (Pool_Carbon_Routine):
  - DOC components: DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF (all mg/l).
  - Water chemistry and physical variables: pH, EC, DO, Water Temp, WTD (water table depth, cm).
  - Carbon and absorption metrics: POC, CH4, CO2, abs254, SUVA, E4E6 for pool surface water or bulked solutions.
  - Depths and volumes continue to be tracked (Pool area, Pool depth, Pool volume).
- DOC and soil-focused data (Pool_Carbon_Routine_DOC, Pool_Carbon_Routine_Soil):
  - DOC measurements in soil solution and related optical properties (abs254, E4E6, SUVA) for soil contexts.
  - Depth-related sampling details for soil and peat-associated measurements.

## Site, sampling and data quality details
- Sites mentioned: CL (and nearby sites LL, MU for quarterly amalgamation in Pool_Carbon_Quarterly).
- Sampling framework includes natural vs artificial/restoration pool classifications (NAT vs ART) and a quarterly rotation across seasons.
- Depth and continuous monitoring: depth measurements from piezometers and continuous loggers; piezometer-based sampling describes depth context in the peat.
- Quality control: explicit note that data were quality controlled, with handling of values below detection limits.

## Metadata, data governance and accessibility
- Each dataset/file provides comprehensive metadata definitions for every column (units, descriptions).
- Documentation references accompanying methods for data generation (as described in the related Hydrological Processes manuscript).
- Data are structured to support reuse in monitoring frameworks, enabling clear traceability of measurements across time, site, pool type, and depth.

## Relevance for monitoring frameworks
- Provides a time-series, multi-parameter dataset essential for assessing carbon dynamics in peatland pools under natural and restoration conditions.
- Includes both water-column and soil/piezometer contexts, allowing integrated analysis of carbon transport, processing, and storage.
- Rich metadata and standardized units facilitate synthesis, benchmarking, and governance-aligned data sharing in monitoring programs.
- Suitable for informing policy decisions, evaluating restoration outcomes, and guiding future monitoring designs in peatland ecosystems.