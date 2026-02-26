# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

## Overview
- Provides high-resolution meteorological data to support the ammonia enhancement experiment and estimation of ammonia deposition to forest ecosystems.
- Wind conditions below the forest canopy are used to control the ammonia enhancement experiment.
- Extends the prior 2021–2022 dataset from the same site.

## Data collection and site context
- Location: Glencorse woodland near Edinburgh (55.8539°, -3.2151°), altitude 200 m.
- Instrumentation: a 16 m mast extending 2 m above the canopy, installed adjacent to the ammonia enhancement manifold.
- Period and cadence:
  - Data collection: 1 January 2023 to 31 December 2024.
  - Measurements: every 20 seconds; 15-minute averaging.
  - All data recorded in GMT.
- Measured variables (sampled at multiple heights with above- and below-canopy coverage):
  - Atmospheric: air temperature, relative humidity, wind speed, wind direction, rainfall, barometric pressure, photosynthetically active radiation (PAR), total solar radiation.
  - Microclimate: leaf wetness (LWS) sensors at four heights (0.5 m, 2.0 m, 7.1 m, 11.6 m).
  - Soil: volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths (near surface, 10 cm, 15 cm).
  - Sensor details capture multiple instruments and manufacturers (e.g., Vaisala, HMP60, METER Environment, Campbell Scientific, Skye Instruments, Vector Instruments).
- Data scope note: above- and below-canopy measurements exist for rainfall, PAR, total solar radiation, wind, temperature, and humidity to contextualize the ammonia enhancement process.

## Data structure and metadata
- Dataset size: 70,176 measurements across 41 parameters.
- Format: CSV file with a structured, repeatable schema.
- Core fields (illustrative): Timestamp, Height (m), Manufacturer, Instrument, Description; followed by sensor-specific blocks such as Rain, Throughfall, LWS1–LWS4, AirT1–AirT4, RH1–RH4, Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3, WS_Cup1–WS_Cup4, PAR1–PAR2, Total_Solar1–Total_Solar2, WXT_WS1–WXT_BP2, WXT_WD1–WXT_RH2, etc.
- Descriptions and units are embedded per variable (e.g., Rain in mm, PAR in µmol m^-2 s^-1, Total_Solar in W m^-2, temperature in °C, VWC in m^3 m^-3, EC in dS m^-1).
- Data provenance and instrumentation metadata accompany measurements to support discoverability and reuse.

## Quality assurance and provenance
- Quality control: visual inspection to remove obvious errors from instrument malfunction, datalogger programming issues, and power outages; some data gaps due to sensor replacement.
- Data lineage: an explicit extension of the 2021–2022 Glencorse dataset; methodologies and complete experimental design described in related publications.
- Governance: funded by UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme; data contributed to the NERC Environmental Information Data Centre ecosystem.

## Access, reuse, and documentation
- Contextual relevance: feeds into models of ammonia deposition and the broader ammonia enhancement experiment physically controlling atmospheric deposition to forest ecosystems.
- Documentation: linked to full methodological details and prior data releases (Deshpande et al. 2024a; Deshpande et al. 2024b) with DOIs provided.
- Data discoverability: rich metadata including instrument type, height, manufacturer, and sensor description to facilitate data discovery and cross-study comparison.

## Governance, funding, and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- Key references:
  - Deshpande, A. G., et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ., 2024a.
  - Deshpande, A. G., et al. Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Glencorse, UK, 2021-2022, NERC EDS Environmental Information Data Centre, 2024b.