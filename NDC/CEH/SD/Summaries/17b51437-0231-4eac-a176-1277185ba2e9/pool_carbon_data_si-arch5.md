# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- Study of carbon concentrations in natural and restoration (artificial) pools across blanket peatlands in Scotland during 2013–2015.
- Data collection and generation methods outlined in the manuscript: Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022.
- Data have undergone quality control (e.g., values below detection limits addressed).
- Provided as six CSV files, with site codes CL, LL, MU and a mix of quarterly and routine sampling data.

## Data structure and contents
- Six CSV files:
  - Pool_Carbon_Quarterly
    - Sites: CL, LL, MU
    - Description: All data from LL, CL, and MUpools amalgamated into one table
    - Key fields: Pool, Treat (NAT = natural pools; ART = artificial/restoration pools), Site, Quarter (1–5), Year, Date, Time
    - Measurements: pH, EC (µS/cm), DO (mg/l), Water Temp (°C), abs254, SUVA (l/mg/m), E4E6, DOC (mg/l), POC (mg/l), CH4 (µg/l), CO2 (mg/l), Pool area (m2), Pool depth (cm), Pool volume (m3)
  - Pool_Carbon_Routine
    - Sites: CL only
    - Description: Routine sampling data for CL (frequent sampling)
    - Key fields: Pool, Treat, Year, Date, Week
    - Measurements: DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF, pH, EC, DO, Water Temp, WTD (cm), POC, CH4, CO2, abs254, SUVA, E4E6, Pool area (m2), Pool depth (cm), Pool volume (m3)
  - Pool_Carbon_Routine_DOC
    - Sites: CL only
    - Description: Piezo soil water DOC data at different depths
    - Key fields: Year, Date, Week, Pool, Depth
    - Measurements: DOC (mg/l)
  - Pool_Carbon_Routine_Colour
    - Sites: CL only
    - Description: Piezo soil water colour data at different depths
    - Key fields: Year, Date, Week, Pool, Depth
    - Measurements: Abs254 (abs/m), E4E6, SUVA (l/mg/m)
  - Pool_Carbon_Routine_Depth
    - Sites: CL only
    - Description: Pool depth below peat
    - Key fields: Year, Date, Week, Pool, Depth below peat (cm)
  - Pool_Carbon_Routine_Soil
    - Sites: CL only
    - Description: Bulked soil solution water
    - Key fields: Year, Date, Week, Pool, Depth
    - Measurements: DOC (mg/l), Abs254 (abs/m), E4E6, SUVA
- Common structure details
  - Pool, Treat (NAT/ART), Year, Date, Week are common identifiers to link data across files
  - Units are specified per variable (e.g., pH, EC in µS/cm, DO mg/l, Temperature °C, DOC mg/l)
  - Depth-related fields capture sampling depth (for soil and piezometer measurements)

## Data governance and stewardship implications
- Standardization:
  - Consistent use of pool identifiers, site codes, treatment labels, and time stamps across files to enable reliable merging and longitudinal analyses.
  - Clear, pluggable unit definitions and variable descriptions to support reuse and interoperability.
- Metadata and documentation:
  - Each dataset file includes explicit variable definitions and units; cross-file keys (Pool, Site, Year, Date, Week, Treat) enable dataset integration.
  - Methods and QA notes referenced to the accompanying Hydrological Processes 2022 manuscript.
- Data availability and updates:
  - Data are organized for sharing as CSVs with accompanying documentation; stewardship should maintain versioning, track updates, and preserve cross-file links during updates.
- Data quality:
  -QA performed with attention to detection limits; non-detects or below-detection-limit values addressed as part of quality control.

## Practical use for Data Stewards
- Ensure the six CSVs remain consistent and interoperable when integrated into broader data catalogs or portals.
- Maintain strong linkage keys (Pool, Site, Treat, Year, Date, Week) to support joins across files for comprehensive analyses.
- Preserve and communicate method provenance by referencing the 2022 Hydrological Processes manuscript for methods and QA procedures.
- Provide guidance on data sharing policies, embargo considerations, and updates to reflect ongoing or future sampling if applicable.

## Limitations and considerations
- Data cover 2013–2015 for peatland pools; routine sampling is concentrated at CL with additional quarterly data from LL and MU.
- Some data types (e.g., soil solution colour, DOC at soil depths) are file-specific (partial overlap across files); careful merging is required to avoid misalignment.
- Users should consult the cited manuscript for full methodological context and any field-specific considerations that influence data interpretation.

## Licensing and attribution
- For full methodological details and QA procedures, users should cite the associated manuscript: Carbon concentrations in natural and restoration pools in blanket peatlands, Hydrological Processes 2022.