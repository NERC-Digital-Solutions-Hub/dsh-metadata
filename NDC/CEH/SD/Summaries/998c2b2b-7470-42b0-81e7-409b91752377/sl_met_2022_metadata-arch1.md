# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

## Overview
- Data support the ammonia enhancement experiment by characterizing wind and meteorological conditions controlling NH3 dynamics.
- Location: Queensberry Estate, Sri Lanka (6.9693°, 80.5911°; altitude 1645 m).
- Timeframe: 17 March 2022 to 31 December 2022, in Sri Lanka Standard Time (SLST).
- Mast height: 12 m, extending 5 m above the forest canopy; measurements collected near the ammonia enhancement manifold.
- Data intended for correlation analyses, model development, and informing practical decisions related to ammonia deposition experiments.

## Data collection and variables
- Measurements taken at multiple heights for a vertical profile:
  - Leaf wetness sensors (LWS1–LWS4) at 0.3, 2.0, 3.6, and 5.6 m.
  - Air temperature and relative humidity at several near-ground, mid-canopy, and above-canopy heights.
  - Wind speed and wind direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation above and below the canopy.
  - Soil volumetric water content (VWC), electrical conductivity (EC), and temperature (T) at three depths (near surface and deeper layers).
  - Wind, temperature, humidity, radiation sensors located both below and above the canopy (e.g., WXT and canopy/ground-level arrays).
- Sampling cadence: instruments record every 20 seconds; results averaged to 15-minute intervals.
- Units and metadata included in the dataset schema; complete methodology and analysis details described in Deshpande et al. (2024).

## Quality control
- Visual quality checks performed; obvious instrument malfunctions, datalogger issues, and power-cut artifacts removed.
- Some data gaps occurred due to time taken to replace faulty sensors.

## Data structure and access
- Dataset contains 27,812 measurements across 37 parameters.
- Provided as a CSV with fields including:
  - Timestamp, Height, Instrument, Description
  - Leaf Wetness Sensors: LWS1–LWS4 with specific heights and descriptions
  - Air temperature and relative humidity at multiple heights (AirT1–AirT4, RH1–RH4)
  - Soil: VWC1–VWC3, EC1–EC3, T1–T3 (with corresponding depths/descriptions)
  - Wind: WS_Cup1–WS_Cup2, WXT_WS1–WXT_WS2, WXT_WD1–WXT_WD2
  - Radiation: PAR1–PAR2, Total_Solar1–Total_Solar2
  - Additional canopy-level sensors (e.g., WXT_AirT1–WXT_AirT2, WXT_RH1–WXT_RH2, WXT_BP1–WXT_BP2)
- Data is accompanied by publication references detailing the experimental design and analysis.

## Context for analysis and potential uses
- The wind conditions measured below the canopy are used to control and interpret the ammonia enhancement experiment.
- Enables correlations between meteorological variables (wind profiles, temperature, humidity, soil moisture, radiation) and the ammonia enhancement/deposition processes.
- The multi-height data supports vertical profiling and assessment of how microclimate gradients influence NH3 behavior.
- Data can be integrated with the related ammonia deposition study (Deshpande et al., 2024) for broader insights into NH3 dynamics in tropical forest settings.

## Funding and references
- Funded by UKRI GCRF South Asian Nitrogen Hub for establishing the measurement facility.
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024.