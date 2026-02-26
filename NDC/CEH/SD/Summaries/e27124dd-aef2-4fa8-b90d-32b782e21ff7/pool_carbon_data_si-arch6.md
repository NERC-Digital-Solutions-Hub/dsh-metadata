# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- A dataset describing carbon concentrations in natural and restoration (artificial) pools across blanket peatlands in Scotland, collected between 2013 and 2015.
- Data collection methods are detailed in a companion manuscript (Hydrological Processes, 2022); data have been Quality Controlled, including treatment of values below detection limits.
- Organized into six CSV files, with site codes and sampling schemes explicitly defined.

## Data structure and files
- Pool_Carbon_Quarterly
  - Sites: CL, LL, MU
  - Description: All data from LL, CL, and MU pools amalgamated into one table
  - Contents: Quarterly measurements for each pool (e.g., pool number, treatment type NAT/ART, site, quarter, year, date/time, various chemical and physical parameters, pool dimensions)
- Pool_Carbon_Routine
  - Sites: CL only
  - Description: Routine, frequent sampling for CL pools
  - Contents: Time-stamped Series (Year, Date, Week) plus DOC, pH, EC, DO, water temperature, WTD, POC, CH4, CO2, absorbance (abs254), SUVA, E4E6, pool area/depth/volume, and related variables
- Pool_Carbon_Routine_DOC
  - Sites: CL only
  - Description: Piezo soil water DOC data at different depths
  - Contents: Year/Date/Week, Pool, Treat, Depth, DOC
- Pool_Carbon_Routine_Colour
  - Sites: CL only
  - Description: Piezo soil water colour data at different depths
  - Contents: Year/Date/Week, Pool, Treat, Depth, Abs254, E4E6, SUVA
- Pool_Carbon_Routine_Depth
  - Sites: CL only
  - Description: Pool depth below peat on sampling day (from continuous loggers)
  - Contents: Year/Date/Week, Pool, Treat, Depth below peat
- Pool_Carbon_Routine_Soil
  - Sites: CL only
  - Description: Bulked soil solution from piezometers (all depths)
  - Contents: Year/Date/Week, Pool, Treat, DOC, Abs254, E4E6, SUVA

## Key variables and units
- Common pool-level measurements (across files): pH, EC (µS/cm), DO (mg/L), Water Temp (°C), abs254 (abs/m), SUVA (l/mg/m), E4E6 (ratio), DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L), pool area (m²), pool depth (cm), pool volume (m³)
- Quarterly file adds: Year, Date, Time, Week; Quarter (autumn 2013 to autumn 2014) and specific pool identifiers
- Routine file adds: DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF, WTD (cm), plus surface-focused metrics (DOC, Abs254, E4E6, SUVA)
- DOC measurements also captured at soil depth (Depth) and bulked soil solution water for routine soil file
- All datasets include a pool/treatment descriptor: NAT = natural, ART = artificial/restoration

## Quality control and provenance
- Data are Quality Controlled; values below detection limits are treated per the referenced methodology in the main manuscript.
- Descriptions provide clear variable context, units, and measurement depth where applicable.
- The six files collectively cover both quarterly (broader aggregation) and routine (frequent, site-specific) sampling, with CL as the primary site for routine data and CL/LL/MU represented in quarterly data.

## Site and sampling design
- Geographic focus: blanket peatlands in Scotland
- Sites referenced: CL (CrossLochs), LL (Loch Lier), MU (Munsary)
- Sampling schemes:
  - Quarterly data aggregates multiple pools across sites into a single table (Pool_Carbon_Quarterly)
  - Routine data provides high-frequency measurements for CL pools
- Pool types:
  - NAT = natural pools
  - ART = artificial/restoration pools
- Depth and water source information captured via piezometer readings and depth below peat, enabling insights into interactions between water chemistry and hydrology

## Using this data for analysis and data products
- Potential analyses and products:
  - Time-series dashboards comparing NAT vs ART pools on carbon-related metrics (DOC, POC, CH4, CO2, absorbance indices)
  - Cross-file integration to relate surface water chemistry (Quarterly) with soil and piezometer data (DOC_BASE, WTD, Abs254, SUVA, E4E6)
  - Depth-resolved studies using Pool_Carbon_Routine_DOC and Pool_Carbon_Routine_Soil
  - Spatial/temporal trends across CL, LL, MU pools using the quarterly dataset
- Self-serve outputs:
  - Dashboards or pivot-table style summaries enabling end users to explore temporal trends, depth-specific chemistry, and NAT vs ART contrasts
  - Standardized charts for DOC dynamics, UV absorption indices (abs254, SUVA, E4E6), and greenhouse gas metrics (CH4, CO2)

## Access and metadata considerations
- Data are provided as six CSV files with explicit field definitions and units
- Site identifiers and temporal fields (Year, Date, Week, Quarter) support robust joins and longitudinal analyses
- Reference to the accompanying Hydrological Processes 2022 manuscript for detailed collection methods and QC procedures

## Notes for data support and stewardship
- Ensure consistent joining across quarterly and routine datasets using Pool, Treat, Year/Date/Week
- Be mindful of depth-related variables and piezometer-derived measurements when integrating soil and surface water data
- Verify units and detection-limit handling per the QC notes in the accompanying manuscript
- Consider data updates or errata from the Hydrological Processes 2022 methodology when interpreting chemical and hydrological metrics