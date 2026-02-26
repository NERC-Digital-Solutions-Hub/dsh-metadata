Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

- Overview
  - A comprehensive meteorological dataset collected to support the Glencorse ammonia enhancement experiment, extending the 2021-22 dataset from the same site.
  - Purpose: to understand wind conditions and related meteorology that influence ammonia enhancement and deposition measurements.

- Data collection and instrumentation
  - Site and setup: 16 m mast located 2 m above the forest canopy, next to the ammonia enhancement manifold (Glencorse woodland; coordinates 55.8539 N, -3.2151 W; altitude 200 m).
  - Measurements include: air temperature, relative humidity, leaf wetness, wind speed at multiple heights; rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), total solar radiation (below and above canopy); soil volumetric water content, electrical conductivity, and temperature at three depths.
  - Sampling cadence: sensors record every 20 seconds; data averaged to 15-minute intervals.
  - Time frame: 1 January 2023 to 31 December 2024 (GMT).
  - Experimental control: wind conditions measured below the canopy are used to control the ammonia enhancement experiment.
  - Relation to prior work: dataset extends the 2021-22 data from the same site.

- Quality control
  - Visual QC applied; obvious instrumental malfunctions, datalogger issues, and power-cut errors removed.
  - Some gaps remain due to sensor replacement.

- Data structure and accessibility
  - Total observations: 70,176 measurements across 41 parameters.
  - File format: CSV with long-form column headers (e.g., Timestamp, Height, Instrument, Description) and wide parameter fields.
  - Sample details include measurements such as rainfall (above/below canopy), leaf wetness (four sensors near forest floor to canopy), air temperature and relative humidity at multiple canopy layers, soil moisture and temperature at multiple depths, wind speed/direction at various heights, PAR and solar radiation (below and above canopy), wind and meteorological variables from a variety of instruments and manufacturers.
  - Data are timestamped in GMT; heights are referenced to measurement locations (e.g., ground level, ground flora layer, tree canopy).

- Key variables and coverage
  - Atmospheric: air temperature, relative humidity, wind speed and direction, rainfall, barometric pressure, PAR, total solar radiation.
  - Canopy context: leaf wetness at multiple heights, near-canopy and above-canopy radiation and wind metrics.
  - Soil: volumetric water content, electrical conductivity, temperature at near-surface to 15 cm depths.
  - Instrument metadata: height, manufacturer, instrument type, and description for each measurement (embedded in the dataset structure).
  - All data are linked to 15-minute averaged timestamps for analysis continuity with the ammonia deposition measurements.

- Context and usage
  - Comprehensive basis for correlating meteorological conditions with ammonia concentration and deposition rates reported in the related studies (Deshpande et al., 2024a; 2024b).
  - Facilitates statistical analyses, model development, and scenario testing related to wind-controlled ammonia enhancement.
  - Dataset complements and extends prior work, enabling temporal comparisons across 2021-2022 and 2023-2024 periods.

- Funding and references
  - Funding: UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme.
  - References: 
    - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
    - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from Glencorse site, 2021-2022.