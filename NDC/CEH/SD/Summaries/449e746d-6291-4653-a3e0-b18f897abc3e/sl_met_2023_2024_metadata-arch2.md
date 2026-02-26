# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- Meteorological dataset collected at the Queensberry Estate ammonia enhancement site in Sri Lanka.
- Extends the previous 2022 dataset from the same site; part of wind-controlled NH3 enhancement experiments.
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).

## Data collection and instrumentation
- 12 m mast located next to the ammonia enhancement manifold; height above forest canopy extends measurements up to four levels.
- Measurements include:
  - Air temperature, relative humidity, and leaf wetness at four heights.
  - Wind speed and wind direction, barometric pressure.
  - Photosynthetically active radiation (PAR) and total solar radiation (above and below the canopy).
  - Soil volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths.
- Sampling: data every 20 seconds, averaged to 15-minute intervals.
- Timeframe: 1 January 2023 to 31 December 2024, in Sri Lanka Standard Time (SLST).

## Temporal coverage and spatial context
- Location: Queensberry Estate, Sri Lanka (coordinates 6.9693° N, 80.5911° E; altitude 1645 m).
- Below-canopy wind conditions and related meteorology used to drive the NH3 enhancement experiment.

## Quality control and data handling
- Visual quality checks; removal of obvious errors from instrument malfunctions, datalogger issues, and power cuts.
- Gaps remain due to sensor replacement; step changes in leaf wetness reflect baseline shifts when sensors were swapped.
- Data described as an extension of the 2022 dataset.

## Data structure and contents
- Dataset comprises 70,176 measurements across 37 parameters.
- Provided as a CSV file with metadata columns (Timestamp, Height, Manufacturer, Instrument, Description) and measured variables such as:
  - Rain and throughfall (precipitation-related)
  - Leaf wetness sensors (LWS1–LWS4) at various canopy layers
  - Air temperature and relative humidity at multiple heights
  - Soil VWC, EC, and temperature at different depths (surface to 15 cm)
  - Wind speed and direction near ground and in canopy
  - PAR and total solar radiation (below- and above-canopy)
  - Barometric pressure
- Units and sensor details vary by variable (examples include °C for air temperature, % for RH, mV for LWS, mm for rainfall, and m s-1 for wind).

## Location-specific details
- Data collected near the forest canopy at the Queensberry site to support ammonia enhancement experiments and deposition studies.

## Data availability and references
- Data described in:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Queensberry, Sri Lanka (2022 dataset reference).
- Data and methodological details available through cited publications and the Environmental Information Data Centre entry.