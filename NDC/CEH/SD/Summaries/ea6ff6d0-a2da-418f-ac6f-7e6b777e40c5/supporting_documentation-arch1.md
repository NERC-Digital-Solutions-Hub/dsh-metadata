# Meteorological and atmospheric dust data from Kangerlussuaq, southwest Greenland, 20172019

- Purpose: Describes atmospheric dust, temperature, humidity, wind, and dust deposition measurements at multiple sites in southwest Greenland across 2017–2019 to support analyses of dust fluxes, weather relationships, and particle-size distributions.

## Datasets and key features

- DUSTY_DustTrak.csv
  - Locations: Ridge (67°3'36.0432"N, 50°26'9.5208"W) and SS85 (67°0'9.522'N, 51°0'39.114"W)
  - Instrument: TSI DustTrak DRX Environmental Monitor (inlet height ~2.5 m above ground)
  - Operational dates: Ridge 19/04/2018–03/10/2018 and 13/04/2019–22/08/2019; SS85 21/04/2018–06/10/2018 and 21/04/2019–16/08/2019
  - Sampling frequency: One-minute averaged values every 5 minutes
  - Missing data: 63.9–99.9% data retrieval per sampling period due to power or equipment issues
  - Units: mg m^-3
  - Data structure: Excel CSV with A-Date/Time, B-Site, C-PM1, D-PM2.5, E-RESP, F-PM10, G-Total

- DUSTY_Weather_Station_Temperature_and_Humidity_Data.csv
  - Locations: Ridge and SS85
  - Instrument: Omega OMYL-RH20 (~1 m above ground)
  - Operational dates: Ridge 19/04/2018–07/10/2018 and 11/04/2019–22/08/2019; SS85 21/04/2018–07/10/2018 and 21/04/2019–16/08/2019
  - Sampling frequency: One reading of each variable every 10 minutes
  - Missing data: 98.4–100% missing per sampling period due to power/equipment issues
  - Units: Temperature (°C); Relative humidity (%); Absolute humidity (g m^-3); Dew point (°C)
  - Data structure: CSV with A-Date/Time, B-Site, C-Temperature, D-Relative humidity, E-Absolute humidity, F-Dew Point

- DUSTY_Weather_Station_Wind_Data.csv
  - Locations: Ridge and SS85
  - Instrument: RMYoung 5013 sensor (~2.5 m above ground)
  - Operational dates: Ridge 15/04/2018–06/10/2018 and 11/04/2019–22/08/2019; SS85 18/04/2018–07/10/2018 and 11/04/2019–16/08/2019
  - Sampling frequency: One reading every 5 minutes
  - Missing data: 66.4–99.9% missing per sampling period due to power/equipment issues
  - Units: Mean wind speed (m s^-1); Max wind speed (m s^-1); Min wind speed (m s^-1); Wind direction (degrees)
  - Data structure: CSV with A-Date/Time, B-Site, C-Mean wind speed, D-Max wind speed, E-Min wind speed, F-Wind direction

- HDT_Deposition_Data.csv
  - Locations: SS906, Ridge, SS17b, SS1590, SS85
  - Instrument: Hall Deposition Trap (trap head height 1.5–1.8 m)
  - Operational dates: Sp2017 (23/04/2017–20/06/2017); Su2017 (21/06/2017–12/08/2017); FaWi1718 (12/08/2017–13/04/2018); Sp2018 (14/04/2018–16/06/2018); Su2018 (17/06/2018–13/08/2018); FaWi1819 (14/08/2018–13/04/2019)
  - Sampling frequency: End-of-season sampling (per the above seasonal windows)
  - Protocol: Sediment retrieval, washing into collection bottle, storage, drying, ashing, and LOI-based mineral dust mass estimation; final areal deposition in gm^-2 d^-1 accounting for trap geometry and period
  - Missing data: 4–5 traps per location may be empty or data unavailable due to trap loss
  - Units: gm^-2 day^-1
  - Data structure: Excel CSV; Columns include Location, Trap number, and season-specific data (Season abbreviations)

- 1 = PSA906_DUST_HDT.csv; PSAR_DUST_HDT.csv; PSA17b_DUST_HDT.csv; PSA1590_DUST.csv; PSA85_DUST_HDT.csv
  - Description: Particle-size data for deposited dust trapped at five locations
  - Locations: SS906, Ridge, SS17b, SS1590, SS85
  - Instrument: Hall Deposition Trap
  - Operational dates: Seasonal windows as above
  - Sampling frequency: End-of-season collection
  - Protocol: Same retrieval and processing as HDT data; particle-size analysis with Beckman Coulter LS 230 laser sizer (range 0.375–2000 µm; 93 class intervals)
  - Missing data: Low dust mass may lead to bulked averaging across traps
  - Units: gm^-2 day^-1 (for mass; particle-size distribution per trap)
  - Data structure: CSV with Size (µm) and trap-specific data (Trap numbers)

## Data access and structure

- File formats: CSV/Excel spreadsheets
- Common columns: Date/Time, Site, measurements (dust masses, PM fractions, temperature, humidity, wind metrics), trap identifiers, seasons
- Data reliability notes: 
  - Substantial missingness in several datasets due to power failures, equipment malfunctions, and trap losses
  - Some datasets are seasonally aggregated or bulked (e.g., HDT deposition particle-size data) due to low dust mass at individual traps
  - Particle-size data provide a detailed spectrum (0.375–2000 µm) but may be aggregated when sample mass is low

## Key considerations for analysts

- Data gaps and local-scale coverage: Large portions of dust and weather data have substantial to near-total missingness in several periods and sites; careful handling of missing values and bias is required
- Multi-sensor integration: Combining dust concentration, deposition, and meteorological data can reveal relationships between particle loading, deposition flux, wind regimes, and temperature/humidity, but cross-site and seasonal alignment is needed
- Scale and boundaries: Some measurements are site-specific (Ridge, SS85, SS906, SS17b, SS1590, SS85) and may require careful spatial alignment or aggregation for regional analyses
- Quality assurance: Documentation indicates processing steps (e.g., LOI-based deposition mass, ashing, laser sizing) that should be reflected in any reproducible analysis
- Data discoverability: Datasets are described with explicit names, dates, and measurement definitions, enabling targeted data retrieval for specific research questions

## Summary of what can be analyzed

- Relationships between atmospheric dust concentrations (PM fractions) and meteorological conditions (temperature, humidity, wind speed/direction)
- Temporal patterns of dust loading across seasons and sites
- Dust deposition flux and its spatial variation among deposition traps
- Particle-size distributions of deposited dust across sites and seasons
- Cross-dataset analyses to infer drivers of dust transport and deposition in southwest Greenland (e.g., wind events, humidity, deposition mass)