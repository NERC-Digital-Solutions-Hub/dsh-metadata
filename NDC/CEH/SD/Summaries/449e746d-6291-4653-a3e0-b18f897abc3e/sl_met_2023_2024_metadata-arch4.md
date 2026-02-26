# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- A meteorological data set from the Queensberry Estate ammonia enhancement site in Sri Lanka, collected in 2023–2024.
- Collected to support an ammonia enhancement experiment; wind conditions below the forest canopy control the ammonia enhancement.
- Data collected at a 12 m mast extending 5 m above the forest canopy, located at 6.9693° N, 80.5911° E, altitude 1645 m.
- Measurements span 1 Jan 2023 to 31 Dec 2024; originally extended from a 2022 dataset at the same site.
- Measured at 20-second intervals and averaged to 15-minute intervals; time reported in Sri Lanka Standard Time (SLST).

## What is included
- 70,176 measurements across 37 parameters.
- Data provided in a CSV file with detailed metadata in each row (timestamp, height, instrument, manufacturer, etc.).
- Example variables include:
  - Atmospheric: Rain, Throughfall, air temperatures (AirT1–AirT4), relative humidity (RH1–RH4), wind speed and direction (WXT_WS1/2, WXT_WD1/2), barometric pressure (WXT_BP1/2), photosynthetically active radiation (PAR1–PAR2), total solar radiation (Total_Solar1–Total_Solar2).
  - Soil: soil volumetric water content (Soil_VWC1–Soil_VWC3), soil temperature (Soil_T1–Soil_T3), soil electrical conductivity (Soil_EC1–Soil_EC3) at multiple depths (surface to ~15 cm).
  - Canopy and ground-level sensors: leaf wetness (LWS1–LWS4), wind speeds near floor and in canopy layers (WS_Cup1–WS_Cup3).
  - Other environmental descriptors: a range of sensor-specific fields (Height, Manufacturer, Instrument, Description) for traceability.
- Data columns include: Timestamp, Unit, Height (m), Manufacturer, Instrument, Description, plus parameter-specific fields.

## Data collection details
- Instrumentation:
  - 12 m mast with sensors at multiple heights: leaf wetness sensors near floor, ground flora layer, lower canopy, and upper canopy; air temperature and humidity sensors at forest floor, ground flora layer, canopy, and above canopy; soil sensors at multiple depths; wind, PAR, and radiation sensors at several levels.
- Timings and units:
  - Measurements in SLST; 15-minute averages derived from 20-second measurements.
  - Heights range from near ground level to above canopy for trees and forest floor measurements.
- Location and context:
  - Ammonia enhancement experiment site; wind conditions below canopy are a key control signal for the experiment.

## Quality control and data quality
- Data visually checked; obvious instrument malfunctions, datalogger programming issues, and power-cut artifacts removed.
- Some data gaps due to sensor replacement or maintenance.
- Step changes in leaf wetness measurements reflect different baseline readings when sensors were replaced.

## Data structure and accessibility
- Data supplied as a CSV file with 70,176 records across 37 parameters.
- Core fields in each record include:
  - Timestamp, Unit, Height, Manufacturer, Instrument, Description.
- Dataset is designed for integration with analytical workflows to study environmental conditions and their relation to ammonia deposition and the enhancement experiment.

## Context, usage and references
- Purpose: supports estimation of ammonia deposition and the broader understanding of ammonia enhancement effects on forest ecosystems.
- Related publications:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from the Queensberry, Sri Lanka site (2022).
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).

## Additional notes
- The dataset extends the 2022 data from the same site, enabling temporal comparisons and enhanced modeling of atmospheric and soil–canopy interactions under ammonia enhancement.
- Complete details of experimental design, methodology, analysis, and findings are available in the referenced publications.