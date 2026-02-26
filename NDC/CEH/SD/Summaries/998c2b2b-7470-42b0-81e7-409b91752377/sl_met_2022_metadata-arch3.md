# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

## Overview
- Provides meteorological, soil, and microclimate data to support ammonia (NH3) enhancement experiments in a forest setting.
- Wind conditions measured at multiple heights near and above the forest canopy control the ammonia enhancement experiment.
- Detailed metadata and instrumentation descriptions enable reuse and integration into monitoring/frameworks.

## Location, timing and context
- Location: Queensberry Estate, Sri Lanka (approximately 6.9693 N, 80.5911 E; altitude 1645 m).
- Time period: 17 March 2022 to 31 December 2022.
- Timezone: Sri Lanka Standard Time (SLST).
- Setup: A 12 m measurement mast extends 5 m above the canopy, installed beside the ammonia enhancement manifold.

## Data collection setup and cadence
- Variables collected include air temperature, relative humidity, leaf wetness, wind speed/direction, barometric pressure, photosynthetically active radiation (PAR), total solar radiation, and soil measurements.
- Soil measurements: volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths.
- Cadence: data recorded every 20 seconds and aggregated into 15-minute means.
- Sensor placements: data captured at four heights for leaf wetness; measurements above and below the canopy for several atmospheric variables.
- Instrumentation providers: Vaisala, METER Environment, Campbell Scientific, Vector Instruments, Skye Instruments, among others.

## Measured variables and data structure
- Dataset size: 27,812 measurements across 37 parameters.
- Format: CSV with columns including Timestamp, Height, Instrument, Description, and parameter-specific fields (examples include LWS1–LWS4, AirT1–AirT4, RH1–RH4, Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3, WS_Cup1–WS_Cup2, PAR1–PAR2, Total_Solar1–Total_Solar2, WXT_WS1–WXT_BP2, WXT_WD1–WXT_WD2, WXT_AirT1–WXT_AirT2, WXT_RH1–WXT_RH2, etc.).
- Spatial layers: measurements are representative of ground flora, below-canopy, and above-canopy (canopy vs ground layers).
- Key sensor details: leaf wetness sensors (LWS1–LWS4); temperature/humidity sensors (AirT, RH); soil sensors (VWC, EC, T) at near-surface and at 10–15 cm depths; wind, PAR, and solar radiation sensors near and above the canopy.
- Instrument brands and models include Vaisala HMP60, METER Environment LWS, Campbell Scientific CS655, Vector Instruments A100, Skye Instruments SKP215, and Skye SP1110 for solar measurements.

## Data quality and governance notes
- Quality control: visual inspection to remove obvious instrument faults, datalogger issues, and power-cut artifacts; gaps exist due to sensor replacement.
- Data provenance: complete experimental design, methodology, analysis, and findings are published in Deshpande et al. (2024); funding provided by UKRI GCRF South Asian Nitrogen Hub.
- Metadata and reuse: dataset includes detailed instrument, height, and description fields to support data governance, interpretation, and integration into monitoring frameworks.

## References and context
- Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.