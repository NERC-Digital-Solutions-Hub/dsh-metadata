# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

- Overview
  - A dataset describing carbon concentrations in natural and restoration (artificial) pools in blanket peatlands of Scotland, collected from 2013 to 2015.
  - Data collection methods are described in the associated manuscript (Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022).
  - Data have undergone quality control (e.g., values below detection limits were addressed) and are provided as six CSV files.

- Datasets and structure
  - Pool_Carbon_Quarterly
    - All data from LL, CL, and MU pooled into one table.
  - Pool_Carbon_Routine
    - All routine data from CL (Cross Lochs) only.
  - Pool_Carbon_Routine_DOC
    - Piezo soil water dissolved organic carbon data at different depths (CL).
  - Pool_Carbon_Routine_Colour
    - Piezo soil water colour data at different depths (CL).
  - Pool_Carbon_Routine_Depth
    - Pool depth on sampling day from continuous loggers (CL).
  - Pool_Carbon_Routine_Soil
    - Bulked soil solution DOC data (CL).

- Sites and sampling context
  - Sites: CL (CrossLochs), LL (Loch Lier), MU (Munsary).
  - Sampling includes both natural pools (NAT) and artificial/restoration pools (ART).
  - Quarterly data span autumn 2013 to autumn 2014, with multiple measurements within pools.

- Key variables and units
  - Quarterly dataset (Pool_Carbon_Quarterly)
    - Pool, Treat (NAT ART), Site, Quarter (1–5), Year, Date, Time
    - pH (unitless)
    - EC (µS/cm)
    - DO (mg/L)
    - Water Temp (°C)
    - abs254 (abs/m)
    - SUVA (l/mg/m)
    - E4E6 (dimensionless)
    - DOC (mg/L)
    - POC (mg/L)
    - CH4 (µg/L)
    - CO2 (mg/L)
    - Pool area (m²)
    - Pool depth (cm)
    - Pool volume (m³)
  - Routine dataset (Pool_Carbon_Routine)
    - Pool, Treat (NAT ART), Year, Date, Week
    - DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF (mg/L)
    - pH, EC (µS/cm), DO (mg/L), Water Temp (°C)
    - WTD (cm)
    - POC (mg/L), CH4 (µg/L), CO2 (mg/L)
    - Abs254 (abs/m), SUVA (l/mg/m), E4E6 (dimensionless)
    - Pool area (m²), Pool depth (cm), Pool volume (m³)
  - Routine_DOC
    - Year, Date, Week; Pool; Treat (NAT/ART); Depth (cm); DOC (mg/L)
  - Routine_Colour
    - Year, Date, Week; Pool; Treat; Depth (cm); Abs254 (abs/m); E4E6 (ratio); SUVA (l/mg/m)
  - Routine_Depth
    - Year, Date, Week; Pool; Treat; Depth below peat (cm)
  - Routine_Soil
    - Year, Date, Week; Pool; Treat; DOC (mg/L); Abs254 (abs/m); E4E6 (ratio); SUVA (l/mg/m)

- Data quality and provenance
  - Data are quality controlled; values below detection limits have been addressed.
  - Methods and QC procedures are detailed in the accompanying Hydrological Processes manuscript.
  - Data are organized to support standardized analysis and cross-comparison between natural and restoration pools.

- How analysts can use the data
  - Compare carbon-related parameters between natural and restoration pools over time.
  - Assess relationships between DOC (and POC), color metrics (Abs254, E4E6, SUVA), and inorganic/organic carbon indicators (CH4, CO2).
  - Examine hydrological context (WTD, pool depth, volume) alongside chemical measurements to understand carbon dynamics in peatland pools.
  - Integrate routine, DOC, colour, depth, and soil solution data for comprehensive environmental health assessments.
  - Use the standardized formats to support data repositories and portal uploads for long-term monitoring and policy performance evaluation.

- Data access and stewardship
  - Data are provided in six CSV files with clearly defined columns and units.
  - Datasets are prepared to be stored in and uploaded to appropriate environmental data portals, aligning with monitoring objectives and standardised reporting formats.

- Considerations for reuse
  - Acknowledge site codes (CL, LL, MU) and pool treatments (NAT vs ART) when aggregating or comparing data.
  - Be aware of differences between quarterly (aggregated) and routine (CL-only) data in scope and resolution.
  - Refer to the linked manuscript for detailed sampling methods, QC processes, and any caveats related to measurement techniques.