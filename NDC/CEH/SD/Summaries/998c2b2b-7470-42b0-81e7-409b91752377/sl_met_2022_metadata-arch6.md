# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

## Overview
- Meteorological data collected from a 12 m mast near the ammonia enhancement manifold at Queensberry Estate, Sri Lanka (coordinates 6.9693°, 80.5911°; altitude 1645 m).
- Timeframe: 17 March 2022 to 31 December 2022, in Sri Lanka Standard Time (SLST).
- Purpose: Wind conditions measured below the forest canopy to control the ammonia enhancement experiment.

## Data collection
- Measurements taken at four heights for air temperature, relative humidity, and leaf wetness; wind speed and direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation above and below the canopy.
- Soil measurements at three depths: volumetric water content (VWC), electrical conductivity (EC), and temperature (T).
- Instrumentation includes Vaisala devices (HMP60), METER Environment leaf wetness sensors, Campbell Scientific CS655 sensors, Vector Instruments anemometers, Skye Instruments PAR and total solar sensors, and WXT536 equipment for wind and environmental parameters.
- Sampling rate: 20-second measurements with 15-minute averages for the dataset.
- All data reported in Sri Lanka Standard Time.

## Quality control
- Visual checks performed; obvious errors from instrument malfunction, datalogger issues, and power cuts removed.
- Gaps present due to sensor replacement and maintenance.

## Data structure and contents
- Dataset comprises 27,812 measurements across 37 parameters.
- Provided as a CSV file with columns including:
  - Timestamp (formatted as 15-minute timestamps)
  - Height, Unit, Description for each parameter
  - Leaf Wetness Sensors: LWS1–LWS4 at various heights
  - Near-ground and above-canopy air temperature (AirT1–AirT4) and relative humidity (RH1–RH4)
  - Soil measurements: Soil_VWC1/2/3, Soil_EC1/2/3, Soil_T1/2/3 at corresponding depths
  - Wind measurements: WS_Cup1/2, WXT_WS1/2, WXT_WD1/2
  - Radiation and light: PAR1/2, Total_Solar1/2
  - Other environmental parameters as per sensor descriptions
- The dataset captures both below-canopy and above-canopy environmental conditions relevant to the ammonia enhancement study.

## Temporal and geographic coverage
- Location: Queensberry Estate, Sri Lanka (forest environment near the ammonia enhancement facility)
- Time period: 17 March 2022 – 31 December 2022
- Time standard: SLST

## Data notes and references
- Complete details of experimental design, methodology, analysis, and findings are published in Deshpande et al. (2024).
- Funding: UKRI GCRF South Asian Nitrogen Hub.

## Reference
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.