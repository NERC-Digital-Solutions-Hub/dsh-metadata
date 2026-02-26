# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- High-frequency meteorological dataset from a 12 m mast near the ammonia enhancement manifold at Queensberry Estate, Sri Lanka (coordinates 6.9693 N, 80.5911 E; altitude 1645 m).
- Time period: 1 January 2023 – 31 December 2024; data in Sri Lanka Standard Time (SLST).
- Extension of the 2022 dataset; wind conditions below the forest canopy control the ammonia enhancement experiment.
- Total: 70,176 measurements across 37 parameters, provided as CSV with 15-minute averages of measurements taken every 20 seconds.

## Data collection details
- Measurements taken at four heights for air temperature, relative humidity, and leaf wetness sensors (LWS1–LWS4) at 0.3 m, 2.0 m, 3.6 m, and 5.6 m.
- Additional above- and below-canopy measurements include:
  - Rain (above-canopy) and Throughfall (below-canopy)
  - Leaf wetness (LWS1–LWS4) near forest floor, ground flora, lower tree canopy, and upper canopy
  - Air temperature (AirT1–AirT4) and relative humidity (RH2–RH4) at multiple canopy layers
  - Soil volumetric water content (VWC1–VWC3), soil electrical conductivity (EC1–EC3), soil temperature (T1–T3) at surface and depths (surface, 10 cm, 15 cm)
  - Wind speed (WS_Cup1–WS_Cup3) and wind direction (WXT_WD1–WXT_WD2) at ground and canopy levels
  - PAR (PAR1–PAR2) and Total Solar Radiation (Total_Solar1–Total_Solar2)
  - Barometric pressure (WXT_BP1–WXT_BP2)
- Instruments from brands including Vaisala, METER Environment, Campbell Scientific, HS Hyquest Solutions, Vector Instruments, Skye Instruments; data recorded every 20 seconds and averaged to 15-minute intervals.
- Complete experimental design, methodology, analysis and findings described in Deshpande et al. (2024a); dataset extends the 2022 Queensberry site data (Deshpande et al., 2024b).

## Quality control
- Visual checks performed; obvious errors from instrument malfunction, datalogger issues, and power cuts removed.
- Some gaps occur due to sensor replacements; step changes in leaf wetness measurements reflect different baselines for individual leaf sensors.

## Data structure and format
- CSV dataset comprising 70,176 measurements across 37 parameters.
- Columns include: Timestamp, Height, Manufacturer, Instrument, Description, plus parameter-specific fields (e.g., Rain above-canopy, Throughfall below-canopy, LWS1–LWS4, AirT1–AirT4, RH2–RH4, Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3, WS_Cup1–WS_Cup3, PAR1–PAR2, Total_Solar1–Total_Solar2, WXT_WS1/WXT_WS2, WXT_WD1/WXT_WD2, WXT_BP1/BP2).

## Access, use and outputs
- Data suitable for exploring relationships between meteorological conditions and the ammonia enhancement experiment.
- Facilitates development of dashboards or self-serve data views for multi-parameter analysis across canopy layers and soil.
- Useful for estimating ammonia concentration and deposition rates and for validating forest-ecosystem deposition models.

## Funding
- Funded by the UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) for establishing the facility.

## References
- Deshpande, A. G. et al. 2024a. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ.
- Deshpande, A. G. et al. 2024b. Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Queensberry, Sri Lanka, 2022, NERC EDS Environmental Information Data Centre.