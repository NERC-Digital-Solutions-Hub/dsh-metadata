# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- A dataset describing carbon concentrations and related water chemistry in natural and restoration (artificial) pools across blanket peatlands in Scotland, collected in 2013–2015.
- Data have undergone quality control (e.g., values below detection limits removed or flagged).
- Data collection methods are described in the referenced manuscript (Hydrological Processes, 2022).

## Data structure and files
- Data are provided as six CSV files, covering different sampling regimes and data types:
  - Pool_Carbon_Quarterly (Sites: CL, LL, MU)
    - Amalgamated data from LL, CL, MU pools into one table.
    - Variables include pool, treat (NAT = natural, ART = artificial/restoration), site (LochLier, Munsary, CrossLochs), quarter, year, date/time, and a suite of chemical and physical measurements (pH, EC, DO, water temperature, absorbance metrics such as abs254, SUVA, E4E6, DOC, POC, CH4, CO2), pool physicals (area, depth, volume), etc.
  - Pool_Carbon_Routine (Sites: CL only)
    - Frequent routine sampling in CL pools.
    - Variables include Year/Date/Week and DOC fractions (DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF), pH, EC, DO, Water Temp, Water Table Depth (WTD), POC, CH4, CO2, absorbance metrics (abs254, SUVA, E4E6), pool physicals (area, depth, volume).
  - Pool_Carbon_Routine_DOC (Sites: CL only)
    - DOC in soil solution at depth; depth-specific samples.
    - Variables: Year/Date/Week, Pool, Depth, and DOC measurements.
  - Pool_Carbon_Routine_Colour (Sites: CL only)
    - Colour-related measurements in soil solution water at depth.
    - Variables: Year/Date/Week, Pool, Depth, Abs254, E4E6, SUVA.
  - Pool_Carbon_Routine_Depth (Sites: CL only)
    - Depth below peat measured during sampling.
    - Variables: Year/Date/Week, Pool, Depth below peat.
  - Pool_Carbon_Routine_Soil (Sites: CL only)
    - Bulked soil solution data from piezometers (all depths combined).
    - Variables: Year/Date/Week, Pool, DOC, Abs254, E4E6, SUVA.
- Sites referenced include Loch Lier (LL), CrossLochs (CL), and Munsary (MU).
- Depth-related and piezometer-related measurements are included in routine datasets.

## Key variables and data types
- Chemical/optical measurements: pH, electrical conductivity (EC), dissolved oxygen (DO), water temperature, abs254, SUVA, E4E6, DOC, POC, CH4, CO2.
- Physical parameters: pool area (m2), pool depth (cm), pool volume (m3), water table depth (WTD).
- Organic carbon pools: DOC, POC, and related fractions in various streamflow paths (inflow, outflow, surface, overland flow).
- Temporal scope: Year, Date, Week (and in quarterly data, Quarter and specific seasonal periods within 2013–2015).
- Data quality: Quality controlled with explicit handling of detection-limit issues.

## Quality, provenance, and governance
- Data collection methods are described in the associated manuscript (Hydrological Processes, 2022).
- Values below detection limits are quality controlled (treated appropriately in the dataset).
- Rich metadata per file and per variable facilitate discoverability and reuse.
- Data are organized to support integration across natural vs restoration pools and across sites, enabling cross-site comparisons and system-wide analyses.

## Potential uses for Data Leaders
- Assess carbon dynamics across natural and restoration peatland pools and evaluate restoration effectiveness.
- Compare chemical and optical indicators (DOC, POC, absorbance metrics) across sites and time (quarterly vs routine sampling).
- Identify data gaps and inform future data collection needs (e.g., standardizing depth-related measurements or expanding site coverage).
- Support data-driven policy or management discussions by providing a coherent dataset with clear provenance and measurement definitions.
- Integrate with wider peatland data networks to strengthen community data practices and collaborative analyses.

## Access, metadata, and integration considerations
- Dataset is organized into six CSV files with explicit variable descriptions, aiding discoverability and correct interpretation.
- Users should align units and definitions across files (e.g., DOC in mg/l, absorbance units) when merging data.
- The inclusion of both quarterly and routine datasets allows analyses at multiple temporal resolutions but may require careful alignment of sampling dates and quarter labels.
- For data leaders, consider establishing a shared data dictionary and data governance practices to maintain consistency if extending or linking with additional datasets.

## Endnotes
- The document outlines a comprehensive, QC-filtered dataset on carbon concentrations and related water chemistry in blanket peatland pools, suitable for system-wide analysis and cross-site comparisons, with clear documentation to support data stewardship and reuse.