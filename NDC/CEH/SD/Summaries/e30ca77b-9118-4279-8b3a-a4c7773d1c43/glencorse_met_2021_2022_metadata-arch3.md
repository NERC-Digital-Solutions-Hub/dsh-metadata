# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022)

## Overview
- Provides high-resolution meteorological and environmental measurements from a forest site to support ammonia enhancement experiments and deposition studies.
- Data used to inform estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka (Deshpande et al., 2024).

## Data collection design
- Location: Glencorse woodland near UKCEH, Edinburgh (latitude 55.8539, longitude -3.2151; altitude 200 m).
- Instrumentation: 16 m mast with measurements at multiple heights, spanning near-ground, ground-flora, tree canopy, and top-canopy layers.
- Variables measured (examples across categories):
  - Atmospheric: air temperature, relative humidity, leaf wetness, wind speed and direction, rainfall, barometric pressure, photosynthetically active radiation (PAR), total solar radiation.
  - Soil: volumetric water content (VWC), electrical conductivity (EC), temperature at multiple depths (surface, 10 cm, 15 cm).
  - Additional data: multiple wind and radiation sensors at different heights; above- and below-canopy measurements.
- Temporal resolution: measurements every 20 seconds; results averaged to 15-minute intervals.
- Observation period: 28 May 2021 to 5 January 2023.
- Data management note: wind conditions measured below the canopy are used to control the ammonia enhancement experiment.

## Data processing and quality control
- Quality control performed: visual inspection; removal of obvious instrument malfunctions, misconfigurations, and power-outage-related errors.
- Acknowledged data gaps due to sensor replacement and maintenance.
- Data flagged as GMT timestamps to ensure consistent time standard.

## Data structure and metadata
- Dataset size: 56,154 measurements across 41 parameters.
- Format: CSV file with descriptive columns (examples include Timestamp, Height, Manufacturer, Instrument, Description).
- Variable-level details: fields include measurements such as Rain, Throughfall, Leaf Wetness Sensors (LWS1–LWS4), multiple AirT and RH sensors, soil moisture and temperature at various depths, soil EC, wind speed sensors (WS_Cup1–WS_Cup4), PAR sensors, total solar radiation, and numerous WXT and other environmental sensors.
- Depths/heights and layering clearly annotated (e.g., below-canopy vs. above-canopy; ground flora layer vs. tree canopy layer).
- Documentation of instrument manufacturers and specific instruments to support traceability and reproducibility.

## Data governance, sharing and metadata considerations
- The dataset includes rich instrument-level metadata (manufacturer, instrument, depth/height, description) to aid data provenance.
- Metadata completeness and clarity are central to reuse; publicly sharing underlying data and documentation is noted as a potential barrier in broader monitoring contexts.
- Time-standardization (GMT) enhances interoperability for multi-site monitoring frameworks.

## Relevance to environmental health monitoring and policy evaluation
- Demonstrates high-resolution, multi-parameter environmental monitoring across vertical forest structure, suitable for modeling pollutant deposition and ecosystem exposure.
- The structured data approach (clear timestamps, depth/height annotations, instrument details) supports transparent reporting, dashboarding, and policy-relevant analyses.
- Findings and methodology contribute to understanding ammonia deposition processes and inform future monitoring designs and governance.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Related publication: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024.