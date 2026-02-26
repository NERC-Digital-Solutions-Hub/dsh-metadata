# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

- This is a data package accompanying the Hydrological Processes (2022) manuscript describing QC’d measurements of carbon concentrations and related water chemistry in natural and restoration (artificial) pools on blanket peatlands in Scotland, collected between 2013 and 2015.
- Data have undergone quality control (e.g., values below detection limits noted).

## Data scope and purpose
- Focus: carbon concentrations and associated water chemistry in peatland pools (natural vs restoration) across Scotland.
- Intended use: GIS-enabled analysis and map-based visualization of spatial and temporal patterns in pool chemistry and carbon pools.

## Data quality and provenance
- Quality controlled data; documented methodology in the manuscript.
- Some measurements flagged for detection limits; values may be adjusted or annotated accordingly.

## Datasets (six CSV files) and structure
- Pool_Carbon_Quarterly
  - Sites: LL, CL, MU (all data amalgamated into one table)
  - Purpose: quarterly pool data across sites
  - Key fields: Pool, Treat (NAT = natural; ART = artificial/restoration), Site, Quarter, Year, Date, Time, plus chemistries and hydrological variables including pH, EC, DO, Water Temp, abs254, SUVA, E4E6, DOC, POC, CH4, CO2, Pool area, Pool depth, Pool volume.

- Pool_Carbon_Routine
  - Sites: CL only
  - Purpose: frequent (routine) sampling data
  - Key fields: Year, Date, Week, DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF, pH, EC, DO, Water Temp, WTD, POC, CH4, CO2, abs254, SUVA, E4E6, Pool area, Pool depth, Pool volume.

- Pool_Carbon_Routine_DOC
  - Sites: CL only
  - Description: Piezo soil water DOC data at different depths
  - Key fields: Year, Date, Week, Pool, Depth, DOC (with depth-specific variants)

- Pool_Carbon_Routine_Colour
  - Sites: CL only
  - Description: Piezo soil water colour data at different depths
  - Key fields: Year, Date, Week, Pool, Depth, Abs254, E4E6, SUVA

- Pool_Carbon_Routine_Depth
  - Sites: CL only
  - Description: Pool depth on sampling day from continuous loggers
  - Key fields: Year, Date, Week, Pool, Depth below peat

- Pool_Carbon_Routine_Soil
  - Sites: CL only
  - Description: Bulked soil solution from piezometers
  - Key fields: Year, Date, Week, Pool, DOC, Abs254, E4E6, SUVA

## Spatial and temporal scope
- Temporal coverage: 2013–2015
- Geographic scope: blanket peatlands in Scotland
- Sites: CL (CrossLochs area), LL (Loch Lier), MU (Munsary or similar; listed as CL, LL, MU)

## Key measurements and units
- Water chemistry: pH, electrical conductivity (EC; µS/cm), dissolved oxygen (DO; mg/L), water temperature (°C)
- DOC and carbon pools: DOC (mg/L), POC (mg/L), CH4 (µg/L), CO2 (mg/L)
- Absorbance and proxies: abs254 (abs/m), SUVA (l/mg/m), E4E6 (dimensionless)
- Hydrology: pool area (m²), pool depth (cm), pool volume (m³), water table depth (WTD; cm, where applicable)
- Depth- and location-specific data: Depth (cm) for routine DOC and colour measurements; Depth below peat for Routine_Depth

## How to use the data in GIS
- Join and map by Pool, Site, Year, Date, and Week to visualize spatial distribution of carbon concentrations and water chemistry.
- Compare natural vs restoration pools (NAT vs ART) across sites and time.
- Integrate with other GIS layers (land cover, hydrology, peatland maps) to analyze drivers of carbon dynamics.
- Analyse temporal trends (seasonal/quarterly in Pool_Carbon_Quarterly; higher-frequency patterns in Pool_Carbon_Routine).

## Data preparation considerations for GIS workflows
- Align pool identifiers across files; reconcile Pool and Site codes (CL, LL, MU).
- Harmonize time fields (Year, Date, Week, Time) and convert to a consistent temporal format for visualization.
- Ensure unit consistency across datasets (e.g., DOC, POC, CH4, CO2, abs254, SUVA, E4E6).
- Handle missing values and QC flags (values below detection limits) appropriately in analyses and maps.
- When combining routine DOC and soil DOC datasets, account for depth and measurement context (soil solution vs pool water).

## Reference and access
- Data collection and generation methods are described in the manuscript: Hydrological Processes 2022.
- The six CSV files comprise the data package for the study of carbon concentrations in natural and restoration pools on blanket peatlands in Scotland, 2013–2015.