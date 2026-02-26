# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

## Overview
- Meteorological dataset from the Queensberry Estate ammonia enhancement site in Sri Lanka, collected to support wind-controlled NH3 enhancement experiments.
- Data spans 17 March 2022 to 31 December 2022 and are used to describe environmental conditions influencing ammonia deposition and related ecological processes.
- The dataset supports environmental health monitoring by providing multi-layer atmospheric and soil measurements near a forest canopy.

## Data collection
- Instrumentation: 12 m mast extending 5 m above the forest canopy, located at 6.9693° N, 80.5911° E, altitude 1645 m.
- Measurements taken at multiple heights (near forest floor, ground flora layer, sub-canopy, and above canopy) for air temperature, relative humidity, leaf wetness, wind speed/direction, barometric pressure, photosynthetically active radiation, and solar radiation.
- Soil measurements at three depths for volumetric water content, electrical conductivity, and temperature.
- Data cadence: measurements every 20 seconds with 15-minute average values.
- Data recorded in Sri Lanka Standard Time (SLST).
- Complete experimental design, methodology, analysis, and findings are detailed in Deshpande et al. (2024).

## Quality control
- Visual data verification with removal of obvious instrument malfunctions, datalogger issues, and power-cut artifacts.
- Some gaps occurred during sensor replacement.

## Data structure and contents
- 27,812 measurements across 37 parameters.
- Provided as a CSV with descriptive columns, including:
  - Timestamp and height
  - Instrument details (manufacturer, model)
  - Parameter descriptions (e.g., leaf wetness sensors LWS1–LWS4 at various heights; AirT1–AirT4; RH1–RH4; Soil_VWC, Soil_EC, Soil_T at multiple depths; wind speeds (WS_Cup1/2); PAR, Total_Solar; WXT sensors; etc.)
- Data are organized to reflect measurements at different canopy layers (ground flora, lower canopy, upper canopy) and above-canopy conditions, with specific units and instrument specifications.

## Provenance and access
- Data structure and parameters are aligned with standardized environmental monitoring practices to enable reuse and cross-study comparisons.
- Complete details of the experimental design and methodology are described in Deshpande et al. (2024).
- Data stewardship includes storage and uploading to appropriate data portals.

## Funding
- Funding for establishing the monitoring facility provided by UKRI GCRF South Asian Nitrogen Hub.

## References
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.