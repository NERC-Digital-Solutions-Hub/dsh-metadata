# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 2017-2019

- Data comprise meteorological measurements, atmospheric dust concentrations, dust deposition, and particle-size distributions collected at two sites in southwest Greenland (Ridge and SS85) and at five deposition locations (SS906, Ridge, SS17b, SS1590, SS85).
- Instrumentation includes a TSI DustTrak DRX, RMYoung wind sensor, and Omega OMYL-RH20 humidity/temperature sensor, with standard sample intervals and field protocols.
- Seasonal campaigns occurred mainly across 2018 and 2019, with data processing and quality-control steps described (LOI for deposition, particle-size analysis, etc.).
- Large data gaps are present due to power, equipment, and trap issues, affecting data completeness across all files.

## Data files and contents

- DUSTY_DustTrak.csv
  - Location: Ridge and SS85
  - Measurements: PM1, PM2.5, RESP (respirable), PM10, Total (particle concentrations)
  - Instrument: TSI DustTrak DRX Environmental Monitor (inlet ~2.5 m above ground)
  - Sampling: 1-minute averages every 5 minutes
  - Units: mg m^-3
  - Operational dates: 2018 and 2019 campaigns with site-specific windows
  - Data issues: missing data due to power/instrument malfunctions
  - Structure: A – Date/Time; B – Site; C–G – PM1, PM2.5, RESP, PM10, Total

- DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv
  - Locations: Ridge and SS85
  - Instrument: Omega OMYL-RH20 (~1 m above ground)
  - Sampling: 1 reading every 10 minutes
  - Units: Temperature (°C); Relative humidity (%); Absolute humidity (g m^-3); Dew Point (°C)
  - Operational dates: 2018 and 2019 campaigns
  - Data issues: data retrieval nearly complete but with occasional gaps
  - Structure: A – Date/Time; B – Site; C – Temperature; D – Relative humidity; E – Absolute humidity; F – Dew Point

- DUSTY_Weather_Station_Wind_Data.csv
  - Locations: Ridge and SS85
  - Instrument: RMYoung 5013
  - Sampling: 1 reading every 5 minutes
  - Units: Wind velocity (m s^-1); Wind direction (degrees)
  - Operational dates: 2018 and 2019 campaigns
  - Data issues: missing data per sampling period due to power/equipment problems
  - Structure: A – Date/Time; B – Site; C – Mean wind speed; D – Max wind speed; E – Min wind speed; F – Wind direction

- HDT_Deposition_Data.csv
  - Locations: SS906, Ridge, SS17b, SS1590, SS85
  - Instrument: Hall Deposition Trap (head height 1.5–1.8 m)
  - Seasonal periods: Sp2017, Su2017, FaWi1718, Sp2018, Su2018, FaWi1819
  - Sampling: End of each season (seasonal snapshots)
  - Processing: Sediment retrieval, filtration, drying, ashing, LOI to derive minerogenic mass; deposition rates are calculated as gm^-2 d^-1
  - Missing data: some traps lost (n/d), 4–5 traps per location
  - Units: gm^-2 day^-1
  - Structure: A – Location; B – Trap number (1–5); C–H – season codes

- Data Files (particle-size data)
  - PSA906_DUST_HDT.csv; PSAR_DUST_HDT.csv; PSA17b_DUST_HDT.csv; PSA1590_DUST.csv; PSA85_DUST_HDT.csv
  - Content: Particle-size distributions for deposited dust at each location
  - Instrument: Hall Deposition Trap; particle-size analysis with laser sizer (0.375–2000 µm)
  - Seasonal data: same seasonal windows as deposition data
  - Missing data: traps may not yield data; bulked averages used when needed
  - Structure: Size (µm); subsequent columns for trap data

## Locations, coordinates, and sites

- Ridge: 67°3'36.0432"N, 50°26'9.5208"W
- SS85: 67°0'9.522"N, 51°0'39.114"W
- Deposition sites: SS906, Ridge, SS17b, SS1590, SS85 (same regional area)

## Temporal coverage and sampling details

- Dust concentration (DUSTY_DustTrak.csv)
  - Campaigns: 2018 and 2019
  - Sites: Ridge and SS85
  - Frequency: 1-minute measurements averaged over 5-minute intervals
- Weather data (DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv)
  - Campaigns: 2018 and 2019
  - Frequency: 10-minute interval readings
- Wind data (DUSTY_Weather_Station_Wind_Data.csv)
  - Campaigns: 2018 and 2019
  - Frequency: 5-minute interval readings
- Deposition data (HDT_Deposition_Data.csv)
  - Seasons: Sp2017 to FaWi1819 (end-of-season sampling)
  - Frequency: seasonal, with 4–5 traps per site
- Particle-size data (PSA906_DUST_HDT.csv etc.)
  - Seasons: same seasonal windows
  - Frequency: end-of-season sampling

## Data quality, gaps, and caveats

- Missing data across all datasets due to power issues, instrument malfunctions, trap losses
  - DustTrak: 63.9–99.9% missing per sampling period
  - Weather: 98.4–100% missing per sampling period
  - Wind: 66.4–99.9% missing per sampling period
  - Deposition: some traps missing data due to trap loss; average distributions used where needed
- Data are stored in CSV-formatted spreadsheets; some datasets aggregate multiple traps or sites
- Standardized recording of locations, instruments, operational windows, and measurement units to aid cross-dataset integration

## Data processing, structure, and provenance

- Processing steps described for deposition data:
  - Sampled dust collected, filtered, dried, ashed
  - LOI inverses used to estimate minerogenic mass
  - Final areal dust deposition calculated by trap geometry and time period
- Particle-size analysis performed with a laser sizer (0.375–2000 µm) to produce size distributions
- Data structure for most files follows typical tabular CSV layout with clearly defined columns (Date/Time, Site, measured variables, and metadata)

## Potential uses and analysis considerations for monitoring

- Time-series analysis of dust concentrations in ridges vs. SS85
- Correlation of dust levels with wind speed/direction and meteorological conditions
- Seasonal deposition patterns and shifts across years
- Integration of particle-size distributions with deposition rates to assess inorganic dust flux and grain-size changes
- Data quality assessment and gap-filling approaches to improve long-term environmental health monitoring
- Cross-referencing with other environmental datasets to evaluate broader ecosystem health and policy performance over time