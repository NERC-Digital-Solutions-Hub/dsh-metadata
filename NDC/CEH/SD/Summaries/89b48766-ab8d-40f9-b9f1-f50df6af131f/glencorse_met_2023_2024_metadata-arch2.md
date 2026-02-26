# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

## Overview
- Provides meteorological data to support the Glencorse ammonia enhancement experiment and to extend the 2021-22 dataset.
- Enables analysis of environmental conditions and their influence on ammonia deposition and related processes.

## What and where
- Location: Glencorse woodland, near Edinburgh, UKCEH.
- Measurement mast: 16 m tall, extending 2 m above the forest canopy; installed beside the ammonia enhancement manifold.
- Coordinates: 55.8539 N, -3.2151 W; altitude ≈ 200 m.

## Data collection and processing
- Data collection scope:
  - Air temperature, relative humidity, leaf wetness, wind speed at four heights.
  - Rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), total solar radiation (above and below canopy).
  - Soil volumetric water content (VWC), electrical conductivity (EC), soil temperature at multiple depths.
- Temporal resolution: measurements every 20 seconds; 15-minute averages computed.
- Timeframe: 1 January 2023 to 31 December 2024; times recorded in GMT.
- Quality control: visual checks; removal of clear instrument/malfunction, datalogger, and power-cut errors; gaps due to sensor replacement.

## Data structure and variables
- Dataset: 70,176 measurements across 41 parameters.
- Format: CSV with detailed column structure (example fields include Timestamp, Height, Instrument, Description, and numerous sensor-specific entries).
- Key parameter categories: rainfall/throughfall, leaf wetness sensors (LWS1–LWS4), near-ground and canopy air temperature and humidity (AirT, RH at multiple heights), soil metrics (VWC, EC, T at depths near surface, 10 cm, 15 cm), wind speeds and directions at multiple heights, PAR, and total solar radiation, below- and above-canopy readings.

## Timeframe and cadence
- 2023-01-01 to 2024-12-31: GMT-based timestamps.
- Data cadence: high-frequency (20 s measurements) with 15-minute averaged outputs for analysis.

## Experimental relevance
- Wind conditions measured below the forest canopy are used to control and inform the ammonia enhancement experiment.
- Data extend the existing 2021-22 site dataset, enabling cross-period comparisons and trend analyses.

## Data availability and references
- Related publications:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from Glencorse site (2021-2022).
- Data source and hosting: NERC EDS Environmental Information Data Centre (for the 2021-2022 dataset; 2023-2024 dataset documented here).
  
## Funding
- UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- UKCEH National Capability for UK Challenges Programme (NE/Y006208/1).