# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 2017-2019

- A multi-file dataset describing atmospheric dust and meteorological conditions at two Greenland sites (Ridge and SS85), covering 2017–2019.
- Includes measurements of particulate matter (PM1, PM2.5, respirable, PM10, and total), weather variables (temperature, relative and absolute humidity, dew point), wind (speed and direction), and dust deposition with particle-size data.

## Data files and locations

- DUSTY_DustTrak.csv
  - Location: Ridge and SS85
  - Variables: Date/Time, Site, PM1, PM2.5, RESP, PM10, Total
  - Instrument: TSI DustTrak DRX Environmental Monitor (inlet height ~2.5 m)
  - Operational dates: 19/04/2018–03/10/2018; 13/04/2019–22/08/2019 (Ridge); 21/04/2018–06/10/2018; 21/04/2019–16/08/2019 (SS85)
  - Sampling: 1-minute averages every 5 minutes
  - Missing data: 63.9–99.9% missing per sampling period (power loss, instrument faults)
  - Units: mg m^-3

- DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv
  - Location: Ridge and SS85
  - Variables: Temperature (°C), Relative Humidity (%), Absolute Humidity (g m^-3), Dew Point (°C)
  - Instrument: Omega OMYL-RH20 (~1 m above ground)
  - Operational dates: 19/04/2018–07/10/2018; 11/04/2019–22/08/2019 (Ridge); 21/04/2018–07/10/2018; 21/04/2019–16/08/2019 (SS85)
  - Sampling: 1 reading every 10 minutes
  - Missing data: 98.4–100% missing per sampling period (power/equipment issues)
  - Data structure: Date/Time, Site, Temperature, Humidity, Absolute Humidity, Dew Point
  - Units: Degrees C, %, g m^-3

- DUSTY_Weather_Station_Wind_Data.csv
  - Location: Ridge and SS85
  - Variables: Mean wind speed (m s^-1), Max wind speed (m s^-1), Min wind speed (m s^-1), Wind direction (degrees)
  - Instrument: RMYoung 5013 (2.5 m above ground)
  - Operational dates: 15/04/2018–06/10/2018; 11/04/2019–22/08/2019 (Ridge); 18/04/2018–07/10/2018; 11/04/2019–16/08/2019 (SS85)
  - Sampling: 1 reading every 5 minutes
  - Missing data: 66.4–99.9% missing per sampling period (power/equipment issues)
  - Data structure: Date/Time, Site, Mean wind speed, Max wind speed, Min wind speed, Wind direction
  - Units: Wind velocity (m s^-1), Wind direction (degrees)

- HDT_Deposition_Data.csv
  - Location: Five sites (SS906, Ridge, SS17b, SS1590, SS85)
  - Variables: Depot measurements by season (Spring/Summer/Autumn-Winter/Spring/Summer/Winter)
  - Instrument: Hall Deposition Trap (head height 1.5–1.8 m)
  - Operational dates: Seasons from Spring 2017 to Autumn/Winter 2018/19
  - Sampling: End-of-season deposition per trap
  - Retrieval/Processing: Sediments retrieved, washed, filtered (0.45 µm or 0.7 µm), desiccated, reweighed, ashed at 500°C for 4 hours; LOI used to estimate minerogenic dust; final areal deposition in g m^-2 d^-1
  - Missing data: 4–5 traps at each site unavailable in some seasons
  - Particle-size data: For 1 (PSA906) to 1 (PS85) datasets, particle-size distribution (0.375–2000 µm) via laser sizer; bulked data at some sites due to low dust mass
  - Data structure: Excel CSV; columns include Location, Trap number, seasons (Sp2017, Su2017, FaWi1718, Sp2018, Su2018, FaWi1819)
  - Units: g m^-2 d^-1 (deposited dust)

- Data Files (data per site)
  - PSA906_DUST_HDT.csv (SS906 data)
  - PSAR_DUST_HDT.csv (Ridge data)
  - PSA17b_DUST_HDT.csv (SS17b data)
  - PSA1590_DUST.csv (SS1590 data)
  - PSA85_DUST_HDT.csv (SS85 data)

- Particle-size data note
  - Size range: 0.375–2000 µm
  - Instrument: Beckman Coulter LS 230 laser sizer
  - Data handling: Where dust mass was too low, data from all HDTs were bulked to produce an average size distribution per location

## Key measurements and variables for monitoring and policy evaluation

- Airborne particulates
  - PM1, PM2.5, respirable fraction, PM10, and total particle concentrations
- Meteorological context
  - Temperature, relative humidity, absolute humidity, dew point
- Airflow conditions
  - Wind speed and wind direction
- Dust deposition
  - Areal dust deposition flux (g m^-2 d^-1)
  - Particle-size distribution of deposited minerogenic dust
- Temporal resolution
  - High-frequency time series for dust and weather; seasonal deposition summaries

## Data quality, gaps and challenges

- Frequent missing data across datasets (power losses and instrument malfunctions cited)
- High missing-data rates for dust and wind measurements (substantial portions of sampling periods unavailable)
- Weather data shows near-complete missingness in some periods, indicating potential reliability issues
- Site and seasonally specific gaps due to traps being knocked over, animal damage, or retrieval issues
- Particle-size data sometimes combined across traps due to very low dust mass in individual traps

## Data structure and formats

- Data are provided as CSV/Excel-style spreadsheets
- Each dataset includes:
  - Location identifiers and coordinates
  - Instrument details and measurement heights
  - Operational date ranges
  - Sampling frequencies and data processing steps
  - Clear unit definitions
  - Data quality notes and missing data indicators

## How this dataset supports monitoring frameworks

- Enables multi-parameter environmental health assessments at multiple sites with temporal context
- Provides a real-world example of data challenges typical in policy monitoring: data gaps, metadata completeness, and data governance considerations
- Offers deposition flux estimates and particle-size distributions useful for exposure and risk assessments
- Illustrates the need for robust metadata, QA/QC procedures, and transparent data sharing when informing future policy decisions

## Considerations for use and governance

- Data gaps and variable data availability should be accounted for in any analysis or policy evaluation
- Metadata coverage varies by dataset; ensure provenance, instrument specifics, and calibration history are captured for reproducibility
- Public sharing of underlying data may require addressing gaps in data availability and ensuring data quality standards are met
- Standardization of units and time stamps is essential for cross-site comparisons and long-term trend analysis