# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 20172019

- This dataset collection comprises meteorological and atmospheric dust measurements collected at two southwest Greenland locations, Ridge and SS85, over 2017–2019.
- Measurements include dust concentrations, weather conditions (temperature, humidity, wind), dust deposition, and particle-size distributions from deposited dust.
- Data are organized into multiple CSV files with site-specific and season-specific records, accompanied by detailed descriptions of instruments, operational dates, sampling frequencies, and data processing steps.

## Datasets and contents

- DUSTY_DustTrak.csv
  - Purpose: Atmospheric dust concentration measurements at Ridge and SS85.
  - Instrument: TSI DustTrak DRX Environmental Monitor (8543-M) with inlet at ~2.5 m above ground.
  - Operational dates: Ridge (2018-04-19 to 2018-10-03; 2019-04-13 to 2019-08-22), SS85 (2018-04-21 to 2018-10-06; 2019-04-21 to 2019-08-16).
  - Sampling: 1-minute average every 5 minutes.
  - Missing data: 63.9% to 99.9% per sampling period (power auto-zero faults, equipment malfunctions).
  - Units: mg/m^3.
  - Structure: A = Date/Time, B = Site, C–G = PM1, PM2.5, RESP, PM10, Total.

- DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv
  - Purpose: Air temperature and humidity at Ridge and SS85.
  - Instrument: Omega OMYL-RH20 (~1 m above ground).
  - Operational dates: Ridge (2018-04-19 to 2018-10-07; 2019-04-11 to 2019-08-22), SS85 (2018-04-21 to 2018-10-07; 2019-04-21 to 2019-08-16).
  - Sampling: 1 reading every 10 minutes.
  - Missing data: 98.4% to 100% per sampling period (power or equipment issues).
  - Units: Temperature (°C), Relative humidity (%), Absolute humidity (g/m^3), Dew point (°C).
  - Structure: A = Date/Time, B = Site, C = Temperature, D = Relative humidity, E = Absolute humidity, F = Dew Point.

- DUSTY_Weather_Station_Wind_Data.csv
  - Purpose: Wind speed and direction data at Ridge and SS85.
  - Instrument: RMYoung 5013 (2.5 m above ground).
  - Operational dates: Ridge (2018-04-15 to 2018-10-06; 2019-04-11 to 2019-08-22), SS85 (2018-04-18 to 2018-10-07; 2019-04-11 to 2019-08-16).
  - Sampling: 1 reading every 5 minutes.
  - Missing data: 66.4% to 99.9% per sampling period (power or equipment issues).
  - Units: Wind speed (m/s), Wind direction (degrees).
  - Structure: A = Date/Time, B = Site, C = Mean wind speed, D = Max wind speed, E = Min wind speed, F = Wind direction.

- HDT_Deposition_Data.csv
  - Purpose: Dust deposition measurements at five locations (SS906, Ridge, SS17b, SS1590, SS85).
  - Instrument: Hall Deposition Trap (head height 1.5–1.8 m).
  - Seasonal periods: Sp2017, Su2017, FaWi1718, Sp2018, Su2018, FaWi1819 (defined by specific date ranges).
  - Sampling: End-of-season retrieval per season.
  - Processing: Sediments retrieved, filtered, dried, weighed, ashed at 500°C for 4 hours; LOI used to estimate minerogenic dust mass; final areal dust deposition calculated as g/m^2/day, accounting for trap diameter and collection period.
  - Missing data: 4 or 5 traps per location; “n/d” indicates no data due to trap loss or damage.
  - Units: g/m^2/day.
  - Structure: A = Location, B = Trap number (1–5), C–H = Season-specific data.

- Data Files (PSA906_DUST_HDT.csv, PSAR_DUST_HDT.csv, PSA17b_DUST_HDT.csv, PSA1590_DUST.csv, PSA85_DUST_HDT.csv)
  - Purpose: Particle-size data for deposited dust at the listed locations.
  - Instrument: Hall Deposition Trap; particle-size analysis with a laser sizer (0.375–2000 µm, 93 class intervals).
  - Seasonal periods: Correspond to the HDT dataset seasons; deposition material may be bulked when low mass was collected.
  - Missing data: 4 or 5 traps per location.
  - Units: Particle size (µm) with deposition mass per trap as previously described.
  - Structure: A = Size (µm), B–F = Trap numbers (HDT1–HDT4/5) indicating per-trap size distributions.

## Metadata, units, and data structure

- All datasets use CSV text format with explicit headers and site identifiers (Ridge, SS85, and other location codes, e.g., SS906, SS17b, SS1590, SS85, Ridge).
- Geographical coordinates are provided for each site.
- Units are specified per dataset (e.g., mg/m^3 for dust, °C for temperature, % for humidity, m/s for wind, g/m^2/day for deposition, µm for particle size).
- Data columns consistently include Date/Time, Site, and measurements specific to each dataset.

## Data quality, missing data, and limitations

- Across datasets, substantial missing data due to power loss, auto-zero faults, and equipment malfunctions.
- Dust concentration data (DUSTY_DustTrak.csv) show 63.9% to 99.9% data retrieval per sampling period.
- Weather-related datasets (temperature/humidity and wind) show 98.4% to 100% data gaps per sampling period.
- Some deposition datasets note missing data due to traps being damaged or knocked over; records indicate 4–5 traps per location may be missing data.
- Data processing steps (LOI and ashing) introduce additional processing-derived estimates for minerogenic dust; particle-size analyses provide distributional context but may be affected by low mass in some traps.

## Provenance, processing, and standards

- Field protocols include standardized instrument deployment heights (typically around 1–2 m above ground) and seasonal sampling strategies.
- Deposition calculations involve:
  - Retrieval of sediment from HDT traps and washing into collection bottles.
  - Vacuum filtration and desiccation for dry mass.
  - LOI to estimate minerogenic dust mass.
  - Calculation of final areal dust deposition (g/m^2/day) with corrections for trap diameter and collection duration.
- Particle-size analysis performed with a Beckman Coulter LS 230 laser sizer for sizes 0.375–2000 µm.
- For low dust mass, particle-size data were often bulked across traps to produce location-level distributions.

## Data management and accessibility

- Data are organized per dataset with explicit descriptions of locations, instruments, operational windows, and sampling regimes.
- Data are stored as CSV files with detailed metadata embedded in the descriptions, including measurement units and data structures.
- The naming conventions (e.g., PSA906_DUST_HDT.csv) reflect site-location mappings and measurement type to aid discoverability and reuse.

## Governance considerations for Data Stewards

- Ensure metadata completeness and consistency across all files (sites, coordinates, instruments, time ranges, units, and sampling frequencies).
- Standardize site identifiers and data dictionaries to improve interoperability across datasets.
- Maintain documentation of missing data periods and instrument malfunctions for transparency.
- Implement versioning and change-tracking when updates or corrections are made; capture processing steps (e.g., LOI, ashing) as part of data provenance.
- Consider publishing a data dictionary and data quality reports to accompany the datasets, enabling data users to assess suitability for their analyses.
- Plan for data updates as new seasons are collected, ensuring alignment of new data with existing seasonal schema and deposition calculations.