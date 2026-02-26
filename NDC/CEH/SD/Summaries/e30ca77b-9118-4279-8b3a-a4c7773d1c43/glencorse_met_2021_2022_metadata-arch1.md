# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022)

## Overview
- Dataset of meteorological measurements collected to support ammonia enhancement experiments and analysis of NH3 deposition to forest ecosystems.
- Location: Glencorse woodland, near UKCEH, Edinburgh (coordinates 55.8539°, -3.2151°; altitude 200 m).
- Key purpose: Use wind-controlled NH3 enhancement data to understand deposition dynamics and inform related analyses.

## Data collection details
- Setup: 16 m mast extending 2 m above the forest canopy; installed adjacent to the ammonia enhancement manifold.
- Measurements include:
  - Air temperature, relative humidity, leaf wetness, wind speed at four heights
  - Rainfall, wind direction, barometric pressure
  - Photosynthetically active radiation (PAR) and total solar radiation above and below canopy
  - Soil volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths
- Sampling: every 20 seconds; 15-minute interval averages
- Timeframe: 28 May 2021 to 5 January 2023
- Time reference: GMT

## Quality control
- Data visually inspected; obvious instrument/logger/Power issues removed
- Gaps occurred due to sensor replacement and power outages
- Data used for analyses reflect cleaned measurements after quality checks

## Data structure and contents
- Size: 56,154 measurements across 41 parameters
- Format: CSV with detailed columns (example fields include):
  - Timestamp, Height, Manufacturer, Instrument, Description
  - Rain, Throughfall
  - Leaf Wetness Sensors (LWS1–LWS4) with height, unit, and description
  - Air temperature and relative humidity near forest floor, ground flora layer, tree canopy, and top of canopy (AirT1–AirT4; RH1–RH4)
  - Soil VWC, EC, and T at depths near surface, 10 cm, and 15 cm (VWC1–VWC3, EC1–EC3, T1–T3)
  - Wind speed sensors near ground, ground flora layer, tree canopy, and top of canopy (WS_Cup1–WS_Cup4)
  - PAR and Total Solar radiation (PAR1, Total_Solar1–Total_Solar2)
  - Wind and radiation-related metadata fields (WXT_WS*, WXT_WD*, WXT_AirT*, WXT_RH*, WXT_BP*)
- Notes:
  - All measurements are recorded in GMT
  - 41 parameters span meteorology, soil, and canopy-interfacing sensors
  - Data include both below-canopy and above-canopy measurements for comparative analyses

## Measurements and sensors (summary)
- Meteorology near and below canopy: air temperature, relative humidity, wind speed, wind direction, barometric pressure
- Radiation: PAR and total solar radiation (below- and above-canopy)
- Precipitation: rainfall and throughfall
- Plant/soil interface: leaf wetness at multiple canopy layers; soil VWC, EC, and temperature at multiple depths
- Wind profiling: multiple height levels for wind speed and related above/below canopy contrasts

## Timeframe and data format
- Timeframe: 28 May 2021 – 5 January 2023
- Data format: CSV with structured metadata-enabled columns
- Data provenance: collected at a dedicated ammonia enhancement facility with prior validation and quality checks

## Experimental context
- Wind conditions measured below the forest canopy were used to control the ammonia enhancement experiment
- Data support estimation of ammonia deposition to forest ecosystems and related analyses (Deshpande et al. 2024)

## Data quality considerations
- Visual quality control completed; minor gaps from sensor maintenance and power disruptions
- Data suitable for correlation and time-series analyses with careful handling of gaps and sensor-specific calibrations

## Practical applications for analysts
- Identify correlations between ammonia enhancement/deposition and meteorological variables
- Develop predictive models of NH3 flux/deposition using multi-height wind, temperature, humidity, and radiation data
- Integrate with other environmental datasets to study ecosystem responses to ammonia enhancement
- Use in atmospheric deposition studies and validation against broader deposition models

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub
- Key reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.